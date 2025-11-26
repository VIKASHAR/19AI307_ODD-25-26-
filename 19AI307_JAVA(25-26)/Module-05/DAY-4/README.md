
# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.

Note : Read the threadname from the User

Set the Priority as 2.

For example:

Input	Result
NewThread
Priority of Thread: 2
Name of Thread: NewThread
Thread[NewThread,2,main]


## AIM:
To write a Java program that demonstrates setting the name and priority of a thread and displaying its details.

## ALGORITHM :
1. Create a Scanner to read the thread name from the user.

2. Get the reference to the current thread using Thread.currentThread().

3. Set the thread’s name using setName().

4. Set the thread’s priority using setPriority().

5. Print the thread’s priority and name.

6. Print the thread object to display its details.



## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:


```
import java.util.Scanner;
public class ThreadSetNamePriority {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(name);
        t.setPriority(2);
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}

```




## OUTPUT:

<img width="734" height="264" alt="image" src="https://github.com/user-attachments/assets/f124394d-aba1-43ed-9c70-07d4ccee01f0" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
