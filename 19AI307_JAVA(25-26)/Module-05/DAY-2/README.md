# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.

Input	Result
welcome java
ReaderThread received: welcome java

## AIM:
To write a Java program that demonstrates inter-thread communication using PipedInputStream and PipedOutputStream.

## ALGORITHM :
1. Create a PipedInputStream and connect it to a PipedOutputStream.

2. Create a writer thread that reads a line from the user and writes it to the piped output stream.

3. Create a reader thread that reads data from the piped input stream and displays it.

4. Start both the writer and reader threads.

5. Close the streams after reading and writing.



## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;
public class PipedCommDemo {
    public static void main(String[] args) throws Exception {
        PipedInputStream pin = new PipedInputStream();
        PipedOutputStream pout = new PipedOutputStream(pin);
        Thread writer = new Thread(() -> {
            try {
                Scanner sc = new Scanner(System.in);
                String msg = sc.nextLine();
                pout.write(msg.getBytes());
                pout.close();
            } catch (Exception e) {}
        });
        Thread reader = new Thread(() -> {
            try {
                byte[] buffer = new byte[1024];
                int len = pin.read(buffer);
                String received = new String(buffer, 0, len);
                System.out.println("ReaderThread received: " + received);
                pin.close();
            } catch (Exception e) {}
        });
        writer.start();
        reader.start();
    }
}

```





## OUTPUT:

<img width="1191" height="199" alt="image" src="https://github.com/user-attachments/assets/534879d8-affe-46b9-ade9-e6b2def5133f" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
