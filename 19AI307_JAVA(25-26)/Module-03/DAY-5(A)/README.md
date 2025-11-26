# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

Input	Result
Manoj
Hello, Manoj! This message is from the Inner Class.


## AIM:
To write a Java program that demonstrates the use of inner classes by creating an OuterClass containing an InnerClass, and displaying a message using a method defined inside the inner class.

## ALGORITHM :
1. Define a class OuterClass containing a non-static inner class InnerClass.

2. Inside InnerClass, define a method displayMessage(String name) that prints a greeting message using the provided name.

3. In the main method, create a Scanner object to read a string input from the user.

4. Read the user’s name and store it in a variable.

5. Create an object of OuterClass.

6. Using the outer class object, create an object of the inner class (OuterClass.InnerClass).

7. Call the displayMessage() method using the inner class object and pass the user’s name.

8. Close the Scanner object.

9. End the program.


## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class OuterClass {
    class InnerClass {
        void displayMessage(String name) {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        OuterClass outer = new OuterClass();
        OuterClass.InnerClass inner = outer.new InnerClass();
        inner.displayMessage(name);
        sc.close();
    }
}

```





## OUTPUT:
<img width="1066" height="338" alt="image" src="https://github.com/user-attachments/assets/23116dcf-ddef-4532-94ff-f1f5d430550a" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
