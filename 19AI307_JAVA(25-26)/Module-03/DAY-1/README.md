# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
```
finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).
```

## AIM:
To calculate and display the final payable amount for different types of gold customers based on discounts and cashback using inheritance.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read customer details and gold rate from the user.
4. Create the appropriate customer object based on customer type.
5. Calculate the final price (and cashback for PremiumCustomer).
6. Display all the required customer details and final payable amount.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100.0;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 2.0; 
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 5.0; 
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01; 
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class JewelryStore {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = sc.nextDouble();
        double rate = sc.nextDouble();

        Customer customer;
        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(id, name, weight, rate);
        } else if (type.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(id, name, weight, rate);
        } else {
            customer = new Customer(id, name, weight, rate);
        }

        customer.display();
        sc.close();
    }
}

```






## OUTPUT:
<img width="882" height="782" alt="image" src="https://github.com/user-attachments/assets/fc382f42-55af-4418-b7e6-e7fa0c961ae2" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
