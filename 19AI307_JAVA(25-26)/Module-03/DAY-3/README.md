# Ex.No:3(C) ABSTRACTION

## QUESTION:
```
Description:
Create abstract class GameScore with method finalScore().
Subclasses:
ArcadeGame: score = baseScore + (level × 100)\
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500
Input Format:
First line: 1 or 2
Second line: base, level (or attempts)
Output Format:
Final score (int)
```

## AIM:
To calculate the final game score using abstraction with different scoring rules for ArcadeGame and PuzzleGame.

## ALGORITHM :
1.	Start the program and read the type of game from the user.
2. Create an abstract class GameScore with an abstract method finalScore().
3. Implement ArcadeGame and PuzzleGame classes with their specific score formulas.
4. Based on input type, create the appropriate game object.
5. Call the finalScore() method to calculate the score.
6. Display the final score as the output.




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054 
*/
```

## SOURCE CODE:
```JAVA
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        return (attempts <= 3) ? 1000 - (attempts * 100) : 500;
    }
}

public class GameScoreCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;

        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());
    }
}
```






## OUTPUT:



<img width="1225" height="322" alt="image" src="https://github.com/user-attachments/assets/e14a1132-c5cf-4cc4-ad92-1d5103c7dbdb" />


## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
