# Ex.No:2(B) METHODS

## QUESTION:
Create a method printName(String name) that gets input from the user for the string and prints "Hello, " followed by the name passed.

## AIM:
To write a Java method printName(String name) that takes a user's name as input and prints "Hello, <name>".

## ALGORITHM :
1.Start the program.
2.Import the necessary package 'java.util'
3.Import the Scanner class for user input.
4.Define a method printName(String name) that prints:
   "Hello, " + name
4.In the main() method:
a. Create a Scanner object.
b. Ask the user to enter their name.
c. Store the input in a String variable.
d. Call the printName() method and pass the name as argument.
5.End the program.




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.*;
public class main{
    static String printName(String name){
        return "Hello, "+name;
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        String s=printName(str);
        System.out.print(s);
    }
}
```





## OUTPUT:

<img width="451" height="173" alt="image" src="https://github.com/user-attachments/assets/a525d7df-f8ba-4797-a0b7-f6dc850f6240" />



## RESULT:
The program was successfully executed.
