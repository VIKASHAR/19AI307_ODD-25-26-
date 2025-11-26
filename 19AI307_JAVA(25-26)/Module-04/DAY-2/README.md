# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:

[FlightName] registered with Radar Control Tower. Total Flights: [count]

For example:

Input	Result
3
AI101
BA202
EK303
AI101 registered with Radar Control Tower. Total Flights: 1
BA202 registered with Radar Control Tower. Total Flights: 2
EK303 registered with Radar Control Tower. Total Flights: 3


## AIM:
To write a Java program that demonstrates the Singleton design pattern by ensuring only one RadarControlTower object is created and used to register multiple flights.

## ALGORITHM :
1. Create a class RadarControlTower with a private static instance variable.

2. Make the constructor private to prevent multiple object creation.

3. Define a static method getInstance() to return the single shared instance.

4. Add a method registerFlight() to count and display registered flights.

5. In main(), read the number of flights using Scanner.

6. Get the single instance of RadarControlTower.

7. Loop for each flight name and call registerFlight().

8. Close the Scanner.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.*;
class RadarControlTower {
    private static RadarControlTower instance;
    private int count = 0;
    private RadarControlTower() {}
    public static RadarControlTower getInstance() {
        if (instance == null)
            instance = new RadarControlTower();
        return instance;
    }
    public void registerFlight(String flightName) {
        count++;
        System.out.println(flightName + " registered with Radar Control Tower. Total Flights: " + count);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        RadarControlTower tower = RadarControlTower.getInstance();
        for (int i = 0; i < n; i++) {
            String flightName = sc.nextLine();
            tower.registerFlight(flightName);
        }
        sc.close();
    }
}

```





## OUTPUT:

<img width="1190" height="230" alt="image" src="https://github.com/user-attachments/assets/687c5e39-2453-4165-8082-28a5525a5a71" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
