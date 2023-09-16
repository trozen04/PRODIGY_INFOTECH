import java.util.ArrayList;
import java.util.Scanner;

class Contact {
    private String name;
    private String phoneNumber;
    private String email;

    public Contact(String name, String phoneNumber, String email) {
        this.name = name;
        this.phoneNumber = phoneNumber;
        this.email = email;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getPhoneNumber() {
        return phoneNumber;
    }

    public void setPhoneNumber(String phoneNumber) {
        this.phoneNumber = phoneNumber;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }

    @Override
    public String toString() {
        return "Name: " + name + "\nPhone: " + phoneNumber + "\nEmail: " + email + "\n";
    }
}

public class ContactManagementSystem {
    private static ArrayList<Contact> contacts = new ArrayList<>();
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        while (true) {
            System.out.println("\nContact Management System");
            System.out.println("1. Add a new contact");
            System.out.println("2. View contact list");
            System.out.println("3. Edit a contact");
            System.out.println("4. Delete a contact");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");

            int choice = scanner.nextInt();
            scanner.nextLine(); // Consume the newline

            switch (choice) {
                case 1:
                    addContact();
                    break;
                case 2:
                    viewContactList();
                    break;
                case 3:
                    editContact();
                    break;
                case 4:
                    deleteContact();
                    break;
                case 5:
                    System.out.println("Exiting the program. Goodbye!");
                    scanner.close();
                    System.exit(0);
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }

    private static void addContact() {
        System.out.print("Enter name: ");
        String name = scanner.nextLine();
        System.out.print("Enter phone number: ");
        String phoneNumber = scanner.nextLine();
        System.out.print("Enter email address: ");
        String email = scanner.nextLine();

        Contact contact = new Contact(name, phoneNumber, email);
        contacts.add(contact);

        System.out.println("Contact added successfully.");
    }

    private static void viewContactList() {
        if (contacts.isEmpty()) {
            System.out.println("Contact list is empty.");
        } else {
            System.out.println("\nContact List:");
            for (int i = 0; i < contacts.size(); i++) {
                System.out.println((i + 1) + ". " + contacts.get(i));
            }
        }
    }

    private static void editContact() {
        viewContactList();
        if (contacts.isEmpty()) {
            return;
        }

        System.out.print("Enter the index of the contact you want to edit: ");
        int index = scanner.nextInt();
        scanner.nextLine(); // Consume the newline

        if (index < 1 || index > contacts.size()) {
            System.out.println("Invalid index. Please try again.");
        } else {
            System.out.println("Editing contact at index " + index + ":");
            Contact contact = contacts.get(index - 1);

            System.out.print("Enter new name: ");
            contact.setName(scanner.nextLine());
            System.out.print("Enter new phone number: ");
            contact.setPhoneNumber(scanner.nextLine());
            System.out.print("Enter new email address: ");
            contact.setEmail(scanner.nextLine());

            System.out.println("Contact edited successfully.");
        }
    }

    private static void deleteContact() {
        viewContactList();
        if (contacts.isEmpty()) {
            return;
        }

        System.out.print("Enter the index of the contact you want to delete: ");
        int index = scanner.nextInt();
        scanner.nextLine(); // Consume the newline

        if (index < 1 || index > contacts.size()) {
            System.out.println("Invalid index. Please try again.");
        } else {
            Contact contact = contacts.remove(index - 1);
            System.out.println("Contact deleted successfully.");
        }
    }
}
