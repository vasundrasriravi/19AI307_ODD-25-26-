# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Circle with a private instance variable radius. Provide public getter and setter methods to access and modify the radius variable. However, provide two methods called calculateArea() and calculatePerimeter() that return the calculated area and perimeter based on the current radius value.

## AIM:
To understand and implement access specifiers in Java using private data members and public getter and setter methods along with area and perimeter calculation.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Circle with a private variable radius.
4. Create public getter and setter methods to access and modify radius.
5. Define calculateArea() to compute and return π * radius * radius.
6. Define calculatePerimeter() to compute and return 2 * π * radius.
7. In the main method, create an object of Circle.
8. Read radius input from the user.
9. Set the radius using the setter method.
10. Call calculateArea() and calculatePerimeter() to compute values.
11. Display the radius, area, and perimeter.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Circle 
{
   
    private double radius;

  
    public double getRadius() 
    {
        return radius;
    }

   
    public void setRadius(double radius) 
    {
        this.radius = radius;
    }

    
    public double calculateArea() 
    {
        return Math.PI * radius * radius;
    }

   
    public double calculatePerimeter() {
        return 2 * Math.PI * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Circle c = new Circle();

        double r = sc.nextDouble();  
        c.setRadius(r);

        System.out.printf("Radius: %.2f\n", c.getRadius());
        System.out.printf("Area: %.2f\n", c.calculateArea());
        System.out.printf("Perimeter: %.2f\n", c.calculatePerimeter());
    }
}

```
## OUTPUT:

<img width="581" height="364" alt="image" src="https://github.com/user-attachments/assets/21aa05cc-e625-42bf-8552-550151a3f075" />


## RESULT:
Thus, the Java program was successfully written and executed using private variables and public getter, setter, and calculation methods to demonstrate access specifiers.
