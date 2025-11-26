# Ex.No:3(D)    INTERFACE 

## QUESTION:
```
Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.

LenientJudge: WIN if diff ≥ 5, DRAW if < 5

StrictJudge: WIN if diff ≥ 10, DRAW if < 10

```


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
Program to implement a Interface using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.util.*;

interface BoxingJudge {
    String decide(int p1, int p2);
}

class LenientJudge implements BoxingJudge {
    public String decide(int p1, int p2) {
        if (Math.abs(p1 - p2) >= 5)
            return (p1 > p2) ? "WIN" : "LOSE";
        return "DRAW";
    }
}

class StrictJudge implements BoxingJudge {
    public String decide(int p1, int p2) {
        if (Math.abs(p1 - p2) >= 10)
            return (p1 > p2) ? "WIN" : "LOSE";
        return "DRAW";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt();
        int type = sc.nextInt();
        BoxingJudge judge = (type == 1) ? new LenientJudge() : new StrictJudge();
        System.out.println(judge.decide(a, b));
    }
}

```





## OUTPUT:


<img width="1220" height="415" alt="image" src="https://github.com/user-attachments/assets/1dfbc65c-1db6-40b4-94c7-f81635c8ef7f" />


## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
