# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To write a Java program that creates a class Smartphone with private instance variables brand, model, and storageCapacity, provides getter and setter methods, and includes a method increaseStorage() to increase storage capacity.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Smartphone with private variables:
   brand
   model
   storageCapacity
4.Provide public getter and setter methods for each variable.
5.Define a method increaseStorage(int value) that increases the storage capacity.
6.In the main method:
  Create a Scanner object to take user input.
  Create an object of Smartphone class.
  Get brand, model, and storage input from the user.
  Call the setter methods to store values.
  Ask the user for additional storage to increase.
  Call increaseStorage().
  Display the updated details.
7.End the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by:GOGINENI BIDHISHA 
RegisterNumber:  21223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Smartphone phone = new Smartphone();

        phone.setBrand(sc.nextLine());
        phone.setModel(sc.nextLine());
        phone.setStorageCapacity(sc.nextInt());

        int extra = sc.nextInt();

        phone.increaseStorage(extra);
        phone.display();
       sc.close();
    }
}

```





## OUTPUT:

<img width="857" height="478" alt="image" src="https://github.com/user-attachments/assets/c429ded1-f3e8-48b5-a44c-a7d82302c9f1" />


## RESULT:
The Java program was successfully executed.
