# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
<img width="887" height="297" alt="image" src="https://github.com/user-attachments/assets/0f596e31-00b8-4414-bc49-6d8f68537477" />


## AIM:

To write a Java program that sets the name and priority of two threads (t1 and t2).
The thread names are taken from the user, and their priorities are set to 4 and 2 respectively, then displayed.
## ALGORITHM :
1.	Start the program.

2.Read two thread names from the user.

3.Create two Thread objects t1 and t2.

4.Set name of t1 and t2 using user input.

5.Set priority of t1 = 4 and t2 = 2.

6.Print the thread details.

7.End program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:

```
import java.util.*;

public class ThreadPriorityExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        Thread t1 = new Thread();
        Thread t2 = new Thread();

        t1.setName(name1);
        t2.setName(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);
    }
}

```





## OUTPUT:

<img width="809" height="245" alt="image" src="https://github.com/user-attachments/assets/fb47661a-a49e-4f71-956b-2a6dffb438e6" />


## RESULT:

The program is being implemented successfully.
