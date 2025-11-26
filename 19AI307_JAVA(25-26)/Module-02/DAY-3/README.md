# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:

To create a BankAccount class with private variables and use getter and setter methods to access and modify them.
## ALGORITHM :
1.	Define a class with private variables accountNumber and balance.
2. Provide public getter and setter methods to access these variables.
3. Create an object of the BankAccount class in the main method.
4. Read account details from the user and set the values using setter methods.
5. Display the stored values using getter methods.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: HAMZA FAROOQUE 
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class BankAccount {

    private String accountNumber;
    private double balance;

    public String getAccountNumber() {
        return accountNumber;
    }

    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }


    public double getBalance() {
        return balance;
    }

    public void setBalance(double balance) {
        this.balance = balance;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        BankAccount account = new BankAccount();



        String accNum = scanner.nextLine();
        account.setAccountNumber(accNum);


        double bal = scanner.nextDouble();
        account.setBalance(bal);


        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Balance: " + account.getBalance());

        scanner.close();
    }
}
```






## OUTPUT:

<img width="1229" height="451" alt="image" src="https://github.com/user-attachments/assets/1095dc6c-c093-454d-9775-317a63a6cb69" />


## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
