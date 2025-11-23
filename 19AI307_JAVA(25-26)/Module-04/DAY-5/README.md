# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
<img width="837" height="624" alt="image" src="https://github.com/user-attachments/assets/41d4c959-8f31-4722-a43b-9d7eefb47e3d" />


## AIM:
The aim of this program is to implement the Model-View-Controller (MVC) design pattern in Java to manage a simple bank account system. The Model stores the account balance, the Controller performs operations such as deposit and withdrawal, and the View displays the updated balance or error messages. This structure helps separate business logic, user interaction, and output display, ensuring clean, modular, and maintainable code.

## ALGORITHM :
1.Read the initial bank balance.

2.Create Model (BankAccount) to store and update balance.

3.Create View to display balance or error messages.

4.Create Controller to perform deposit/withdraw actions on the Model.

5.Read number of operations.

6.For each operation:

If "deposit X" → controller deposits and view displays updated balance.

If "withdraw X":

If enough balance → withdraw and display updated balance.

Else → view prints “insufficient balance”.

7.End program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by:GOGINENI BIDHISHA 
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:

```
import java.util.*;

// --- Model ---
class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance = balance;
    }

    public double getBalance() {
        return balance;
    }

    public void deposit(double amount) {
        balance += amount;
    }

    public boolean withdraw(double amount) {
        if (amount <= balance) {
            balance -= amount;
            return true;
        } else {
            return false;
        }
    }
}

// --- View ---
class BankView {
    public void showBalance(double balance) {
        System.out.printf("Current Balance: ₹%.2f%n", balance);
    }

    public void showError(String message) {
        System.out.println(message);
    }
}

// --- Controller ---
class BankController {
    private BankAccount model;
    private BankView view;

    public BankController(BankAccount model, BankView view) {
        this.model = model;
        this.view = view;
    }

    public void deposit(double amount) {
        model.deposit(amount);
        view.showBalance(model.getBalance());
    }

    public void withdraw(double amount) {
        if (model.withdraw(amount)) {
            view.showBalance(model.getBalance());
        } else {
            view.showError("Withdrawal failed: insufficient balance.");
        }
    }
}

// --- Main Application ---
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double initialBalance = Double.parseDouble(sc.nextLine());
        int n = Integer.parseInt(sc.nextLine());

        BankAccount model = new BankAccount(initialBalance);
        BankView view = new BankView();
        BankController controller = new BankController(model, view);

        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().split(" ");
            String action = parts[0];
            double amount = Double.parseDouble(parts[1]);

            if (action.equalsIgnoreCase("deposit")) {
                controller.deposit(amount);
            } else if (action.equalsIgnoreCase("withdraw")) {
                controller.withdraw(amount);
            }
        }

        sc.close();
    }
}

```





## OUTPUT:

<img width="839" height="739" alt="image" src="https://github.com/user-attachments/assets/bf743018-b831-4e72-ac1d-f3015604fdac" />


## RESULT:

The program is being implemented successfully.
