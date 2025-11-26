# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are building customizable robots using the Prototype Pattern. Clone an existing robot template and change its name and feature.

For example:

Input	Result
RoboAlpha  
Voice Recognition
Original Robot: RoboAlpha   - Voice Recognition
Cloned Robot: RoboAlpha   - Voice Recognition


## AIM:
To write a Java program that demonstrates the use of the Prototype Design Pattern by cloning a Robot object and displaying both original and cloned objects.

## ALGORITHM :
1.Start the program and create a class Robot with attributes name and feature.

2.Implement a clone() method to create a copy of the Robot object.

3.Create a display() method to print robot details with a tag.

4.Read robot name and feature from the user.

5.Create a prototype Robot object using the input values.

6.Clone the prototype to create a new Robot object.

7.Display details of both the original and cloned Robot objects.

8.End the program.



## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Robot implements Cloneable {
    String name, feature;

    Robot(String name, String feature) {
        this.name = name;
        this.feature = feature;
    }

    public Robot clone() {
        return new Robot(name, feature);
    }

    void display(String tag) {
        System.out.println(tag + ": " + name + " - " + feature);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        String feature = sc.nextLine();

        Robot prototype = new Robot(name, feature);
        Robot cloned = prototype.clone();

        prototype.display("Original Robot");
        cloned.display("Cloned Robot");
    }
}

```





## OUTPUT:

<img width="1120" height="394" alt="image" src="https://github.com/user-attachments/assets/50bb9aa5-e1d2-48b9-b2b0-496c5016eeab" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
