# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

<img width="249" height="149" alt="image" src="https://github.com/user-attachments/assets/8d06aeba-43ce-4bfe-a8e3-41aa01474b38" />

## AIM:
To create a class Car with attributes brand, model, and year, create two objects of the class, and print their details.

## ALGORITHM :
1.	Start the program.
2. Create a class named Car.
3. Inside the class, declare three attributes:
    i.String brand
    ii.String model
    iii.int year
4.Create a constructor to initialize these attributes.
5.In the main method:
    i.Create two objects of the Car class with different values.
    ii.Print the details of both cars in the required format.
6.End the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:212223040048  
*/
```

## SOURCE CODE:

```
class Car{
    String brand;
    String model;
    int year;
    
}
public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;
        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;
        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}
```





## OUTPUT:

<img width="615" height="201" alt="image" src="https://github.com/user-attachments/assets/2699395e-9081-4ae0-b21f-488f79f47ad3" />


## RESULT:
The program successfully created two Car objects and printed.
