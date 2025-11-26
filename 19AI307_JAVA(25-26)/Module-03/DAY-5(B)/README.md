# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.

Input	Result
car
CAR has 4 wheels.


## AIM:
To create a Java program that uses an enum to represent different vehicle types and prints the number of wheels based on user input.

## ALGORITHM :
1.Start the program.

2.Define an enum VehicleType with vehicle names and wheel counts.

3.Read the vehicle type from the user.

4.Convert the user input to uppercase.

5.Use valueOf() to get the matching enum constant.

6.If matching, print the vehicle name and number of wheels.

7.If no match, print an invalid vehicle type message.

8.End the program.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

enum VehicleType {
    CAR(4),
    BIKE(2),
    BUS(6);

    private int wheels;

    VehicleType(int wheels) {
        this.wheels = wheels;
    }

    public int getWheels() {
        return wheels;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().trim().toUpperCase();

        try {
            VehicleType vehicle = VehicleType.valueOf(input);
            System.out.println(vehicle + " has " + vehicle.getWheels() + " wheels.");
        } catch (Exception e) {
            System.out.println("Invalid vehicle type entered.");
        }
    }
}

```

## OUTPUT:

<img width="707" height="344" alt="image" src="https://github.com/user-attachments/assets/00056ee2-1af5-4df7-8254-b881129ba8a3" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.
