# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the maximum odd number in an array

<img width="281" height="395" alt="image" src="https://github.com/user-attachments/assets/93f1bcfd-38bc-40e1-b925-39e731552fde" />

## AIM:

To write a Java program to find the maximum odd number in an array.

## ALGORITHM :
1.	Start
2. Read the size of the array
3. Read all array elements
4. Check each element:
    >If it is odd, compare and update the maximum odd value
5. If no odd number exists → display "No odd number found"
6. Otherwise → display the maximum odd number
7. End



## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class MaxOddNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }

        int maxOdd = Integer.MIN_VALUE;
        for (int num : arr) {
            if (num % 2 != 0 && num > maxOdd) {
                maxOdd = num;
            }
        }

        if (maxOdd == Integer.MIN_VALUE) {
            System.out.println("No odd number found");
        } else {
            System.out.println(maxOdd);
        }

        scanner.close();
    }
}

```





## OUTPUT:

<img width="605" height="523" alt="image" src="https://github.com/user-attachments/assets/74a5102f-6916-49f9-b4ab-d1efcba37715" />



## RESULT:

The program successfully finds and displays the maximum odd number in the array, or prints “No odd number found” if none exists.
