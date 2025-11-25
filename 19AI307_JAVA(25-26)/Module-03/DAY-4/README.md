# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
Bot Types:
SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
RainBot: Predicts "COLD" if temperature < 20, else "WARM".

## AIM:
To write a Java program that implements an interface to create different weather prediction bots and display predictions based on the temperature.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface Bot with an abstract method prediction().
4. Create a class SunBot that implements Bot and predicts
   - “HOT” if temperature > 30
   - “MODERATE” otherwise

5. Create a class RainBot that implements Bot and predicts
     - “COLD” if temperature < 20
     - “WARM” otherwise
6. In the main() method, read the temperature and bot type from the user.
7. Create the appropriate bot object based on the bot type.
8. Call the prediction() method of the selected bot.
9. Display the result.
10. End the program.
## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface Bot 
{
    void prediction();
}

class SunBot implements Bot 
{
    int temp;
    SunBot(int a) 
    {
        temp = a;
    }
    public void prediction() 
    {
        if (temp > 30)
            System.out.println("HOT");
        else
            System.out.println("MODERATE");
    }
}

class RainBot implements Bot 
{
    int temp;
    RainBot(int a) 
    {
        temp = a;
    }
    public void prediction() 
    {
        if (temp < 20)
            System.out.println("COLD");
        else
            System.out.println("WARM");
    }
}

class prog 
{
    public static void main(String args[]) 
    {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int type = sc.nextInt();

        Bot b = null;

        if (type == 1) 
        {
            b = new SunBot(temperature);
        } 
        else if (type == 2) 
        {
            b = new RainBot(temperature);
        }

        if (b != null)
            b.prediction();
        else
            System.out.println("Invalid bot type");
    }
}

```
## OUTPUT:

<img width="400" height="233" alt="image" src="https://github.com/user-attachments/assets/60ceda6d-8a77-4a33-af10-3621de3d11e6" />


## RESULT:
Thus, the Java program using interfaces was successfully written, compiled, and executed to simulate weather prediction bots.
