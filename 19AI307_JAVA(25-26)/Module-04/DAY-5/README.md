# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Write a DAO (Data Access Object) class for a Contact model with fields name and phone.Implement a method to return all contacts whose names start with a specific letter.

## AIM:
To implement the DAO Behavioural Pattern in Java by separating data access logic from business logic, and retrieving contacts based on a starting letter.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Contact model class with name and phone attributes.
4. Create a ContactDAO interface with: - addContact(Contact contact) - getContactsStartingWith(char letter)
5. Implement ContactDAOImpl to store contacts in an ArrayList.
6. In addContact(), add Contact objects to the list.
7. In getContactsStartingWith(), loop through the list and filter contacts whose names begin with the given letter.
8. In the main method, read n (number of contacts).
9. Read name and phone for each contact and add them via the DAO.
10. Read a letter from the user.
11. Call getContactsStartingWith() and print the matching contacts.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: VASUNDRA SRI R
RegisterNumber: 212222230168 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Contact {
    private String name;
    private String phone;

    public Contact(String name, String phone) {
        this.name = name;
        this.phone = phone;
    }

    public String getName() {
        return name;
    }

    public String getPhone() {
        return phone;
    }
}

interface ContactDAO {
    void addContact(Contact contact);
    List<Contact> getContactsStartingWith(char letter);
}

class ContactDAOImpl implements ContactDAO {
    
    private List<Contact> contacts = new ArrayList<>();

    public void addContact(Contact contact) {
        contacts.add(contact);
    }

    public List<Contact> getContactsStartingWith(char letter) {
        List<Contact> filtered = new ArrayList<>();

        for (Contact c : contacts) {
            if (c.getName().charAt(0) == letter) {
                filtered.add(c);
            }
        }
        return filtered;
    }
}

public class ContactManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ContactDAO dao = new ContactDAOImpl();

        int n = sc.nextInt();
        sc.nextLine(); 

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            String phone = sc.nextLine();
            dao.addContact(new Contact(name, phone));
        }

        char letter = sc.next().charAt(0);

        List<Contact> result = dao.getContactsStartingWith(letter);

        for (Contact c : result) {
            System.out.println(c.getName());
            System.out.println(c.getPhone());
        }

        sc.close();
    }
}

```
## OUTPUT:

<img width="409" height="745" alt="image" src="https://github.com/user-attachments/assets/8487e36e-8a53-4b22-8ba2-647b252d71b3" />


## RESULT:
Thus, the Java program was successfully written and executed using the DAO Behaviour Pattern, enabling structured data access and retrieval of contacts starting with a specific letter.
