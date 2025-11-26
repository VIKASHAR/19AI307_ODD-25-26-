# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

import java.util.Scanner;
class City {

    String cityName;
    long population;
    double area;

    void printDetails() {
           // Your Code Here
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
         // Your Code Here
         scanner.close();
    }
}

For example:

Input	Result
New York
8419000
783.8
City Name: New York
Population: 8419000
Area: 783.8
London
8982000
1572
City Name: London
Population: 8982000
Area: 1572.0

## AIM:
To write a Java program that reads city details (name, population, area) from the user and displays them using a class.

## ALGORITHM :
1. Create a class City with variables for city name, population, and area.

2. Read the city name, population, and area from the user.

3. Store the values in a City object.

4. Call the method to print the city details.

5. End the program.




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class City {
    String cityName;
    long population;
    double area;

    void printDetails() {
        System.out.println("City Name: " + cityName);
        System.out.println("Population: " + population);
        System.out.println("Area: " + area);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        City obj = new City();
        obj.cityName = scanner.nextLine();
        obj.population = scanner.nextLong();
        obj.area = scanner.nextDouble();
        obj.printDetails();
        scanner.close();
    }
}

```





## OUTPUT:

<img width="662" height="487" alt="image" src="https://github.com/user-attachments/assets/59b07f11-a74f-4e3c-86f8-d28e99c4d0d2" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
