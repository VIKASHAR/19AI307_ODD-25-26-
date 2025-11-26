
# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to write an array of strings into a file using PrintWriter.

Input	Result
welcome
Array of strings written to file successfully.

## AIM:
To write a Java program that reads a line of text, splits it into words, and writes each word to a file using BufferedReader and PrintWriter.

## ALGORITHM :
1. Create a BufferedReader to read a line of text from the user.

2. Read the input line and split it into an array of words.

3. Create a PrintWriter to write to a file named output.txt.

4. Loop through the array and write each word to the file on a separate line.

5. Close the PrintWriter.

6. Print a success message.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.io.*;
public class Main {
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String line = br.readLine();
        String[] arr = line.split(" ");
        PrintWriter pw = new PrintWriter("output.txt");
        for (String s : arr) pw.println(s);
        pw.close();
        System.out.println("Array of strings written to file successfully.");
    }
}

```





## OUTPUT:

<img width="1020" height="310" alt="image" src="https://github.com/user-attachments/assets/b5e78b23-1778-4da2-af7b-e8d7eb9bf84c" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
