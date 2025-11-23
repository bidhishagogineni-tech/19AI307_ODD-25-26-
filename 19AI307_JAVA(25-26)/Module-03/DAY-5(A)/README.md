# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to define an enum named GameLevel with three constants: EASY, MEDIUM, and HARD.

<img width="370" height="113" alt="image" src="https://github.com/user-attachments/assets/57bd406e-2521-4a20-bb15-1d6902f76ebe" />

## AIM:
To write a Java program that defines an enum named GameLevel with constants EASY, MEDIUM, and HARD, and displays the selected game level based on user input.

## ALGORITHM :
1.Read a string (game level) from the user.

2.Convert the input to uppercase.

3.Use the enum GameLevel to get the matching constant.

4.Print the selected game level.

5.End program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class GameLevelDemo {

    // Define the enum GameLevel
    public enum GameLevel {
        EASY,
        MEDIUM,
        HARD
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String userInput = scanner.nextLine().trim().toUpperCase(); // Read input and convert to uppercase

        try {
            // Convert the user's input string to a GameLevel enum constant
            GameLevel selectedLevel = GameLevel.valueOf(userInput);

            // Display the selected game level
            System.out.println("You selected game level: " + selectedLevel);

        } catch (IllegalArgumentException e) {
            System.out.println("Invalid game level entered. Please choose from EASY, MEDIUM, or HARD.");
        } finally {
            scanner.close(); // Close the scanner to prevent resource leaks
        }
    }
}

```





## OUTPUT:

<img width="803" height="211" alt="image" src="https://github.com/user-attachments/assets/e567af3d-49b8-482c-b318-43c7572cc240" />


## RESULT:

     The program is implemented successfully.

