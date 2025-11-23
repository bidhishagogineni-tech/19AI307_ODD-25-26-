# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
<img width="708" height="177" alt="image" src="https://github.com/user-attachments/assets/5454069e-d700-4ff6-8ea2-a6f5b6de369f" />


## AIM:
To write a Java program that reads user input from the keyboard using InputStreamReader and displays a greeting message with the entered name.

## ALGORITHM :
1.	Start the program.

2.Create an InputStreamReader to read from System.in.

3.Wrap it with BufferedReader for easier reading.

4.Read the user's input as a string.

5.Print "Hello, <name>!".

6.End program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Greeting {
    public static void main(String[] args) {
        try {
            // Create an InputStreamReader wrapped in BufferedReader
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);
            
            // Read input from the user
            String name = br.readLine();
            
            // Display greeting
            System.out.println("Hello, " + name + "!");
            
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}

```






## OUTPUT:

<img width="519" height="214" alt="image" src="https://github.com/user-attachments/assets/edf5aada-bb1b-44ef-9acb-23ea8d848297" />


## RESULT:

The program is being implemented successfully.
