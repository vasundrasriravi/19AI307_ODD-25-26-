# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program demonstrating method creation and method calling, where one method internally calls another to perform a calculation.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a method square(int x) that returns x * x.
4. Define another method cube(int x) that returns x * square(x).
5. In the main method, create a Scanner object to read an integer from the user.
6. Read the input value.
7. Call the cube() method with the input value.
8. Display the result returned by the cube() method.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    int square(int x)
    {
        return x*x;
    }
    
    int cube(int x)
    {
        return x*square(x);
    }
    
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        Main obj = new Main();
        System.out.println(obj.cube(num));
    }
}

```
## OUTPUT:

<img width="549" height="248" alt="image" src="https://github.com/user-attachments/assets/98a3df76-16a6-4bb3-872a-5d021d54ec2a" />


## RESULT:
Thus, the Java program was successfully written and executed using methods where one method calls another to compute the cube of a number.
