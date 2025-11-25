# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to determine the priority and name of the current thread.
Note: Read the thread name from the user.

## AIM:
To write a Java program that reads a thread name from the user, sets it to the current thread, and displays the thread priority and full thread details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the thread name as input from the user.
4. Get the current thread using Thread.currentThread().
5. Set the thread’s name using setName().
6. Retrieve the thread priority using getPriority().
7. Display the thread name, priority, and full thread information.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(name);
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
        sc.close();
    }
}

```
## OUTPUT:

<img width="874" height="280" alt="image" src="https://github.com/user-attachments/assets/f2666a91-f456-4ec8-8596-3f565b0b2f52" />


## RESULT:
Thus, the Java program to determine the priority and name of the current thread was successfully written and executed.
