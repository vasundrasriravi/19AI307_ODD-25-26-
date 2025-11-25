# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program that uses the Integer wrapper class and Math.pow() to determine whether a given number is an Armstrong number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer input from the user.
4. Convert the number into an Integer wrapper class object.
5. Find the number of digits using obj.toString().length().
6. Extract each digit using modulo and division.
7. Raise each digit to the power of the total number of digits using Math.pow().
8. Add the powered digits to compute the sum.
9. Compare the sum with the original number.
10. If equal, it is an Armstrong number; otherwise, it is not.
11. Display the result.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168  
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog 
{
    public static void main(String args[]) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        
        Integer obj = Integer.valueOf(n);
        int digits = obj.toString().length();
        
        int temp = n;
        int sum = 0;

        while (temp > 0) 
        {
            int d = temp % 10;
            sum += (int)Math.pow(d, digits);
            temp /= 10;
        }

        if (sum == n)
            System.out.println(n + " is an Armstrong number.");
        else
            System.out.println(n + " is not an Armstrong number.");
    }
}





```
## OUTPUT:

<img width="879" height="330" alt="image" src="https://github.com/user-attachments/assets/2604a5cb-3f80-44f1-9873-3fd3762fa908" />


## RESULT:
Thus, the Java program using the Integer wrapper class and Math.pow() was successfully written and executed to check whether a number is an Armstrong number.
