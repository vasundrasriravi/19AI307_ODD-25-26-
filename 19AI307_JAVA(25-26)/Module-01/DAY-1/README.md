# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely wants to learn how Java print statements work. Write a Java program that:

Takes her name, age, and favorite decimal number

Prints greeting using print()

Prints age using println()

Prints favorite number using printf() with 2 decimal places

## AIM:
To write a Java program that demonstrates the use of variables, data types, operators, and different print statements (print, println, and printf).

## ALGORITHM :
1.	Start the program.
2. Create a Scanner object to read input.
3. Read the name (String), age (int), and favorite number (float).
4. Display greeting using System.out.print().
5. Display age using System.out.println().
6. Display favorite number using System.out.printf() formatted to two decimals.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## Sourcecode.java:
```
import java.util.*;
public class Main
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        int age = sc.nextInt();
        double num = sc.nextDouble();
        System.out.println("Hello, "+name);
        System.out.println("You are "+age+" years old");
        System.out.printf("Your favorite number is %.2f",num);
    }
}
```
## OUTPUT:
<img width="700" height="300" alt="image" src="https://github.com/user-attachments/assets/cd79b650-a46b-4221-ab6f-d24541f47da1" />

## RESULT:
Thus, the Java program was successfully written and executed to demonstrate the different printing methods in Java.

