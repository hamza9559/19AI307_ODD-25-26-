# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To create a Calculator class with one static method and one non-static method and use them to display a message and perform addition.

## ALGORITHM :
1.	Create a class with a non-static add method and a static info method.
2. Read two integer inputs from the user.
3. Call the static method using the class name to display readiness.
4. Create an object of the class to call the non-static add method.
5. Display the result of addition and end the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        Calculator.info();

        Calculator calc = new Calculator();
        System.out.println("Sum: " + calc.add(num1, num2));

        sc.close();
    }
}
```






## OUTPUT:

<img width="863" height="393" alt="image" src="https://github.com/user-attachments/assets/f8d07d6f-b1ff-43e4-b04a-04b9f68a1f3e" />


## RESULT:

Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
