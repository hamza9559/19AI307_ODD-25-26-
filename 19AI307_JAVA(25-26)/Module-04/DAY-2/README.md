# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
```
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.
Hidden Clue:
Use Singleton to manage shared access.
Count and log each print job submission.
Validate that state is preserved across all accesses.
```

## AIM:

To simulate a singleton Print Spooler Manager that handles all print job submissions and preserves the total job count across multiple accesses.
## ALGORITHM :
1.	Start the program and read the number of print job submissions.
2. Implement a singleton PrintSpoolerManager class with a private constructor and static getInstance() method.
3. Include a variable to track the total number of jobs submitted.
4. For each submission, get the singleton instance of the spooler.
5. Increment the job count and log the department name along with total jobs in the queue.
6. Ensure that the job count is preserved across all accesses to the singleton instance.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; // singleton instance
    private int jobCount; // total jobs in queue

    private PrintSpoolerManager() {
        jobCount = 0;
    }

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```





## OUTPUT:

<img width="1216" height="535" alt="image" src="https://github.com/user-attachments/assets/9690b6e6-5fdf-41d1-a5ae-fc63d0dba6e5" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
