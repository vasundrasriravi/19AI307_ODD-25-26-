# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to replace each space in a string with a hyphen (-).

## AIM:
To write a Java program using string functions to read a string from the user and replace all spaces with hyphens.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string input from the user.
4. Use the replace() method to replace every space character with a hyphen.
5. Store the modified string.
6. Display the modified string to the user.
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String s = sc.nextLine();
        String s1 = s.replace(' ','-');
        System.out.println("Modified string: "+s1);
    }
}
```
## OUTPUT:

<img width="831" height="323" alt="image" src="https://github.com/user-attachments/assets/dacd611b-dfe0-4dde-a101-9f81712fe126" />


## RESULT:
Thus, the Java program was successfully written and executed to replace each space in a string with a hyphen.
