# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Counter with a static integer variable count. Every time an object is created, increase count by 1. Print the total count using a static method

## AIM:
To create a Java class Counter that uses a static variable to count how many objects are created and display the total count using a static method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a class named Counter with a static integer variable count initialized to 0.
4. Define a constructor in the Counter class that increments the count variable every time an object is created.
5. Create a static method printCount() that prints the value of the count variable.
6. In the main method, create multiple Counter objects inside a loop.
7. Each time an object is created, the constructor increases count by 1.
8. After the loop ends, call the static method printCount() to display the total number of objects created.
9. End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.*;
class Counter
{
    static int count=0;
    
    Counter()
    {
        count++;
    }
    
    static void printCount()
    {
        System.out.println("Total objects created: "+count);
    }
}
class prog
{
    public static void main(String args[])
    {
        for(int i=0; i<7; i++)
        {
            new Counter();
        }
        Counter.printCount();
    }
}
```
## OUTPUT:

<img width="594" height="233" alt="image" src="https://github.com/user-attachments/assets/e6e10952-2191-4526-be90-21cc81a4ebcc" />


## RESULT:
Thus, the Java program using a static variable and static method was successfully written and executed to count and display the total number of objects created.
