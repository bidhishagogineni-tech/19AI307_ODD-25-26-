# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Check for Palindrome Number
<img width="306" height="186" alt="image" src="https://github.com/user-attachments/assets/adc58184-e2a0-49e7-91bd-1b6daf85a608" />

## AIM:
To check whether the given number is palindrome or not.

## ALGORITHM :
1.Start
2.Read a number
3.Store the number in a temporary variable
4.Reverse the number using a loop
5.If original number = reversed number → it is a palindrome
6.Else → not a palindrome
7.End





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class PalindromeNumber {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();
        
        if (isPalindrome(number)) {
            System.out.println(number + " is a Palindrome.");
        } else {
            System.out.println(number + " is not a Palindrome.");
        }
    }

    public static boolean isPalindrome(int num) {
        int originalNumber = num;  
        int reversedNumber = 0;    

        while (num != 0) {
            int digit = num % 10;     
            reversedNumber = reversedNumber * 10 + digit;  
            num = num / 10;          
        

        return originalNumber == reversedNumber;
    }
}


```





## OUTPUT:
<img width="643" height="244" alt="image" src="https://github.com/user-attachments/assets/a6a34cd1-e4c2-4027-aca1-3fa70de57c9b" />



## RESULT:
The program successfully checks the given number and displays whether it is a Palindrome or not.
