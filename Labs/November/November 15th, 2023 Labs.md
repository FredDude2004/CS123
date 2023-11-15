# November 15th, 2023 Labs
## Lab 1
Write a program that reads a strictly positive integer n and then your program should create an integer array and fill it with the numbers from 1 up to n followed by the numbers from n-1 down to 1.

After your code creates and fills the array, it should call the method Tester.printArray with the name of your array as the method's argument.

If the input integer is
<pre>
 5
</pre>
then your array should hold
<pre>
1 2 3 4 5 4 3 2 1
</pre>
If the input integer is
<pre>
2
</pre>
then your array should hold
<pre>
1 2 1
</pre>
Your program can assume that the input integer will always be strictly positive.

```java
import java.util.Scanner;

public class Main
{
   
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int[] arr = new int[n * 2 - 1];
      
      for (int i = 1; i <= arr.length; i++)
      {
         if (i <= n)
         {
            arr[i - 1] = i;
         }
         else
         {
            arr[i - 1] = n * 2 - i;
         }
      }
      Tester.printArray(arr);
   }
}
```

## Lab 2
Write a program that reads a sequence of up to 50 integers and then prints out those input integers that are greater than or equal to the average value of all the input integers.

Your program should print the output integers in the same order that they were found in the input sequence and all the output integers should be printed on a single line.

The input sequence may have fewer than 50 integers and it may have more than 50 integers. Your program should stop reading input integers when either the Scanner no longer has any inputs or if the Scanner has already read 50 inputs (so you need to keep a counter of how many integers have been read).

Remember that you can use the Scanner method hasNextInt() to ask if the Scanner has another integer value.

You will need an array to remember what the input values were (and in what order they were in). After you have the average of all the input integers, then you can go back through them (in the array) and find the ones that are greater than or equal to the average.

Even though you are averaging integer values, their average value need not be an integer. So make the average a double value.

One final hint. Read the input integers using a while-loop and search through the array using a for-loop.

If the input integers are
<pre>
1 9 2 8 3 7 4 6 10 5
</pre>
then their average is 5.5, so the input integers that are above average are
<pre>
9 8 7 6 10
</pre>
in that order.

```java
import java.util.Scanner;

public class Main
{
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
   
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int[] array = new int[50];
      int count = 0;
      
      while (in.hasNextInt() && count < 50)
      {
         array[count] = in.nextInt();
         count++;
      }
   
      double avg = average(array, count);
         
      for (int j = 0; j < count; j++)
      {
         if (array[j] >= avg)
         {
            System.out.print(array[j] + " ");
         }
      }
      System.out.println();
   }
}
```

## Lab 3
Write a program that reads a sequence of up to 50 integers and then puts into an array those input integers that are positve and even.

After your program puts all the positve, even input integers into an array, it should call the method Tester.printArray with the name of your array as the method's argument.

Your array that is printed by Tester.printArray should only contain exactly those input integers that were positive and even.

Your array that is printed by Tester.printArray should contain the positive, even input integers in the same order that they were found in the input sequence.

The input sequence may have fewer than 50 integers and it may have more than 50 integers. Your program should stop reading input integers when either the Scanner no longer has any inputs or if the Scanner has already read 50 inputs (so you need to keep a counter of how many integers have been read, just like in the previous lab).

Remember that you can use the Scanner method hasNextInt() to ask if the Scanner has another integer value.

Notice that you will not know how many input integers are positive and even until you have looked at all of the input integers. So you do not know, when your program starts, how large to make the array that you will need to give to Tester.printArray. It could be that all 50 input integers are positive and even. Or it could be that none of the input integers are positive and even.

So what you need to do is create an array of size 50 to hold all of the possible input integers. As you fill that array with the available input integers, you need to check each input integer to see if it is positive and even and if so, count it.

Then create a second array with the size of that count (the number of input integes that were positive and even).

Then, go through the first array again, and copy from it, into the second array, those input numbers that were positrive and even. The second array is the array that you give to Tester.printArray.

So you need to write two loops.

First, write a while-loop that reads the input integers into the array of size 50. As you read each input integer, count it as an input. Also, check if the input integer is positive and even. If so, count it using a second counter (one counter for the number of input integers, and a second counter for the number of positive, even input integers).

Second, write a for-loop that goes through the first array and copies, into the second array, those input integers that were positive and even.

If the input integers are
<pre>
1  -3  -2  2  0  5  6  -4  8  0  10  -1
</pre>
then your second array should contain
<pre>
2 0 6 8 0 10
</pre>
in that order. Notice that 0 is a positive, even integer.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int[] source = new int[50];
      int count = 0;
      int size = 0;
      
      while (in.hasNextInt() && count < 50)
      {
         source[count] = in.nextInt();
         if (source[count] >= 0 && source[count] % 2 == 0)
         {
            size++;
         }
         count++;
      }
      
      int[] dest = new int[size];
      int destIndex = 0;
      
      for (int i = 0; i < count; i++)
      {
         if (source[i] >= 0 && source[i] % 2 == 0)
         {
            dest[destIndex] = source[i];
            destIndex++;
         }
      }
      Tester.printArray(dest);
   }
}
```
