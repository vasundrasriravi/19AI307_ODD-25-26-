# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge there is one master console power switch that controls all gaming consoles. Whenever any player turns on a console it internally triggers the master power. The master switch must be a Singleton (only one instance ever created) and must keep a global access count. For each player access print:[PlayerName] accessed Master Power Switch. Total accesses so far: [count]

## AIM:
To implement the Singleton design pattern (single instance, shared state) in Java and demonstrate a global access counter that increments every time the master switch is accessed.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Singleton class MasterPowerSwitch with:
     - private static instance variable
     - private constructor
     - public static getInstance() method that returns the single instance
     - an accessCount variable and access(playerName) method that increments and prints the count
4. In main(), read integer n (number of players).
5. Loop n times and for each iteration read the player's name.
6. Obtain MasterPowerSwitch instance via getInstance() and call access(playerName).
7. Close the scanner.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance = null;
    private int accessCount = 0;
    
    private MasterPowerSwitch() {
    }
    
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }
    
    public void access(String playerName) {
        accessCount++;
        System.out.println(playerName + " accessed Master Power Switch. Total accesses so far: " + accessCount);
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        
        for (int i = 0; i < n; i++) {
            String playerName = sc.nextLine();
            MasterPowerSwitch powerSwitch = MasterPowerSwitch.getInstance();
            powerSwitch.access(playerName);
        }
        
        sc.close();
    }
}

```
## OUTPUT:

<img width="1297" height="330" alt="image" src="https://github.com/user-attachments/assets/cf3a9098-21bd-4cf4-be90-812cbf0ef175" />


## RESULT:
Thus, the Java program was successfully written to demonstrate the Singleton design pattern with a global access counter that increments each time the master switch is accessed.
