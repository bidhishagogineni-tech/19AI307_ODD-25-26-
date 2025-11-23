# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

<img width="471" height="318" alt="image" src="https://github.com/user-attachments/assets/34546079-31a3-4b32-8217-7cc81c1ae872" />


## AIM:

To implement composition in Java where a Library contains multiple Book objects. Books are created and stored only inside the Library, demonstrating that they cannot exist independently.
## ALGORITHM :
1.Read number of books.

2.For each book:

  Read title and author.

  Create a Book object inside the Library using addBook().

3.Store each Book in an internal list.

4.After all books are added, display all stored books using showBooks().



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: GOGINENI BIDHISHA
RegisterNumber:  212223040048
*/
```

## SOURCE CODE:
```

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
        books.add(new Book(title, author)); // Composition: Book created inside Library
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}


```






## OUTPUT:

<img width="873" height="523" alt="image" src="https://github.com/user-attachments/assets/1a4797f8-b6a8-4876-b6a1-1ea3ef067d1d" />


## RESULT:
The program is being implemented successfully.
