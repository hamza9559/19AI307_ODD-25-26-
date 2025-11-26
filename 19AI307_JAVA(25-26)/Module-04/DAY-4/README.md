# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are building customizable robots using the Prototype Pattern. Clone an existing robot template and change its name and feature.

## AIM:
To implement the Prototype Pattern by cloning a robot template and customizing its attributes.

## ALGORITHM :
1.	Start the program and read the robot's name and feature from the user.
2. Create an original Robot object with the given attributes.
3. Implement the clone() method in the Robot class using Cloneable.
4. Clone the original robot to create a new robot object.
5. Display the details of both the original and cloned robot.
6. End the program, ensuring that the cloned robot can be modified independently if needed.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.util.*;

class Robot implements Cloneable {
    private String name;
    private String feature;

    public Robot(String name, String feature) {
        this.name = name;
        this.feature = feature;
    }

    public Robot clone() {
        try {
            return (Robot) super.clone();
        } catch (CloneNotSupportedException e) {
            return null;
        }
    }

    public String toString() {
        return name + " - " + feature;
    }
}

public class PrototypeDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        String feature = sc.nextLine();

        Robot original = new Robot(name, feature);
        Robot clone = original.clone();

        System.out.println("Original Robot: " + original);
        System.out.println("Cloned Robot: " + clone);

        sc.close();
    }
}
```





## OUTPUT:

<img width="1264" height="429" alt="image" src="https://github.com/user-attachments/assets/618e6001-1bcc-4f34-ac59-02de0837ad48" />



## RESULT:
The program executed successfully and demonstrated cloning of a robot using the Prototype Pattern, preserving the original while creating a duplicate.
