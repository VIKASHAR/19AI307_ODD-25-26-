# Ex.No:3(D)    INTERFACE 

## QUESTION:
Schools use different grading schemes. You need to build a system to plug different strategies.

SimpleGrader: A: 90+, B: 75–89, C: 60–74, F: below 60

StrictGrader: A: 95+, B: 85–94, C: 70–84, F: below 70

Input Format:
marks
graderType
marks: Integer (0–100)

graderType: 1 for SimpleGrader, 2 for StrictGrader

Output Format:
A / B / C / F

For example:

Input	Result
92 1
A


## AIM:
To write a Java program that demonstrates abstraction and polymorphism by using an abstract class Grader and two different grading systems (SimpleGrader and StrictGrader) to evaluate marks based on user input.

## ALGORITHM :
1. Create an abstract class Grader with an abstract method grade(int marks) that returns a grade as a string.

2. Define a subclass SimpleGrader that implements the grade() method with a standard grading scale (A, B, C, F).

3. Define another subclass StrictGrader that implements the grade() method with a stricter grading scale.

4. In the main method, create a Scanner object to take input from the user.

5. Read the marks and grader type from the user (1 for SimpleGrader, otherwise StrictGrader).

6. Based on the grader type, create an instance of the appropriate subclass and assign it to a Grader reference.

7. Call the grade() method using the selected grader object and print the resulting grade.

8. End the program.



## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

abstract class Grader {
    abstract String grade(int marks);
}

class SimpleGrader extends Grader {
    String grade(int marks) {
        if (marks >= 90) return "A";
        else if (marks >= 75) return "B";
        else if (marks >= 60) return "C";
        else return "F";
    }
}

class StrictGrader extends Grader {
    String grade(int marks) {
        if (marks >= 95) return "A";
        else if (marks >= 85) return "B";
        else if (marks >= 70) return "C";
        else return "F";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        int graderType = sc.nextInt();
        Grader grader = (graderType == 1) ? new SimpleGrader() : new StrictGrader();
        System.out.println(grader.grade(marks));
    }
}

```



## OUTPUT:
<img width="328" height="237" alt="image" src="https://github.com/user-attachments/assets/275eaf1b-b027-4546-91b2-9dbe68f2a079" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.

