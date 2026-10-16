import java.util.*;
public class BookLookupSystem {
    public static void main(String[] args) {
        Hashtable<Integer, String> books = new Hashtable<>();
        Scanner sc = new Scanner(System.in);
        int choice, id;
        do {
            System.out.println("\n1. Add a Book");
            System.out.println("2. Search a Book");
            System.out.println("3. Remove a Book");
            System.out.println("4. Display All Books");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();
            switch (choice) {
                case 1:
                    System.out.print("Enter Book ID: ");
                    id = sc.nextInt();
                    sc.nextLine();
                    System.out.print("Enter Book Title: ");
                    String title = sc.nextLine();
                    books.put(id, title);
                    System.out.println("Book added successfully.");
                    break;
                case 2:
                    System.out.print("Enter Book ID: ");
                    id = sc.nextInt();
                    if (books.containsKey(id))
                        System.out.println("Book ID: " + id +
                                ", Title: " + books.get(id));
                    else
                        System.out.println("Book not found.");
                    break;
                case 3:
                    System.out.print("Enter Book ID: ");
                    id = sc.nextInt();
                    if (books.containsKey(id)) {
                        books.remove(id);
                        System.out.println("Book removed successfully.");
                    } else
                        System.out.println("Book not found. Unable to remove.");
                    break;
                case 4:
                    if (books.isEmpty())
                        System.out.println("No books available in the library.");
                    else {
                        for (Map.Entry<Integer, String> entry :
                                books.entrySet()) {
                            System.out.println("Book ID: " + entry.getKey()
                                    + ", Title: " + entry.getValue());
                        }
                    }
                    break;
                case 5:
                    System.out.println("Exiting Book Lookup System.");
                    break;
                default:
                    System.out.println(
                            "Invalid choice. Please select a valid option.");
            }
        } while (choice != 5);
        sc.close();
    }
}
