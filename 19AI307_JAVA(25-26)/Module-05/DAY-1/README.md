# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader in Java.

## AIM:
To write a Java program that demonstrates reading data from the keyboard using InputStreamReader wrapped with BufferedReader for efficient character input handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an InputStreamReader object using System.in.
4. Wrap it inside a BufferedReader object.
5. Use the readLine() method to read user input as a string.
6. Display the input back to the user with a greeting message.
7. Handle exceptions using try-catch.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.io.*;

public class prog {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);

            String name = br.readLine();

            System.out.println("Hello, " + name + "!");
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
## OUTPUT:

<img width="490" height="306" alt="image" src="https://github.com/user-attachments/assets/37c0a216-27f5-485a-a964-768feec524c6" />


## RESULT:
Thus, the Java program was successfully written and executed using InputStreamReader to read user input from the keyboard.
