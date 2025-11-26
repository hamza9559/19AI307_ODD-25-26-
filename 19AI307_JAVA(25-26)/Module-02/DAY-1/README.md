# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To create a Vehicle class with attributes and display the details of two vehicles entered by the user.

## ALGORITHM :
1.	Start the program and read the vehicle number, type, and owner details for two vehicles.
2. Create Vehicle class objects using the input values.
3. Store each vehicle’s details in its respective object.
4. Call the method to display the details in the required format.
5. End the program after printing the output.




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Vehicle {
    String number;
    String type;
    String owner;

    Vehicle(String number, String type, String owner) {
        this.number = number;
        this.type = type;
        this.owner = owner;
    }

    void printDetails() {
        System.out.println(number + " | " + type + " | " + owner);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String number1 = scanner.next();
        String type1 = scanner.next();
        String owner1 = scanner.next();

        String number2 = scanner.next();
        String type2 = scanner.next();
        String owner2 = scanner.next();

        Vehicle v1 = new Vehicle(number1, type1, owner1);
        Vehicle v2 = new Vehicle(number2, type2, owner2);

        v1.printDetails();
        v2.printDetails();

        scanner.close();
    }
}
```






## OUTPUT:
<img width="1219" height="331" alt="image" src="https://github.com/user-attachments/assets/eaae20d7-4799-4a23-8b5c-ff3471d0ff97" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.

