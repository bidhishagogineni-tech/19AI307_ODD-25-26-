# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
area(int side) for square
area(int length, int breadth) for rectangle
area(double radius) for circle

<img width="392" height="180" alt="image" src="https://github.com/user-attachments/assets/127233b5-7b53-47be-a500-07b2f4692063" />


## AIM:
To write a Java program that calculates the area of different shapes (square, rectangle, and circle) using method overloading by defining multiple area() methods with different parameter lists.

## ALGORITHM :
1.Start the program.
2.Create a class AreaCalculator.
3.Define an overloaded method area(int side) to calculate the area of a square.
4.Define an overloaded method area(int length, int breadth) to calculate the area of a rectangle.
5.Define an overloaded method area(double radius) to calculate the area of a circle.
6.In the main method, create an object of the AreaCalculator class.
7.Read input values for square side, rectangle dimensions, and circle radius.
8.Call the respective area() methods and store the results.
9.Display the calculated areas.
10.End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class AreaCalculator {
    public static int area(int side) {
        return side * side;
    }

    public static int area(int length, int breadth) {
        return length * breadth;
    }

    public static double area(double radius) {
        return Math.PI * radius * radius;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int side = sc.nextInt();
        System.out.println("Area of square: " + area(side));

        int l = sc.nextInt();
        int b = sc.nextInt();
        System.out.println("Area of rectangle: " + area(l, b));

        double r = sc.nextDouble();
        System.out.println("Area of circle: " + area(r));
    }
}

```





## OUTPUT:

<img width="855" height="389" alt="image" src="https://github.com/user-attachments/assets/d9a7df61-99f7-4c87-9f68-1476b8f0692e" />


## RESULT:
   The program is being implemented successfully.
