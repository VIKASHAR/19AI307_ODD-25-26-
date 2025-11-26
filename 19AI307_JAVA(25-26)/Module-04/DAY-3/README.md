# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A student can enroll in multiple courses. The relationship is many-to-many via association.
If No Courses were assigned, print "No courses enrolled." 

For example:

Input	Result
Hariharan
2
React
Express
Hariharan's enrolled courses:
- React
- Express

## AIM:
To write a Java program that demonstrates Object-Oriented Programming (OOP) concepts by creating Student and Course classes, allowing a student to enroll in multiple courses and display the enrolled courses.

## ALGORITHM :
1. Read student name.

2. Create Student object.

3. Read number of courses.

4. For each course, read name and enroll.

5. Display enrolled courses.




## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:
```
import java.util.*;

class Course {
    String name;
    Course(String name) {
        this.name = name;
    }
}

class Student {
    String name;
    List<Course> courses = new ArrayList<>();

    Student(String name) {
        this.name = name;
    }

    void enroll(Course course) {
        courses.add(course);
    }

    void showEnrolledCourses() {
        System.out.println(name + "'s enrolled courses:");
        if (courses.isEmpty()) {
            System.out.println("No courses enrolled.");
        } else {
            for (Course c : courses)
                System.out.println("- " + c.name);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String studentName = sc.nextLine();
        Student s = new Student(studentName);
        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String courseName = sc.nextLine();
            s.enroll(new Course(courseName));
        }
        s.showEnrolledCourses();
        sc.close();
    }
}

```






## OUTPUT:

<img width="751" height="353" alt="image" src="https://github.com/user-attachments/assets/acbdbc4b-5151-4d8a-a08e-0e0781f2f7d2" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
