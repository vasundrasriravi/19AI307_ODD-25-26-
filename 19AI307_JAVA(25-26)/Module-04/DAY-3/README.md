# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A student can enroll in multiple courses. The relationship is many-to-many via association.If No Courses were assigned, print "No courses enrolled."

## AIM:
To implement composition in Java by creating a Student class that contains a list of Course objects and displays all enrolled courses.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Course class with a name attribute and getter method.
4. Create a Student class with:
      - name
      - List to store enrolled courses
      - enroll() method to add courses
      - showCourses() method to display enrolled courses
5. In the main method, create a Scanner object to read input.
6. Read the student's name and create a Student object.
7. Read the number of courses.
8. Loop to read each course name and add it to the student's course list.
9. Call showCourses() to display all enrolled courses.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class AssociationExample 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String studentName = sc.nextLine();
        Student student = new Student(studentName);

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) 
        {
            String course = sc.nextLine();
            student.enroll(new Course(course));
        }

        student.showCourses();
        sc.close();
    }
}

class Course 
{
    private String name;

    public Course(String name) 
    {
        this.name = name;
    }

    public String getCourseName() 
    {
        return name;
    }
}

class Student 
{
    private String name;
    private List<Course> courses;

    public Student(String name) 
    {
        this.name = name;
        this.courses = new ArrayList<>();
    }

    public void enroll(Course c) 
    {
        courses.add(c);
    }

    public void showCourses() 
    {
        System.out.println(name + "'s enrolled courses:");

        if (courses.isEmpty()) 
        {
            System.out.println("No courses enrolled.");
            return;
        }

        for (Course c : courses) 
        {
            System.out.println("- " + c.getCourseName());
        }
    }
}

```
## OUTPUT:

<img width="874" height="377" alt="image" src="https://github.com/user-attachments/assets/0779820e-a05f-452d-9821-9db1806cc663" />


## RESULT:
Thus, the Java program was successfully written to demonstrate composition, where a Student object contains multiple Course objects and displays the enrolled courses.
