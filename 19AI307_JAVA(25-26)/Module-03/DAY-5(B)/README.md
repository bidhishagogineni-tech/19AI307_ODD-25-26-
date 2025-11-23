# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

<img width="351" height="224" alt="image" src="https://github.com/user-attachments/assets/ade27c9d-bd0e-495e-8135-711e17036700" />


## AIM:
To write a Java program that reverses a number using Integer wrapper class methods and compares the reversed number with the original to determine whether it is a palindrome.

## ALGORITHM :
1.Read an integer from the user.

2.Convert the integer to a string using Integer.toString().

3.Reverse the string using a loop or StringBuilder.

4.Convert the reversed string back to an integer using Integer.parseInt().

5.Compare the original number with the reversed number.

6.If both are equal → it is a palindrome.

7.Else → not a palindrome.

8.Print the reversed number.




## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ReverseNumberComparison {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get input from the user
        String input = scanner.nextLine();

        try {
            Integer originalNumber = Integer.parseInt(input);
            Integer number = originalNumber;
            Integer reversedNumber = 0;

            // Reverse the number
            while (number != 0) {
                int digit = number % 10;
                reversedNumber = reversedNumber * 10 + digit;
                number /= 10;
            }

            // Compare with original number
            if (originalNumber.equals(reversedNumber)) {
                System.out.println(originalNumber + " is a palindrome number.");
            } else {
                System.out.println(originalNumber + " is not a palindrome number.");
                System.out.println("Reversed Number: " + reversedNumber);
            }

        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid integer.");
        }

        scanner.close();
    }
}


```





## OUTPUT:

<img width="802" height="256" alt="image" src="https://github.com/user-attachments/assets/e73b0394-dff5-4134-bef1-12a4384946ff" />


## RESULT:

  The program is implemented successfully.
