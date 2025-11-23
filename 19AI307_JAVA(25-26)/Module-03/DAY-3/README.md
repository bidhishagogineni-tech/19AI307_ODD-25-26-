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

<img width="411" height="212" alt="image" src="https://github.com/user-attachments/assets/00d10cc1-f1f7-4d1f-8138-5b2f17c9f38b" />

## AIM:
To write a Java program that uses abstract classes and inheritance to compute final game scores for different game types (Arcade and Puzzle) by overriding an abstract method.

## ALGORITHM :
1.Start the program.
2.Read the game type (1 for Arcade, 2 for Puzzle).
3.If game type is 1:
  Read base score and level.
  Calculate score = base + (level × 100).
4.If game type is 2:
  Read attempts.
  If attempts ≤ 3, score = 1000 − (attempts × 100).
  Else, score = 500.
5.Display the final score.
6.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

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

public class Main {
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

![Uploading image.png…]()


## RESULT:
The program is implemented successfully.
