# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
<img width="831" height="410" alt="image" src="https://github.com/user-attachments/assets/047650e9-d15c-4e96-863d-1b2f387d6efb" />


## AIM:
To write a Java program that reads a thread name and a priority (1–10) from the user, creates a thread with the given name, sets its priority, and displays the assigned thread details.

## ALGORITHM :
1.	Start the program.

2.Read thread name from the user.

3.Read priority value from the user.

4.Create a new thread with the given name.

5.Set the thread's priority using setPriority().

6.Print the thread name and priority.

7.End the program.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by:GOGINENI BIDHISHA 
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:

```
import java.util.*;

public class ThreadPriorityExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread(threadName);

        t.setPriority(priority);

        System.out.println("Thread " + threadName + " priority is " + priority);
    }
}


```





## OUTPUT:

<img width="758" height="312" alt="image" src="https://github.com/user-attachments/assets/f9f39f72-9686-4829-ab2d-f9dc816d0df3" />


## RESULT:
The program is being implemented successfully.
