# Exploring ArrayLists and Iterators in Java

## Objective

The goal of this exercise is to help students understand the usage of ArrayLists and Iterators in Java by creating a simple program that performs basic operations on a list of names.

## Requirements

1. Create a Java class named `ArrayListIteratorExercise`.
2. In the main method, create an `ArrayList` of `String`s called `names`.
3. Add at least five names to the list.
4. Print the contents of the `ArrayList` using a for-each loop.
5. Create an `Iterator` for the `ArrayList`.
6. Using the `Iterator`, remove all names that have a length less than 4 characters.
7. Print the modified `ArrayList` using the `Iterator`.

---

### Detailed Instructions

If you need a bit more help, you can follow these instructions.

1. Start by creating a new Java class named ArrayListIteratorExercise.

   ```java
   import java.util.ArrayList;
   import java.util.Iterator;

   public class ArrayListIteratorExercise {
       public static void main(String[] args) {
           // Your code here
       }
   }
   ```

2. Inside the main method, create an ArrayList of Strings called names and add at least five names to it.

   ```java
   List<String> names = new ArrayList<>();
   names.add("John");
   names.add("Amy");
   names.add("Eva");
   names.add("Michael");
   names.add("Sam");
   ```

3. Print the contents of the List using a for-each loop.

   ```java
   System.out.println("Original List:");
   for (String name : names) {
       System.out.println(name);
   }
   ```

4. Create an Iterator for the ArrayList.

   ```java
   Iterator<String> iterator = names.iterator();
   ```

5. Using the Iterator, remove all names that have a length less than 4 characters.

   ```java
   while (iterator.hasNext()) {
       String currentName = iterator.next();
       if (currentName.length() < 4) {
           iterator.remove();
       }
   }
   ```

6. Print the modified ArrayList using the Iterator.

   ```java
   System.out.println("\nModified ArrayList:");
   iterator = names.iterator(); // Reset the iterator
   while (iterator.hasNext()) {
       System.out.println(iterator.next());
   }
   ```

Run the program and observe the output. You should see the original List with all the names and the modified ArrayList with names that have a length of 4 or more characters.
