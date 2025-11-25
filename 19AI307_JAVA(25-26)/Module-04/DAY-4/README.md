# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are creating a cross-platform UI tool using the Abstract Factory Design Pattern.Implement factories to create Button and Checkbox components for dark and light themes.The user chooses the theme, and the program must generate UI components and display their types.

## AIM:
To implement the Abstract Factory Design Pattern in Java by creating theme-based factories that generate UI components (Button and Checkbox) depending on the user-chosen theme.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create Button and Checkbox interfaces.
4. Implement DarkButton, LightButton, DarkCheckbox, and LightCheckbox classes.
5. Create an abstract factory interface UIFactory with createButton() and createCheckbox().
6. Implement DarkThemeFactory and LightThemeFactory to generate dark/light UI components.
7. In the main method, read the theme input from the user.
8. If theme is "dark", instantiate DarkThemeFactory; if "light", instantiate LightThemeFactory.
9. Use the factory to create Button and Checkbox objects.
10. Call create() on both objects to print the UI component type.
11. End the program.
## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button {
    void create();
}

interface Checkbox {
    void create();
}

class DarkButton implements Button {
    @Override
    public void create() {
        System.out.println("Dark Button created");
    }
}

class LightButton implements Button {
    @Override
    public void create() {
        System.out.println("Light Button created");
    }
}

class DarkCheckbox implements Checkbox {
    @Override
    public void create() {
        System.out.println("Dark Checkbox created");
    }
}

class LightCheckbox implements Checkbox {
    @Override
    public void create() {
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory {
    @Override
    public Button createButton() {
        return new DarkButton();
    }
    
    @Override
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    @Override
    public Button createButton() {
        return new LightButton();
    }
    
    @Override
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine();
        
        UIFactory factory;
        
        if (theme.equalsIgnoreCase("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equalsIgnoreCase("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            scanner.close();
            return;
        }
        
        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();
        
        button.create();
        checkbox.create();
        
        scanner.close();
    }
}

```
## OUTPUT:

<img width="870" height="379" alt="image" src="https://github.com/user-attachments/assets/6086c284-d036-4cbb-a5ec-edf4b413b635" />


## RESULT:
Thus, the Java program was successfully written and executed to demonstrate the Abstract Factory Pattern, generating UI components (Button and Checkbox) based on the selected theme.
