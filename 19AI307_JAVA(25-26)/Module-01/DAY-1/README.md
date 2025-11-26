# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is entering a battle arena tournament, but only heroes who meet specific power and skill criteria are allowed inside.

To enter the arena, a hero (Lovely) must satisfy any one of these conditions:

Her power level is above 80 and her rank is above 5
→ (power > 80 && rank > 5)

Or she has a magic orb and her experience is at least 3 years
→ (hasMagicOrb == true && experience >= 3)

Note: If either of the above conditions is satisfied, she is allowed to enter. Otherwise, she is rejected.

Input Format:
First line: int power

Second line: int rank

Third line: boolean hasMagicOrb

Fourth line: int experience

Output Format:

Can Enter Arena: true/false

For example:

Input	Result
85
6
false
1
Can Enter Arena: true
82
5
true
2
Can Enter Arena: false

## AIM:
To write a Java program that demonstrates type conversion between different primitive data types, including widening and narrowing conversions, and to display the results of each conversion.

## ALGORITHM :
1. Start the program and create a Scanner object to read inputs from the user.

2. Read an integer, a double, a float, and a byte value from the user.

3. Convert the integer to a double (widening conversion) and store the result.

4. Convert the double to an integer (narrowing conversion) and store the result.

5. Convert the float to an integer (narrowing conversion) and store the result.

6. Convert the byte to a float (widening conversion) and store the result.

7. Display all the converted results to the user.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## Sourcecode.java:

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int power = sc.nextInt();
        int rank = sc.nextInt();
        boolean hasMagicOrb = sc.nextBoolean();
        int experience = sc.nextInt();
        
        boolean canEnter = (power > 80 && rank > 5) || (hasMagicOrb && experience >= 3);
        
        System.out.println("Can Enter Arena: " + canEnter);
    }
}

```





## OUTPUT:

<img width="732" height="651" alt="image" src="https://github.com/user-attachments/assets/e10f3ec6-bdd9-4570-9020-a6d8c5ea2383" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.
