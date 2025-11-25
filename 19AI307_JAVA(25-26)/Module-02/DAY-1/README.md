# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a class Car with attributes brand, model, and year, then create two objects of this class and print their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class named Car with attributes brand, model, and year.
4. In the main method, create two objects of the Car class.
5. Assign values to the attributes for each object.
6. Print the details of Car 1.
7. Print the details of Car 2.
8. End the program.
9. 
## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.*;
class Car
{
    String brand;
    String model;
    int year;
}
public class Main 
{
    public static void main(String[] args) 
    {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}

```
## OUTPUT:

<img width="622" height="250" alt="image" src="https://github.com/user-attachments/assets/7d58d22c-1eed-4a19-ae47-4069a2d07d88" />


## RESULT:
Thus, the Java program using classes and objects was successfully written and executed to create two Car objects and display their details.
