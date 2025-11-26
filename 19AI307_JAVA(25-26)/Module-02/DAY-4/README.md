# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program with a variable declared inside a for-loop. Try to access it outside the loop and explain the result.

## AIM:
To demonstrate variable scope by declaring a variable inside a loop and showing that it cannot be accessed outside the loop.

## ALGORITHM :
1.	Start the program and take input from the user.
2. Use a for-loop and declare a variable inside it.
3. Print the value of the variable within the loop.
4. Try to access the variable outside the loop (which will cause an error).
5. Conclude that variables inside loops have local scope only.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.util.Scanner;

public class LoopScopeDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();  // Take input from user

        for (int i = 0; i < n; i++) {
            int loopVar = i * 2;
            System.out.println("Inside loop iteration " + i + ", loopVar = " + loopVar);
        }

        scanner.close();
    }
}
```





## OUTPUT:

<img width="1208" height="501" alt="image" src="https://github.com/user-attachments/assets/4a8f1df6-a208-4c00-a6e0-dd3bacd5cb1e" />


## RESULT:

Thus, the program executed successfully and showed that a variable declared inside a for-loop is only accessible within the loop block, proving its limited scope.
