# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to remove all vowels from a given string.

<img width="399" height="109" alt="image" src="https://github.com/user-attachments/assets/5fcef11b-3280-44cc-9119-87b7285584f4" />

## AIM:
To write a Java program that removes all vowels from a given string and displays the string without vowels.

## ALGORITHM :
1.	Start
2. Read a string from the user
3. Create an empty string to store the result
4. Traverse each character of the string
5. If the character is not a vowel, add it to the result
6. Print the result string
7. End





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:
```
import java.util.*;

public class RemoveVowels {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String result = str.replaceAll("[AEIOUaeiou]", "");
        System.out.println("String without vowels: " + result);
    }
}


```






## OUTPUT:
<img width="816" height="252" alt="image" src="https://github.com/user-attachments/assets/e2e706a9-6ab6-407e-a4ca-c9df69cce2b7" />



## RESULT:
The program successfully removes all vowels from the given string and displays the result.
