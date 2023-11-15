```java


import java.util.Arrays;

public class Array_Notation
{
   public static void main(String[] args)
   {
      int[] arr1 = new int[10];    // An array with "default" values.
      int[] arr2 = {12, 34, 56, 78, 90};     // Initialize an array.
            arr2 = {5, 4, 3, 2, 1};          // NOT ALLOWED!
            arr2 = new int[]{5, 4, 3, 2, 1}; // Assign an array value.
      int[] arr3 = new int[0]; // Java allows an empty array (C++ doesn't).
      int[] arr4 = {};
            arr1 = new int[]{};

      System.out.println( arr2 );   // NOT USEFUL!
      System.out.println( Arrays.toString(arr2) ); // Print an array.
      System.out.println( Arrays.toString(new int[]{4, 5, 6, 7}) );
      System.out.println( Arrays.toString(arr1) );
   }
}




public class Example1
{
   public static void main(String[] args)
   {
      int[] a1 = new int[15];
      int[] a2 = new int[10];
      int[] a3 = new int[5];
      a2 = a3;
      a3 = a1;
      // How many array objects are there now?
   }
}

public class Example2
{
   public static void main(String[] args)
   {
      int[] a1 = new int[10];
      int[] a2 = new int[5];
      int[] a3 = new int[2];
      a1 = a3;
      a2 = a1;
      // How many array objects are there now?
   }
}

public class Example3
{
   public static void main(String[] args)
   {
      int[] a1 = new int[15];
      int[] a2 = new int[10];
      int[] a3 = new int[5];
      int[] a4 = new int[0];
      a2 = a3;
      a3 = a1;
      a1 = a4;
      // How many array objects are there now?
   }
}




Section 6.4 Common Array Algorithms

 1. Filling
 2. Sum and Average Value
 3. Maximum and Minimum
 4. Element Separators
 5. Linear Search
 6. Removing an Element
 7. Inserting an Element
 8. Swapping Elements
 9. Copying Arrays
10. Reading Input




import java.util.Arrays;

public class Filter
{
   public static void main(String[] args)
   {
      int[] array1 = new int[10]; // Array for random numbers.

      for (int i = 0; i < array1.length; ++i) // Fill array with random integers.
      {
         array1[i] = (int)(21*Math.random()) - 10;
      }
      System.out.println( Arrays.toString(array1) );

      int count = 0; // Counter of the positive integers.

      for (int i = 0; i < array1.length; ++i)
      {
         if (array1[i] >= 0) // Find the positive integers.
         {
            ++count;
         }
      }

      int[] array2 = new int[count]; // Array for positive integers.

      int count2 = 0; // Index into the second array.
      for (int i = 0; i < array1.length; ++i)
      {
         if (array1[i] >= 0)// Find the positive integers.
         {
            array2[count2] = array1[i]; // Copy.
            ++count2;                   // Keep track of where we are in the 2nd array.
         }
      }
      System.out.println( count2 );
      System.out.println( Arrays.toString(array2) );
   }
}
```