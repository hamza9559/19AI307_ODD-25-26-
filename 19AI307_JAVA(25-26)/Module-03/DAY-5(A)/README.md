# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To determine whether the fighter wins, loses, or draws using different judging criteria based on the judge type.

## ALGORITHM :
1.	Start the program and read both player scores and judge type.
2. Define an interface BoxingJudge with a decide() method.
3. Implement LenientJudge and StrictJudge classes with different score difference rules.
4. Create the correct judge object based on the input type.
5. Call the decide() method to evaluate WIN, LOSE, or DRAW.
6. Display the result returned by the judge.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.*;

public class OuterClass {
    

    class InnerClass {
        void greet(String name) {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine().trim();

  
        OuterClass outer = new OuterClass();

        OuterClass.InnerClass inner = outer.new InnerClass();

        inner.greet(name);
    }
}
```






## OUTPUT:

<img width="1231" height="382" alt="image" src="https://github.com/user-attachments/assets/7a91c75f-0460-4f80-adcb-dab34dbb8a3f" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
