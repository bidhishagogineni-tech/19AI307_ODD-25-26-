# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

<img width="305" height="142" alt="image" src="https://github.com/user-attachments/assets/f42e9010-6e58-44ec-a072-47b3f4cbbe81" />

## AIM:

To write a Java program that creates a class Employee containing a display() method which returns the current object using this, and another method that calls display().printName() to print the employee’s name.
## ALGORITHM :
1.Start the program.
2.Create a class Employee with a variable name.
3.Define setName() to assign the name using this.name = name.
4.Define display() and return the current object using this.
5.Define printName() to print the employee's name.
6.In the main method, read the employee name from the user.
7.Create an Employee object and set the name.
8.Call object.display().printName() to print the name.
9.End the program.
## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  21223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Employee {
    String name;
    void setName(String name) {
        this.name=name;
    }
    Employee display(){
        return this;
    }
    void printName(){
        System.out.println("Employee Name: "+this.name);
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        Employee emp=new Employee();
        emp.setName(name);
        emp.display().printName();
    }
}

```





## OUTPUT:

<img width="658" height="249" alt="image" src="https://github.com/user-attachments/assets/14bfe64d-288f-4853-beae-d61bd76e8b7d" />


## RESULT:
   The program is implemented successfully.
