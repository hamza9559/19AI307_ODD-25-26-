# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:

To implement a library system where Books are created and managed only within a Library, demonstrating composition.
## ALGORITHM :
1. Start the program and create a Library object.
2. Read the number of books to be added from the user.
3. For each book, read the title and author.
4. Create a Book object inside the Library and store it in a list.
5. After adding all books, traverse the list to display details of each book.
6. End the program ensuring that books cannot exist independently of the library.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054 
*/
```

## SOURCE CODE:

```JAVA
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {

    private List<Book> books = new ArrayList<>();
    public void addBook(String title, String author) {
        // Type Your Code Here
        books.add(new Book(title, author)); 
    }

    public void showBooks() {
        // Type Your Code Here
        System.out.println("Books in Library:");
        for (Book book : books) {
            System.out.println("- " + book.getDetails());
        }
    }
}


```





## OUTPUT:


<img width="1288" height="618" alt="image" src="https://github.com/user-attachments/assets/136907e8-1ae5-4a5a-8660-709c57125a9e" />


## RESULT:
The program executed successfully and displayed all books stored in the library, demonstrating composition where books are fully managed by the library.
