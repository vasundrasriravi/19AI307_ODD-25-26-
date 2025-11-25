# Ex.No:3(C) ABSTRACTION

## QUESTION:
Write a Java program to implement abstraction using an abstract class MazeAgent with the abstract method generateNavigationCode().
Two child classes ScoutAgent and HunterAgent implement different behaviors to interpret a maze.

## AIM:
To write a Java program that demonstrates abstraction by using an abstract class and overriding abstract methods in derived classes for generating maze navigation codes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class MazeAgent containing an abstract method generateNavigationCode(String[] maze).
4. Create a subclass ScoutAgent that overrides the abstract method and records the corridor row numbers where the signal @ is found.
5. Create another subclass HunterAgent that counts all obstructions # and determines if the agent is trapped or can escape.
6. In the main method, read the number of maze rows.
7. Read all maze rows into a string array.
8. Read the agent type (1 for ScoutAgent, 2 for HunterAgent).
9. Create the corresponding agent object using abstraction (parent reference → child object).
10. Call generateNavigationCode() and print the final result.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class MazeAgent 
{
    abstract String generateNavigationCode(String[] maze);
}

class ScoutAgent extends MazeAgent 
{
    String generateNavigationCode(String[] maze) 
    {
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < maze.length; i++) 
        {
            for (char ch : maze[i].toCharArray()) 
            {
                if (ch == '@') sb.append(i + 1);
            }
        }
        return sb.toString();
    }
}

class HunterAgent extends MazeAgent 
{
    String generateNavigationCode(String[] maze) 
    {
        int c = 0;
        for (String r : maze) 
        {
            for (char ch : r.toCharArray()) 
            {
                if (ch == '#') c++;
            }
        }
        return c >= 10 ? "TRAPPED" : "ESCAPE";
    }
}

public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        String[] maze = new String[n];
        for (int i = 0; i < n; i++) maze[i] = sc.nextLine();

        int t = sc.nextInt();

        MazeAgent agent = (t == 1) ? new ScoutAgent() : new HunterAgent();
        System.out.println(agent.generateNavigationCode(maze));
    }
}

```
## OUTPUT:

<img width="377" height="629" alt="image" src="https://github.com/user-attachments/assets/8bcd121e-318f-4838-a974-27ed831e005d" />


## RESULT:
Thus, the Java program using abstraction was successfully written and executed.
The abstract class and overridden methods worked correctly for both agent types.
