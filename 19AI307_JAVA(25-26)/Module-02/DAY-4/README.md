# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a Java program that uses a constructor to initialize variables and overrides the toString() method to display object details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class named Student with private variables name and age.
4. Define a constructor that accepts name and age and initializes the variables.
5. Override the toString() method to return the student details in a formatted string.
6. In the main method, create a Scanner object to read input from the user.
7. Read the name as a string.
8. Read the age as an integer.
9. Create an object of the Student class using the constructor and pass the input values.
10. Print the Student object, which automatically calls the toString() method.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Student 
{
    private String name;
    private int age;

    public Student(String name, int age) 
    {
        this.name = name;
        this.age = age;
    }
    @Override
    public String toString() 
    {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();

        Student s = new Student(name, age);

        System.out.println(s);  
    }
}

```
## OUTPUT:

<img width="738" height="376" alt="image" src="https://github.com/user-attachments/assets/d8c787d7-798e-4498-becc-7284e400302b" />


## RESULT:
Thus, the Java program using a constructor and an overridden toString() method was successfully written and executed to display the student details.
