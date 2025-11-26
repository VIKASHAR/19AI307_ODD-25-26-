
# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to write multiple lines to a file using FileWriter.

For example:

Input	Result
Hello world
Welcome to Java
exit
File written successfully to multilines.txt


## AIM:

To write a Java program that reads multiple lines from the user and writes them to a file using FileWriter.
## ALGORITHM :
1. Create a Scanner to read input from the user.

2. Create a FileWriter object for the file multilines.txt.

3. Use a loop to read each line from the user.

4. If the line is "exit", break the loop.

5. Otherwise, write the line to the file followed by a newline.

6. Close the FileWriter.

7. Print a message indicating the file has been written successfully.




## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:


```
import java.io.FileWriter;
import java.util.Scanner;
public class MultiLineWrite {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        try {
            FileWriter writer = new FileWriter("multilines.txt");
            while (true) {
                String line = sc.nextLine();
                if (line.equalsIgnoreCase("exit")) break;
                writer.write(line + System.lineSeparator());
            }
            writer.close();
            System.out.println("File written successfully to multilines.txt");
        } catch (Exception e) {
            System.out.println("An error occurred.");
        }
    }
}

```




## OUTPUT:
<img width="1037" height="270" alt="image" src="https://github.com/user-attachments/assets/afd22f9f-8065-4feb-bb06-45b744009bd5" />



## RESULT:

The program has been executed successfully and the desired output has been obtained.
