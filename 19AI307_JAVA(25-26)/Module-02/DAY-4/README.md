# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

nput	Result
Ram
20
Student{name='Ram', age=20}

## AIM:
To write a Java program that creates a Student object using a constructor and prints the object details using the toString() method.

## ALGORITHM :
1. Create a Student class with name and age variables.

2. Define a constructor to initialize these variables.

3. Override the toString() method to return student details.

4. In the main method, read name and age from the user.

5. Create a Student object using the constructor.

6. Print the object, which automatically calls toString().


## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Student {
    String name;
    int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name = scanner.nextLine();
        int age = scanner.nextInt();

        Student s = new Student(name, age);
        System.out.println(s);

        scanner.close();
    }
}
```





## OUTPUT:
<img width="780" height="399" alt="image" src="https://github.com/user-attachments/assets/8e203365-47a9-4c2f-8c5f-89e2bbcb5f3b" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
