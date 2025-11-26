# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)

For example:

Input	Result
1 100 3
400
2 4
500


## AIM:
To write a Java program using abstract classes and method overriding to calculate the final score for different game types: Arcade Game and Puzzle Game.

## ALGORITHM :
1.Create an abstract class GameScore with an abstract method finalScore().

2.Create ArcadeGame class extending GameScore with base score and level.

3.Override finalScore() in ArcadeGame to calculate score using:
baseScore + (level * 100).

4.Create PuzzleGame class extending GameScore with number of attempts.

5.Override finalScore() in PuzzleGame to compute score:

6.Read game type and input values from the user.

7.Create the appropriate game object based on game type.

8.Call the overridden finalScore() method to display the score.



## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    private int baseScore;
    private int level;

    public ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    private int attempts;

    public PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        if (attempts <= 3) {
            return 1000 - (attempts * 100);
        } else {
            return 500;
        }
    }
}

public class GameScoreSystem {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int gameType = scanner.nextInt();

        GameScore gameScore;
        if (gameType == 1) {
            int base = scanner.nextInt();
            int level = scanner.nextInt();
            gameScore = new ArcadeGame(base, level);
        } else if (gameType == 2) {
            int attempts = scanner.nextInt();
            gameScore = new PuzzleGame(attempts);
        } else {
            System.out.println("Invalid game type");
            scanner.close();
            return;
        }

        System.out.println(gameScore.finalScore());

        scanner.close();
    }
}

```




## OUTPUT:
<img width="445" height="299" alt="image" src="https://github.com/user-attachments/assets/4622c197-d371-43e1-a9f4-65058355c608" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
