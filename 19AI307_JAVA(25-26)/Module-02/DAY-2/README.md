# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

For example:

Input	Result
5
125

## AIM:
To write a Java program that demonstrates the use of methods by defining functions to calculate the square and cube of a number, and then displaying the cube of a user-entered value.

## ALGORITHM :
1. Define a class containing a method square(int x) that returns the square of a number.

2. Define another method cube(int x) that returns the cube of a number by multiplying the number with its square.

3. In the main method, create a Scanner object to read an integer input from the user.

4. Read the integer and store it in a variable.

5. Create an object of the class prog.

6. Call the cube() method using the object and pass the input number.

7. Print the cube returned by the method.




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    int square(int x) {
        return x * x;
    }

    int cube(int x) {
        return x * square(x);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        prog p = new prog();
        System.out.println(p.cube(num));
    }
}
```






## OUTPUT:

<img width="418" height="239" alt="image" src="https://github.com/user-attachments/assets/bd7d412b-0faf-4eae-99ac-729a55a35acb" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
