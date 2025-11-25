# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A library wants to maintain records of its members. All members share some common information: a unique member ID, the member’s name, and the date when they joined the library (membershipDate).

There are two types of members:

StudentMember: In addition to the base information, they have the course they are enrolled in (courseEnrolled).

FacultyMember: In addition to the base information, they have the department they belong to (department).
Read exactly 4 member records (Student/Faculty) and display all their details using inheritance.

## AIM:
To write a Java program that demonstrates the concepts of inheritance and aggregation by creating a base class Member and two derived classes StudentMember and FacultyMember, reading 4 member details from the user, and displaying them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Member with attributes: member ID, name, and membership date.
4. Add a constructor to initialize these attributes.
5. Create a derived class StudentMember extending Member and add courseEnrolled.
6. Create another derived class FacultyMember extending Member and add department.
7. In the main class, create an array to store 4 Member objects.
8. For each record, read the type (Student/Faculty) and the respective details.
9. Create the appropriate object (StudentMember or FacultyMember) and store it in the array.
10. After reading all 4 records, display the details of each member.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Member 
{
    String id, name, date;

    Member(String id, String name, String date) 
    {
        this.id = id;
        this.name = name;
        this.date = date;
    }

    void display() 
    {
        System.out.println("Member ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Membership Date: " + date);
    }
}

class StudentMember extends Member {
    String course;

    StudentMember(String id, String name, String date, String course) {
        super(id, name, date);
        this.course = course;
    }

    void display() {
        super.display();
        System.out.println("Student Member - Course Enrolled: " + course);
    }
}

class FacultyMember extends Member {
    String dept;

    FacultyMember(String id, String name, String date, String dept) {
        super(id, name, date);
        this.dept = dept;
    }

    void display() {
        super.display();
        System.out.println("Faculty Member - Department: " + dept);
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String type = sc.next();
        String id = sc.next();
        String name = sc.next();
        String date = sc.next();

        if (type.equals("Student")) {
            String course = sc.next();
            StudentMember s = new StudentMember(id, name, date, course);
            s.display();
        } else {
            String dept = sc.next();
            FacultyMember f = new FacultyMember(id, name, date, dept);
            f.display();
        }
    }
}

```
## OUTPUT:

<img width="1299" height="557" alt="image" src="https://github.com/user-attachments/assets/63dc2e07-3ba8-47ed-99c6-ea12de885f32" />


## RESULT:
Thus, the Java program implementing Inheritance and Aggregation was executed successfully.
