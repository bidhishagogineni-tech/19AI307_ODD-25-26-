# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

Each user has their own preference:

Some are looking for "Gamers"

Some prefer "Pet Lovers"

Others vibe with "Bookworms"

Or maybe they're into "Gym Freaks", etc.

When a new user signs up, the app should only notify users whose preferences match that new person’s type.

Users subscribe to MatchIt’s notification service based on their “match interest”. The system notifies them only when someone with their preferred type signs up.

What Students Must Do:
Implement the Observer Pattern

MatchItServer = Subject

User = Observer

When a new person joins, notify only users who match the preference

Each user prints a custom message when their preferred type joins.

Input Format:
First line: Number of users n

Next n lines: UserName Preference
(e.g., Alice Gamer)

Next line: Number of sign-ups m

Next m lines: NewUserName Type
(e.g., Jack Gamer)

Output Format:
For each signup:

New User Joined: [NewUserName] - Type: [Type]
[UserName]: Omg! A new [Type]? MatchIt, you know me too well! 
...
Only matching users get notified.

## AIM:
To design and implement a Java program using the Observer Design Pattern where users (Observers) subscribe to a MatchItServer (Subject) based on their match preferences. The system should notify only those users whose preference matches the type of a newly joined user, and each observer should display a personalized message when notified.

## ALGORITHM :
1.Read number of existing users n.

2.For each user:

Read userName and preference.

Register the user as an observer with the server.

3.Read number of new sign-ups m.

4.For each new signup:

Read newUserName and type.

Print “New User Joined” message.

Server notifies only observers whose preference matches type.

Each matching user prints their custom notification message.

5.End program.
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:

```
import java.util.*;

// Observer interface
interface Observer {
    void notify(String newUser, String type);
    String getPreference();
}

// Concrete Observer - User
class User implements Observer {
    private String name;
    private String preference;

    public User(String name, String preference) {
        this.name = name;
        this.preference = preference;
    }

    @Override
    public void notify(String newUser, String type) {
        System.out.println(name + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + newUser + "!)");
    }

    @Override
    public String getPreference() {
        return preference;
    }
}

// Subject interface
interface Subject {
    void registerObserver(User user);
    void newSignup(String name, String type);
}

// Concrete Subject - MatchIt Server
class MatchItServer implements Subject {
    private List<User> users = new ArrayList<>();

    @Override
    public void registerObserver(User user) {
        users.add(user);
    }

    @Override
    public void newSignup(String name, String type) {
        System.out.println("New User Joined: " + name + " - Type: " + type);
        for (User user : users) {
            if (user.getPreference().equalsIgnoreCase(type) || 
                user.getPreference().replaceAll("\\s+", "").equalsIgnoreCase(type)) {
                user.notify(name, type);
            }
        }
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().split(" ");
            String name = parts[0];
            String preference = parts[1];
            server.registerObserver(new User(name, preference));
        }

        int m = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < m; i++) {
            String[] parts = sc.nextLine().split(" ");
            String newUser = parts[0];
            String type = parts[1];
            server.newSignup(newUser, type);
        }

        sc.close();
    }
}

```





## OUTPUT:

<img width="920" height="466" alt="image" src="https://github.com/user-attachments/assets/3601671f-ffca-424a-8fb1-2c6452766edb" />


## RESULT:
The program is being implemented successfully.
