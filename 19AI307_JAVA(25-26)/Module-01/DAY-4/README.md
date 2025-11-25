# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To write a Java program that reads an array of integers and calculates the average of its elements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array from the user.
4. Create an integer array of the given size.
5. Read each element and add it to a variable sum.
6. Compute the average using sum / n.
7. Display the average value.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int size = sc.nextInt();
        int sum=0;
        int[] arr = new int[size];
        for(int i=0; i<size; i++)
        {
            arr[i]=sc.nextInt();
            sum=sum+arr[i];
        }
        System.out.printf("The average of elements is %.2f",(double)sum/size);
    }
}
```
## OUTPUT:

<img width="601" height="319" alt="image" src="https://github.com/user-attachments/assets/9dae41dd-8360-4832-85dd-aa804a582bba" />


## RESULT:
The program successfully calculates and displays the average of the array elements.

