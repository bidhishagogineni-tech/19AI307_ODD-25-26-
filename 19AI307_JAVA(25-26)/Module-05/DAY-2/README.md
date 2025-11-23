# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
<img width="824" height="213" alt="image" src="https://github.com/user-attachments/assets/9ab976ed-9219-42d0-8196-0b1dd36a99d8" />


## AIM:
To write a Java program demonstrating inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes user input and another thread reads and prints the received data.

## ALGORITHM :
1.	Start the program.

2.Create PipedInputStream and PipedOutputStream and connect them.

3.Start a WriterThread that reads input from the user and writes it to the pipe.

4.Start a ReaderThread that reads data from the pipe.

5.Reader thread prints the received message.

6.End program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:212223040048  
*/
```

## SOURCE CODE:
```
import java.io.PipedInputStream;
import java.io.PipedOutputStream;
import java.io.IOException;
import java.util.Scanner;

class WriterThread extends Thread {
    private PipedOutputStream pos;
    private String data;

    public WriterThread(PipedOutputStream pos, String data) {
        this.pos = pos;
        this.data = data;
    }

    public void run() {
        try {
            // Write data bytes into the pipe
            pos.write(data.getBytes());
            pos.close(); // close to signal end of data
        } catch (IOException e) {
            System.out.println("WriterThread error: " + e.getMessage());
        }
    }
}

class ReaderThread extends Thread {
    private PipedInputStream pis;

    public ReaderThread(PipedInputStream pis) {
        this.pis = pis;
    }

    public void run() {
        try {
            int ch;
            StringBuilder sb = new StringBuilder();
            while ((ch = pis.read()) != -1) {
                sb.append((char) ch);
            }
            System.out.println("ReaderThread received: " + sb.toString());
            pis.close();
        } catch (IOException e) {
            System.out.println("ReaderThread error: " + e.getMessage());
        }
    }
}

public class InterThreadCommunication {
    public static void main(String[] args) {
        try (Scanner sc = new Scanner(System.in)) {
            // Read input from user
            String input = sc.nextLine();

            // Create piped streams
            PipedOutputStream pos = new PipedOutputStream();
            PipedInputStream pis = new PipedInputStream(pos); // connect streams

            // Create and start threads
            WriterThread writer = new WriterThread(pos, input);
            ReaderThread reader = new ReaderThread(pis);

            reader.start();
            writer.start();

            // Wait for threads to finish
            writer.join();
            reader.join();

        } catch (IOException | InterruptedException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}

```






## OUTPUT:

<img width="844" height="268" alt="image" src="https://github.com/user-attachments/assets/d0665e88-3b50-4582-a687-4be04ae71c27" />


## RESULT:

The program is being implemented successfully.
