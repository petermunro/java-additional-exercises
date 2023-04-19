# Sorting Custom Objects with Comparable in Java

## Objective

The goal of this exercise is to help students understand the usage of the `Comparable` interface by creating a simple program that sorts custom objects.

## Requirements

1. Create a Java class named `Book` that implements the `Comparable` interface.
2. Add instance variables for `title`, `author`, and `publicationyear` to the `Book` class.
3. Create a constructor for the `Book` class that accepts the title, author, and publication year as arguments.
4. Override the `compareTo` method in the `Book` class to compare books based on their publication year.
5. Create a Java class named `BookSortingExercise` with a main method.
6. In the main method, create an `ArrayList` of `Book` objects and add at least five `Book` instances.

   > You can try, for example, these:
   >
   > - "The Catcher in the Rye", "J.D. Salinger", 1951
   > - "To Kill a Mockingbird", "Harper Lee", 1960
   > - "1984", "George Orwell", 1949
   > - "Pride and Prejudice", "Jane Austen", 1813
   > - "The Great Gatsby", "F. Scott Fitzgerald", 1925

7. Sort the `ArrayList` of `Book` objects and print the sorted list.

---

## Detailed Instructions

If you need a bit more help, you can follow these instructions.

1. Start by creating a new Java class named `Book` that implements the `Comparable` interface.

   ```java
   public class Book implements Comparable<Book> {
       // Your code here
   }
   ```

2. Add instance variables for `title`, `author`, and `publication` year to the `Book` class.

   ```java
   private String title;
   private String author;
   private int publicationYear;
   ```

3. Create a constructor for the `Book` class that accepts the `title`, `author`, and `publication` year as arguments.

   ```java
   public Book(String title, String author, int publicationYear) {
       this.title = title;
       this.author = author;
       this.publicationYear = publicationYear;
   }
   ```

4. Override the `compareTo` method in the `Book` class to compare books based on their publication year.

   ```java
   @Override
   public int compareTo(Book other) {
       return other.publicationYear - this.publicationYear;
   }
   ```

   Another way of approaching this is:

   ```java
   @Override
   public int compareTo(Book other) {
       return Integer.compare(this.publicationYear, other.publicationYear);
   }
   ```

5. Create a Java class named `BookSortingExercise` with a main method.

   ```java
   import java.util.ArrayList;
   import java.util.Collections;

   public class BookSortingExercise {
       public static void main(String[] args) {
           // Your code here
       }
   }
   ```

6. In the main method, create an `ArrayList` of `Book` objects and add at least five `Book` instances.

   ```java
   List<Book> books = new ArrayList<>();
   books.add(new Book("The Catcher in the Rye", "J.D. Salinger", 1951));
   books.add(new Book("To Kill a Mockingbird", "Harper Lee", 1960));
   books.add(new Book("1984", "George Orwell", 1949));
   books.add(new Book("Pride and Prejudice", "Jane Austen", 1813));
   books.add(new Book("The Great Gatsby", "F. Scott Fitzgerald", 1925));
   ```

7. Sort the ArrayList of `Book` objects and print the sorted list.

   ```java
   Collections.sort(books);

   System.out.println("Sorted Books by Publication Year:");
   for (Book book : books) {
       System.out.println(book.getTitle() + " by " + book.getAuthor() + " (" + book.getPublicationYear() + ")");
   }
   ```

After completing the exercise, run the program and observe the output. The `ArrayList` of `Book` objects should be sorted by their publication year. This exercise should help you understand how to use the `Comparable` interface to sort custom objects in Java.
