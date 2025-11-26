# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

import java.util.Scanner;

class Employee {
    String name;

    void setName(String name) {
        // assign name using this
    }

    Employee display() {
        // return the current object using this
    }

    void printName() {
        // Print name
    }
}

class prog {
   // Main function
}

 

 

For example:

Input	Result
Sakthi
Employee Name: Sakthi


## AIM:
To write a Java program that sets an employee’s name using a method, returns the current object using this, and prints the name using method chaining.

## ALGORITHM :
1.Create an Employee class with a name variable.

2.Define setName() to assign the name.

3.Define display() to return the current object (this).

4.Define printName() to print the employee name.

5.In the main method, read the name from the user.

6.Create an Employee object and set the name.

7.Call display().printName() to print the name using method chaining.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Employee 
{
    String name;

    void setName(String name) 
    {
        this.name = name;
    }

    Employee display() 
    {
        return this;
    }

    void printName() 
    {
        System.out.println("Employee Name: " + name);
    }
}

class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String empName = sc.nextLine();
        Employee emp = new Employee();
        emp.setName(empName);
        emp.display().printName();
    }
}
```






## OUTPUT:
<img width="695" height="335" alt="image" src="https://github.com/user-attachments/assets/7236cf3c-95b0-426d-b03c-16da34e7c794" />



## RESULT:

The program has been executed successfully and the desired output has been obtained.
