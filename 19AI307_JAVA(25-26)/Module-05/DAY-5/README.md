
# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

For example:

Input	Result
5
10
a = 10
b = 5


## AIM:
To write a Java program that demonstrates the use of synchronization by swapping two numbers inside a synchronized block.

## ALGORITHM :
1. Create a Scanner to read two integers from the user.

2. Store the integers in variables a and b.

3. Create an object lock to use for synchronization.

4. Use a synchronized block on the lock object to swap the values of a and b.

5. Print the swapped values of a and b.



## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class SwapSync {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = Integer.parseInt(sc.nextLine());
        int b = Integer.parseInt(sc.nextLine());
        Object lock = new Object();
        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}

```





## OUTPUT:
<img width="471" height="368" alt="image" src="https://github.com/user-attachments/assets/150a0451-f8d0-4b80-8b09-44a473d21b56" />



## RESULT:

The program has been executed successfully and the desired output has been obtained.
