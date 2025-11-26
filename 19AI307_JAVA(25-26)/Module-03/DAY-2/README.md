# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

For example:

Input	Result
Dog
Dog barks

## AIM:
To write a Java program using inheritance and method overriding where different animals (Dog, Cat, Cow) produce different sounds based on user input.

## ALGORITHM :
1.Create a base class Animal with a method sound().

2.Create derived classes Dog, Cat, and Cow that extend Animal.

3.Override the sound() method in each derived class to print the specific animal sound.

4.Read the animal name from the user.

5.Based on the input, create the corresponding animal object.

6.Call the sound() method to display the animal sound.

7.If the input does not match any known animal, print "Unknown animal".



## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Animal {
    public void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    public void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    public void sound() {
        System.out.println("Cow moos");
    }
}

public class AnimalSound {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Animal a;

        String input = scanner.nextLine().trim().toLowerCase();

        switch (input) {
            case "dog":
                a = new Dog();
                break;
            case "cat":
                a = new Cat();
                break;
            case "cow":
                a = new Cow();
                break;
            default:
                System.out.println("Unknown animal");
                scanner.close();
                return;
        }

        a.sound();
        scanner.close();
    }
}

```





## OUTPUT:
<img width="474" height="369" alt="image" src="https://github.com/user-attachments/assets/5c9ccb4b-5b55-4df9-a6b5-f25a9e5117aa" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
