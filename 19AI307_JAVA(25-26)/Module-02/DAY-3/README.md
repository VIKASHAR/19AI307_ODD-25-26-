# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

import java.util.Scanner;

 class Rectangle {
    // Private instance variables
    private double length;
    private double width;

    // Getter and Setter for length
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }

    // Getter and Setter for width
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }

    // Method to calculate area
    public double calculateArea() {
        return length * width;
    }
}

## AIM:
To write a Java program that uses getter and setter methods to store and display the length and width of a rectangle.

## ALGORITHM :
1. Create a Rectangle class with private variables length and width.

2. Provide setter methods to assign values and getter methods to retrieve them.

3. In the main method, read length and width from the user.

4. Store the values using setters.

5. Display the values using getters.

6. End the program.



## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Rectangle 
{
    private double length;
    private double width;

    public double getLength() 
    {
        return length;
    }
    public void setLength(double length) 
    {
        this.length = length;
    }

    public double getWidth() 
    {
        return width;
    }
    public void setWidth(double width) 
    {
        this.width = width;
    }

    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        Rectangle rect = new Rectangle();
        rect.setLength(sc.nextDouble());
        rect.setWidth(sc.nextDouble());
        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());
    }
}

```

## OUTPUT:

<img width="613" height="470" alt="image" src="https://github.com/user-attachments/assets/81156256-68dd-461c-8c7d-a3ad5c0ba582" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
