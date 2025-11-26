# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to concatenate two strings.

Input	Result
hello
world
Concatenated string: helloworld


## AIM:
To write a Java program that reads two strings from the user and concatenates them into one string.

## ALGORITHM :
1. Read the first string from the user.

2. Read the second string from the user.

3. Concatenate both strings using the + operator.

4. Display the concatenated result.

5. End the program.




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class StringConcatenation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String str1 = sc.nextLine();
        String str2 = sc.nextLine();

        String result = str1 + str2;

        System.out.println("Concatenated string: " + result);
        sc.close();
    }
}

```





## OUTPUT:

<img width="848" height="409" alt="image" src="https://github.com/user-attachments/assets/d9e23095-0132-4354-ac77-f087986de569" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
