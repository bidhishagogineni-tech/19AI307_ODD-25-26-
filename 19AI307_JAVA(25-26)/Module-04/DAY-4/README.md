# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are building customizable robots using the Prototype Pattern. Clone an existing robot template and change its name and feature.

<img width="619" height="157" alt="image" src="https://github.com/user-attachments/assets/8d5b30a1-89de-417f-9687-b738072b8423" />


## AIM:
To design and implement a Java program that demonstrates the Prototype Design Pattern by creating a robot object and producing its clone. The cloned robot should replicate the original robot’s properties and allow modifications such as changing the robot's name and feature without affecting the original object.

## ALGORITHM :
1.Read number of books.

2.For each book: read title & author.

3.Library creates Book objects internally (composition).

4.Add books to its internal list.

5.Print all books stored in library.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

// Step 1: Create a Prototype interface
interface Prototype extends Cloneable {
    Prototype clone();
}

// Step 2: Create the Robot class implementing Prototype
class Robot implements Prototype {
    private String name;
    private String feature;

    public Robot(String name, String feature) {
        this.name = name;
        this.feature = feature;
    }

    // Clone method
    public Prototype clone() {
        try {
            return (Prototype) super.clone();
        } catch (CloneNotSupportedException e) {
            return null;
        }
    }

    public void setName(String name) {
        this.name = name;
    }

    public void setFeature(String feature) {
        this.feature = feature;
    }

    public void display() {
        System.out.println(name + " - " + feature);
    }
}

// Step 3: Main class
public class PrototypePatternDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Get input for original robot
        String name = sc.nextLine();
        String feature = sc.nextLine();

        // Create original robot
        Robot originalRobot = new Robot(name, feature);

        // Clone the robot
        Robot clonedRobot = (Robot) originalRobot.clone();

        // Display both
        System.out.print("Original Robot: ");
        originalRobot.display();

        System.out.print("Cloned Robot: ");
        clonedRobot.display();

        sc.close();
    }
}


```





## OUTPUT:

<img width="867" height="346" alt="image" src="https://github.com/user-attachments/assets/5d18497a-8b15-4a40-8240-296d54f5e0e5" />


## RESULT:
The program is being implemented successfully.
