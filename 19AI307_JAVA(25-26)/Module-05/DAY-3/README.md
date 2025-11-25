# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.

## AIM:
To write a string into a text file using Java file handling classes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a FileWriter object with filename output.txt.
4. Write a string into the file using writer.write().
5. Close the file using writer.close().
6. Use try-catch to handle possible IOException.
7. Print a success message if writing completes.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168  
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;

public class WriteToFile {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("output.txt");
            writer.write("This is the content written to the file.");
            writer.close();
            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}


```
## OUTPUT:

<img width="879" height="231" alt="image" src="https://github.com/user-attachments/assets/b1944cf1-eb5f-46ee-b342-80475b293320" />


## RESULT:
Thus, the Java program to write a string into a text file using FileWriter was successfully written and executed.
