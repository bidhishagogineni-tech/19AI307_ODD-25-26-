# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Create a class with a private constructor and a static factory method.

<img width="307" height="164" alt="image" src="https://github.com/user-attachments/assets/bb659931-69ca-4ae5-b25d-56b231b84ad0" />

## AIM:
To write a Java program that creates a class with a private constructor and a static factory method to create and return objects, and to display the employee details entered by the user.

## ALGORITHM :
1.Start the program.
2.Create a class Employee with private instance variables.
3.Define a private constructor inside the class.
4.Provide a static factory method to create and return an object of the class.
5.In the main method, read the name and ID from the user.
6.Call the factory method to create the Employee object.
7.Display the employee details.
8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by:GOGINENI BIDHISHA 
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

 ```
import java.util.Scanner;
class prog{
    private String name;
    private int id;
    
    private prog(String name,int id) {
        this.name=name;
        this.id=id;
    }
    public void display() {
        System.out.println("Employee Details: ");
        System.out.println("Name: "+this.name);
        System.out.println("ID  : "+this.id);
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int id=sc.nextInt();
        prog p=new prog(name,id);
        p.display();
    }
}
```





## OUTPUT:
<img width="646" height="389" alt="Screenshot 2025-11-21 153756" src="https://github.com/user-attachments/assets/373be1f5-b151-4408-9dc2-000a886a733e" />




## RESULT:

The program is executed successfully.
