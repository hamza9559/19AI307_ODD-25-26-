# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Find the largest digit in a number using wrapper class methods.

## AIM:
To find and display the largest digit in a number using wrapper class methods.

## ALGORITHM :
1.	Start the program and read the number from the user.
2. Convert the number into a string using a wrapper class method.
3. Initialize a variable to track the largest digit.
4. Traverse each digit in the string representation of the number.
5. Convert each character to a digit using wrapper class methods and compare.
6. Print the largest digit found.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.util.Scanner;

public class LargestDigit {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        String numberStr = Integer.toString(num); // Using wrapper class method
        int largest = Integer.MIN_VALUE;

        for (int i = 0; i < numberStr.length(); i++) {
            int digit = Character.getNumericValue(numberStr.charAt(i)); // Wrapper class method
            if (digit > largest) {
                largest = digit;
            }
        }

        System.out.println("The largest digit is: " + largest);
    }
}
```





## OUTPUT:

<img width="1224" height="384" alt="image" src="https://github.com/user-attachments/assets/08a011bd-014a-4006-8336-9a7126e3b445" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
