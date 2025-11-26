# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Use a synchronized block (not method) to safely increment a shared counter using multiple threads.
## AIM:
To safely increment a shared counter using multiple threads with a synchronized block to prevent race conditions.

## ALGORITHM :
1.	Start the program and read the number of threads and increments per thread.
2. Declare a shared counter variable and an object to act as a lock.
3. Create multiple threads, each performing the specified number of increments.
4. Use a synchronized block on the lock object to safely increment the counter.
5. Start all threads and wait for their completion using join().
6. Display the final value of the counter.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054 
*/
```

## SOURCE CODE:

```JAVA
import java.util.*;

public class Main {
    private static int counter = 0;
    private static final Object lock = new Object();

    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int nThreads = sc.nextInt();
        int increments = sc.nextInt();

        Thread[] threads = new Thread[nThreads];

        for (int i = 0; i < nThreads; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < increments; j++) {
                    synchronized(lock) {
                        counter++;
                    }
                }
            });
            threads[i].start();
        }

        for (Thread t : threads) {
            t.join();
        }

        System.out.println("Final count: " + counter);
    }
}
```





## OUTPUT:

<img width="1275" height="451" alt="image" src="https://github.com/user-attachments/assets/e4bd77db-172b-44f8-bc9a-c66220ff2808" />



## RESULT:
The program executed successfully and displayed the correct final count, ensuring thread-safe increments using a synchronized block.
