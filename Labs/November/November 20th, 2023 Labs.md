# November 20th, 2023 Labs
## Lab 1 
In the Main class below, write a public static method called initials that has an String array input parameter and returns a String value made up of the first letter from each String in the input array.

Your method should put the characters in its output String in the same order that they were found in the input array.

If the method's input array looks like this
<pre>
{"cantaloupe", "apple", "tangerine", "strawberry"}
</pre>
then the String returned by the method should be
<pre>
"cats"
</pre>
You do not need to write any code that calls your method. Your method will be called and tested by another program.

```java
public class Main
{
   /* Define your method in this class. */
   public static String initials(String[] str)
   {
      String result = "";
      for (int i = 0; i < str.length; i++)
      {
         result += str[i].substring(0,1);
      }
      return result;
   }
}
```

## Lab 2
In the Main class below, write a public static method called labMethod that has a single integer parameter n (which must be a strictly positive integer), and returns an integer array filled with the integers from 1 up to n followed by the integers from n-1 down to 1 (this is similar to Lab 1 from last Wednesday).

You do not need to write any code that calls your method. Your method will be called and tested by another program.

If the method's parameter is 5, then the array that the method returns should hold
<pre>
1 2 3 4 5 4 3 2 1
</pre>
Your method can assume that its integer parameter will always be strictly positive.

Hint: Your method needs to create the array object that it will fill and return.

```java
public class Main
{
   /* Define your method in this class. */
   public static int[] labMethod(int n)
   {
      int[] result = new int[n * 2 - 1];
      for (int i = 1; i <= result.length; i++)
      {
         if (i <= n)
         {
            result[i - 1] = i;
         }
         else
         {
            result[i - 1] = n * 2 - i;
         }
      }
      
      return result;
   }
}
```

## Lab 3 
In the Main class below, write a public static method called labMethod that has an integer array input parameter and returns an integer array that holds all the integer values from the input array that are greater than or equal to the average value of the integers from the input array (this is similar to Lab 2 from last Wednesday).

Your method should place the integers in its output array in the same order that they were found in the input array.

If the method's input array holds the integers
<pre>
1 9 2 8 3 7 4 6 10 5
</pre>
then their average is 5.5, so the array returned by the method should hold the following integers
<pre>
9 8 7 6 10
</pre>
in that order.

You do not need to write any code that calls your method. Your method will be called and tested by another program.

```java
public class Main
{
   /**
      Define your method in this class.
      Your method will need five steps.
      1. Find the average of the integers in its input array.
      2. Count how many numbers in the input array are above average.
      3. Create the correctly sized output array.
      4. Fill the output array with the numbers from the input array that are above average.
      5. Return the output array.
   */
   public static double average(int[] arr, int size)
   {
      double sum = 0.0;
      double count = 0.0;
      for (int i = 0; i < size; i++)
      {
         sum += arr[i];
         count++;
      }
      double average = sum / count;
      return average;
   }
   
   public static int[] labMethod(int[] array)
   {
      double avg = average(array, array.length); // step 1
      int size = 0; 
      for (int i = 0; i < array.length; i++) // step 2
      {
         if (array[i] >= avg)
         {
            size++;
         }
      }
      
      int[] result = new int[size]; // step 3
      int resultIndex = 0;
      for (int j = 0; j < array.length; j++) // step 4
      {
         if (array[j] >= avg)
         {
            result[resultIndex] = array[j];
            resultIndex++;
         }
      }
      return result; // step 5
   }
}
```