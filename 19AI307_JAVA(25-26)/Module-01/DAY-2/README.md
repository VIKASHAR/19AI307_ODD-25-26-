# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Given a month number (1 to 12), print which quarter of the year it belongs to:

Months 1,2,3 → "First Quarter"

Months 4,5,6 → "Second Quarter"

Months 7,8,9 → "Third Quarter"

Months 10,11,12 → "Fourth Quarter"
If the number is not in 1-12, print "Invalid Month".

Write a java program to get the month from user and and display appropriate output for the given input.

For example:

Input	Result
2
First Quarter

## AIM:
To write a Java program that reads a month number from the user and determines which quarter of the year it belongs to, displaying the appropriate quarter or an error message for invalid input.

## ALGORITHM :
1. Start the program and create a Scanner object to read user input.

2. Read an integer value representing the month number.

3. If the month is between 1 and 3, display "First Quarter".

4. Else if the month is between 4 and 6, display "Second Quarter".

5. Else if the month is between 7 and 9, display "Third Quarter".

6. Else if the month is between 10 and 12, display "Fourth Quarter".

7. If none of the conditions match, display "Invalid Month".




## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int month = sc.nextInt();
        if(month >= 1 && month <= 3)
            System.out.println("First Quarter");
        else if(month >= 4 && month <= 6)
            System.out.println("Second Quarter");
        else if(month >= 7 && month <= 9)
            System.out.println("Third Quarter");
        else if(month >= 10 && month <= 12)
            System.out.println("Fourth Quarter");
        else
            System.out.println("Invalid Month");
    }
}
```


## OUTPUT:

<img width="453" height="237" alt="image" src="https://github.com/user-attachments/assets/c9cba8f6-1afe-4522-98ab-0549002974f4" />



## RESULT:

The program has been executed successfully and the desired output has been obtained.
