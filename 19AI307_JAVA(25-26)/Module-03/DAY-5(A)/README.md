# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.
## AIM:
To write a Java program that demonstrates the concept of inner classes in Java and how to create and access an inner class object from the outer class.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class named prog.
4. Inside the outer class, define an inner class InnerClass with a method displayMessage().
5. In the main method, create a Scanner object to read user input.
6. Read a name from the user.
7. Create an object of the outer class.
8. Using the outer object, create an object of the inner class.
9. Call the displayMessage() method of the inner class object.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class prog {

    class InnerClass {
        void displayMessage(String name) {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();

        prog outer = new prog();
        prog.InnerClass inner = outer.new InnerClass();
        inner.displayMessage(name);
    }
}


```
## OUTPUT:

<img width="1216" height="320" alt="image" src="https://github.com/user-attachments/assets/689ecd9a-82b8-482e-a182-efeffac46385" />


## RESULT:
Thus, the Java program was successfully written and executed to demonstrate accessing an inner class from the outer class.
