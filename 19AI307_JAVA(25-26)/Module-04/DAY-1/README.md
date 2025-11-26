# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that reads integers continuously and handles null or zero values appropriately.

## ALGORITHM :
1. Create a Scanner object to read input from the user.
2. Use a loop to read each line until no more input exists.
3. Read the input string and trim extra spaces.
4. Check if the input string is equal to "null".
5. If so, print "Null Integer".
6. Otherwise, convert the string to an integer.
7. Check if the integer is zero and print "Null Integer" if true.
8. Otherwise, print the integer value.


## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Vikash.A.R
RegisterNumber: 212222040179
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();

            if (input.equals("null")) {
                System.out.println("Null Integer");
            } else {
                Integer num = Integer.parseInt(input);

                if (num == 0) {
                    System.out.println("Null Integer");
                } else {
                    System.out.println(num.toString());
                }
            }
        }
    }
}
```

## OUTPUT:

<img width="917" height="423" alt="image" src="https://github.com/user-attachments/assets/e0b354b4-17b4-4200-b407-caa3fae9e716" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.

