# Using Custom Comparators to Sort Books

## Objective

The goal of this exercise is to help you understand the usage of custom comparators in Java. You will build upon the previous exercise with the `Book` class and create custom comparators to sort books by title and author in addition to the publication year.

## Requirements

1. Create a custom comparator for sorting `Book` objects by title.
2. Create a custom comparator for sorting `Book` objects by author.
3. Sort the `List` of `Book` objects by title using the custom title comparator and print the sorted list.
4. Sort the `List` of `Book` objects by author using the custom author comparator and print the sorted list.

---

## Derailed Instructions

As before, you can follow these steps if you need more help.

1. Create a custom comparator for sorting `Book` objects by title.

   ```java
   public class TitleComparator implements Comparator<Book> {
        @Override
        public int compare(Book book1, Book book2) {
            return book1.getTitle().compareTo(book2.getTitle());
        }
    }
   ```

2. Create a custom comparator for sorting `Book` objects by author.

   ```java
   public class AuthorComparator implements Comparator<Book> {
        @Override
        public int compare(Book book1, Book book2) {
            return book1.getAuthor().compareTo(book2.getAuthor());
        }
    }
   ```

3. Sort the `List` of `Book` objects by title using the custom title comparator and print the sorted list.

   ```java
   Comparator<Book> titleComparator = new TitleComparator();

   Collections.sort(books, titleComparator);

   System.out.println("Sorted Books by Title:");
   for (Book book : books) {
       System.out.println(book.getTitle() + " by " + book.getAuthor() + " (" + book.getPublicationYear() + ")");
   }
   ```

4. Sort the `List` of `Book` objects by author using the custom author comparator and print the sorted list.

   ```java
   Comparator<Book> authorComparator = new AuthorComparator();

   Collections.sort(books, authorComparator);

   System.out.println("\nSorted Books by Author:");
   for (Book book : books) {
       System.out.println(book.getTitle() + " by " + book.getAuthor() + " (" + book.getPublicationYear() + ")");
   }
   ```

After completing the exercise, run the program and observe the output.

The `List` of `Book` objects should be sorted by title and author using the custom comparators. This exercise should help students understand how to create and use custom comparators in Java to sort objects based on various properties.
