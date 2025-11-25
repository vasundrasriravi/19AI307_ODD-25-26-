# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList) into a file and then deserialize the file back into objects.

## AIM:
To write a Java program that demonstrates serialization and deserialization of a list of Student objects using ObjectOutputStream and ObjectInputStream.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student class that implements Serializable.
4. Define fields: id, name, marks, along with a toString() method.
5. In the main method, create an ArrayList.
6. Read the number of students from the user.
7. For each student, read id, name, and marks, then add to the list.
8. Create a file (students.dat) and serialize the ArrayList using: ObjectOutputStream → writeObject()
9. Print a success message for serialization.
10. Open the same file using ObjectInputStream.
11. Deserialize the object using readObject() and cast to ArrayList.
12. Print a success message for deserialization.
13. Display all deserialized student details.
14. Handle exceptions using try–catch blocks.
15. End the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class prog {
    @SuppressWarnings("unchecked")
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        ArrayList<Student> list = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            sc.nextLine();
            String name = sc.nextLine();
            double marks = sc.nextDouble();
            sc.nextLine();
            list.add(new Student(id, name, marks));
        }

        String filename = "students.dat";

        try {
            ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename));
            oos.writeObject(list);
            oos.close();
            System.out.println("Students serialized successfully into: " + filename);
        } catch (Exception e) {
            System.out.println(e);
        }

        try {
            ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename));
            ArrayList<Student> deserialized = (ArrayList<Student>) ois.readObject();
            ois.close();

            System.out.println("Students deserialized successfully from: " + filename);
            System.out.println();
            System.out.println("Deserialized Students:");
            for (Student s : deserialized) {
                System.out.println(s);
            }
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
## OUTPUT:

<img width="1271" height="468" alt="image" src="https://github.com/user-attachments/assets/13117d36-f9c7-4071-aa42-e47a6ac9fe09" />


## RESULT:
Thus, the Java program was successfully written and executed to serialize and deserialize a list of Student objects using Java's object streams.
