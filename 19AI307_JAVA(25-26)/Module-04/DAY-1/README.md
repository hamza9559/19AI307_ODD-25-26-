# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
```
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?
```

## AIM:

To read multiple strings into a String array and print each string in uppercase while preventing NullPointerException by checking for null elements.
## ALGORITHM :
1.	Start the program.
2. Create a Scanner object to take input from the user.
3. Declare a String array to store the input strings.
4. Store each entered string into the array.
5. For each string in the array:
6. Check if the element is not null.
7. If valid, print it in uppercase; otherwise print a message for null value.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

public class StringArrayUppercase {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String[] arr = new String[4];
        int i = 0;
        while (sc.hasNextLine() && i < arr.length) {
            arr[i] = sc.nextLine().trim();
            i++;
        }
        for (int j = 0; j < i; j++) {
            if (arr[j] == null || arr[j].equalsIgnoreCase("null")) {
                System.out.println("Null element");
            } else {
                System.out.println(arr[j].toUpperCase());
            }
        }
        sc.close();
    }
}
```






## OUTPUT:

<img width="1269" height="366" alt="image" src="https://github.com/user-attachments/assets/e60c07b2-4dbd-4bdb-b830-561171c6aa69" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
