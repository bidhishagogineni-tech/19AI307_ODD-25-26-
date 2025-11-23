# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that stores input strings in an array and prints each string in uppercase while preventing a NullPointerException by checking for null values before calling the .toUpperCase() method.

## ALGORITHM :
1.Start the program.

2.Declare or create a String array.

3.Read input strings from the user and store them in the array.

4.Traverse the array using a loop.

5.For each element, check if the string is not null.

     If the element is not null → convert it to uppercase and print it.

     If the element is null → skip processing to avoid NullPointerException.

6.End the program.




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class NullPointerArrayExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.next();
        String str = input.equalsIgnoreCase("null") ? null : input;

        try {
            System.out.println(str.toUpperCase());
        } catch (NullPointerException e) {
            System.out.println("Null element");
        }

        sc.close();
    }
}


```






## OUTPUT:
<img width="507" height="251" alt="image" src="https://github.com/user-attachments/assets/a58b5548-2ccb-4def-ae84-f54100218bdf" />



## RESULT:
The program is implemented successfully.

