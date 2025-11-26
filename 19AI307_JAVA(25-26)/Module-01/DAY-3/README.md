# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
The digital root of a number is the result obtained by repeatedly summing the digits of the number until a single-digit number is obtained. For example:

Step-by-step for 9875:

9 + 8 + 7 + 5 = 29

2 + 9 = 11

1 + 1 = 2

So, the digital root of 9875 is 2.

Write a Java program that:

Prompts the user to enter a non-negative integer.

Repeatedly calculates the sum of the digits of the number until a single-digit number is obtained.

Displays each step of the calculation clearly, and finally outputs the digital root.

For example:

Input	Result
9875 
Single digit sum: 2


## AIM:
To write a Java program that reduces a number to a single digit by repeatedly summing its digits.

## ALGORITHM :

1. Read the number from the user.

2. Repeat summing the digits while the number has more than one digit.

3. Update the number with the sum obtained.

4. Print the final single-digit result.

5 .End the program.




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        long number = sc.nextLong();

        while (number >= 10) { // repeat until number is a single digit
            long sum = 0;
            long temp = number;

            while (temp > 0) {
                long digit = temp % 10;
                sum += digit;
                temp /= 10;
            }
            number = sum;
        }

        System.out.println("Single digit sum: " + number);
        sc.close();
    }
}

```



## OUTPUT:

<img width="640" height="345" alt="image" src="https://github.com/user-attachments/assets/2c0973d1-0344-436a-9872-60eb72e2fce4" />



## RESULT:

The program has been executed successfully and the desired output has been obtained.
