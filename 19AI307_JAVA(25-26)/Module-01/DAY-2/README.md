# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a haunted house, lights turn on or off based on the hour of entry:

If the hour is even and between 2 and 6 (inclusive), lights flicker.

If the hour is odd and between 7 and 11, lights stay off.

If the hour is 12, lights turn red.

Otherwise, the house is dark.

## AIM:
To write a Java program that uses conditional statements to determine the state of lights in a haunted house based on the hour of entry.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a Scanner object to read the hour input from the user
4. Read the hour as an integer.
5. Check if the hour is even and between 2 and 6 (inclusive):
6. Display “Lights flicker”.
7. Else if the hour is odd and between 7 and 11:
8. Display “Lights stay off”.
9. Else if the hour is 12:
10. Display “Lights turn red”.
11. Display “The house is dark”.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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
        int hr = sc.nextInt();
        if(hr%2==0 && hr>=2 && hr<=6)
        {
            System.out.println("Lights flicker");
        }
        else if(hr%2!=0 && hr>=7 && hr<=11)
        {
            System.out.println("Lights off");
        }
        else if(hr==12)
        {
            System.out.println("Lights red");
        }
        else
        {
            System.out.println("Dark house");
        }
    }
}
```
## OUTPUT:

<img width="522" height="372" alt="image" src="https://github.com/user-attachments/assets/9b06b53b-1f4d-4ed6-8b94-a57d7ac6a7d2" />


## RESULT:
Thus, the Java program to implement conditional statements for the haunted house lighting system was successfully executed.
