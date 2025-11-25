# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads 4 strings from the user. For each input: If it can be converted to an integer → print Parsed number: If conversion fails (NumberFormatException) → print Not a valid number

## AIM:
To write a Java program that demonstrates exception handling using try–catch to safely parse integers and handle invalid inputs.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input.
4. Loop four times to read four strings from the user.
5. Inside the loop, attempt to convert the string to an integer using Integer.parseInt().
6. If conversion succeeds, print the parsed number.
7. If a NumberFormatException occurs, print "Not a valid number".
8. Close the Scanner.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class StringParser {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        for (int i = 0; i < 4 && sc.hasNext(); i++) {
            String input = sc.next();
            try {
                int num = Integer.parseInt(input);
                System.out.println("Parsed number: " + num);
            } catch (NumberFormatException e) {
                System.out.println("Not a valid number");
            }
        }
        
        sc.close();
    }
}

```
## OUTPUT:

<img width="737" height="325" alt="image" src="https://github.com/user-attachments/assets/af903e00-0da2-4e57-a970-0d5b0482be7f" />


## RESULT:
Thus, the Java program was successfully written and executed to demonstrate exception handling using try–catch for number parsing.
