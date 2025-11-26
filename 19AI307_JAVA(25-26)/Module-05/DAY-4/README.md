# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To create two threads, assign them names and priorities, and display their details.

## ALGORITHM :
1.	Start the program and read names for two threads from the user.
2. Create a class MyThread that extends Thread and initializes the thread name.
3. Instantiate two thread objects with the given names.
4. Set the priority of the first thread to 4 and the second thread to 2.
5. Display the details of both threads using System.out.println().
6. End the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class MyThread extends Thread {
    MyThread(String name) {
        super(name);
    }
    public void run() {}
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);
    }
}
```






## OUTPUT:

<img width="1287" height="349" alt="image" src="https://github.com/user-attachments/assets/29c396e8-02bc-4d42-8c4d-7e7b34ce20c9" />



## RESULT:
The program executed successfully and displayed the names and priorities of the two threads as set by the user.
