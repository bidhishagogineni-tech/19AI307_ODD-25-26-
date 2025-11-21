# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
finalPrice = purchaseWeight * (goldRatePerGram - discount)

## AIM:
To develop a Java program using inheritance to calculate gold purchase prices for different types of customers—Regular and Premium—where each receives different discount benefits. Premium customers also receive cashback based on their final price.

## ALGORITHM :
1.Start the program.
2.Create a base class Customer with attributes and methods to calculate the final price.
3.Create RegularCustomer class with a fixed 2% discount.
4.Create PremiumCustomer class with a 5% discount and 1% cashback.
5.Input gold rate, customer details, and purchase weight.
6.Create objects for both Regular and Premium customers.
7.Calculate final price using discount rules.
8.For PremiumCustomer, calculate cashback.
9.Display the details of each customer.
10.End the program.



## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

// Subclass for RegularCustomer
class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2.0;
    }

    void display() {
    DecimalFormat df = new DecimalFormat("0.00");
    System.out.println("Customer ID: " + customerId);
    System.out.println("Name: " + name);
    System.out.println("Customer Type: Regular");
    System.out.println("Purchase Weight: " + purchaseWeight + " grams");
    System.out.println("Gold Rate per Gram: " + goldRatePerGram);
    System.out.println("Discount: " + (int)getDiscountRate() + "%");
    System.out.println("Final Price: " + df.format(calculateFinalPrice()));
}

    }

// Subclass for PremiumCustomer
class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5.0;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01; // 1% cashback
    }

    void display() {
    DecimalFormat df = new DecimalFormat("0.00");
    System.out.println("Customer ID: " + customerId);
    System.out.println("Name: " + name);
    System.out.println("Customer Type: Premium");
    System.out.println("Purchase Weight: " + purchaseWeight + " grams");
    System.out.println("Gold Rate per Gram: " + goldRatePerGram);
    System.out.println("Discount: " + (int)getDiscountRate() + "%");
    System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    System.out.println("Cashback: " + df.format(getCashback()));
}

    }
public class GoldStore {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        DecimalFormat df = new DecimalFormat("0.00");

      
        String type = sc.next().toLowerCase();

        String id = sc.next();

        String name = sc.next();

        double weight = sc.nextDouble();

        double goldRate = sc.nextDouble();

        Customer c;
        if (type.equals("regular")) {
            c = new RegularCustomer(id, name, weight, goldRate);
        } else if (type.equals("premium")) {
            c = new PremiumCustomer(id, name, weight, goldRate);
        } else {
            c = new Customer(id, name, weight, goldRate);
        }

        c.display();

        sc.close();
    }
}


```





## OUTPUT:
<img width="802" height="652" alt="image" src="https://github.com/user-attachments/assets/6bf3b70e-8359-4eb1-b63e-cdaf712205a0" />



## RESULT:
The program is implemented successfully.

