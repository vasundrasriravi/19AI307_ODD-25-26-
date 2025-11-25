# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Reversing a number means rearranging its digits in the opposite order. For example:

The reverse of 1234 is 4321

The reverse of 9870 is 789 (since leading zeros in the reversed number are not shown)

Write a Java program that takes an integer input from the user and then reverses its digits using a while loop.

The program should repeatedly extract the last digit of the number using the modulus operator (%) and then build the reversed number.

The loop should continue until the number becomes 0.

Finally, display the reversed number as output.

## AIM:
To write a Java program that reads an integer and reverses its digits using a while loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the integer input from the user.
4. Initialize a variable reversed = 0.
5. Use a while loop while the number is not 0.
6. Extract the last digit using % 10 and add it to reversed.
7. Remove the last digit using / 10.
8. Display the reversed number and end the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
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
        int n = sc.nextInt();
        int rev=0;
        while(n>0)
        {
            int rem=n%10;
            rev=rev*10+rem;
            n=n/10;
        }
        System.out.println("Reversed number: "+rev);
    }
}
```
## OUTPUT:

<img width="500" height="319" alt="image" src="https://github.com/user-attachments/assets/e4a9b053-2ab2-4c4b-ad4b-3d81ca99a0ad" />


## RESULT:
The program successfully reverses the input number and prints the result.

