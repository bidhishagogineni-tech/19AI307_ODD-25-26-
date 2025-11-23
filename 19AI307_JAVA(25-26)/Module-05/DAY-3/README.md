# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

<img width="652" height="177" alt="image" src="https://github.com/user-attachments/assets/31fbc930-5236-47bd-b62c-974535023872" />

## AIM:
To write a Java program that overwrites the content of a file using FileWriter, ensuring that any previous content is erased and replaced with the new user input.

## ALGORITHM :
1.Read a line of text from the user.

2.Create a FileWriter object with overwrite mode enabled (new FileWriter("output.txt")).

3.Write the user input into the file.

4.Close the file writer.

5.Print a success message.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class OverwriteFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String data = sc.nextLine();

        try {
            FileWriter fw = new FileWriter("output.txt"); // overwrite mode
            fw.write(data);
            fw.close();
            System.out.println("File content overwritten successfully.");
        } catch (IOException e) {
            System.out.println("Error writing to file.");
        }
    }
}


```






## OUTPUT:
<img width="875" height="245" alt="image" src="https://github.com/user-attachments/assets/d49b949d-7746-43ec-8e72-19ec608ace06" />



## RESULT:

The program is being implemented successfully.
