# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a class MaxFinder with three overloaded max() methods: max(int a, int b) – returns the maximum of two integers. max(double a, double b) – returns the maximum of two double values. max(int a, int b, int c) – returns the maximum of three integers. In the main() method, demonstrate the use of each overloaded method with various inputs.

## AIM:
To implement compile-time polymorphism (method overloading) in Java by defining multiple max() methods with different parameter lists.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class MaxFinder with three overloaded max() methods:
    - max(int, int)
    - max(double, double)
    - max(int, int, int)
4. In each method, determine and return the maximum value.
5. In the main method, create a Scanner to read various inputs.
6. Read two integers, two doubles, and three integers from the user.
7. Create an object of MaxFinder.
8. Call each overloaded method using the input values.
9. Print the returned maximum values.
10. End the program.
    
## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class MaxFinder 
{

    int max(int a, int b) 
    {
        return (a > b) ? a : b;
    }

    double max(double a, double b) 
    {
        return (a > b) ? a : b;
    }

    int max(int a, int b, int c) 
    {
        int temp = (a > b) ? a : b;
        return (temp > c) ? temp : c;
    }
}

public class Main 
{
    public static void main(String[] args) 
    {

        Scanner sc = new Scanner(System.in);
        MaxFinder mf = new MaxFinder();

        int a = sc.nextInt();
        int b = sc.nextInt();

        double x = sc.nextDouble();
        double y = sc.nextDouble();

        int p = sc.nextInt();
        int q = sc.nextInt();
        int r = sc.nextInt();

        System.out.println("Max(" + a + ", " + b + "): " + mf.max(a, b));
        System.out.println("Max(" + x + ", " + y + "): " + mf.max(x, y));
        System.out.println("Max(" + p + ", " + q + ", " + r + "): " + mf.max(p, q, r));
    }
}

```
## OUTPUT:

<img width="682" height="460" alt="image" src="https://github.com/user-attachments/assets/dae005f2-1f10-4b3a-b5a1-104cc9afb81d" />


## RESULT:
Thus, the Java program was successfully written and executed to demonstrate polymorphism using method overloading.
