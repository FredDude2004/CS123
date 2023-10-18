# October 18th, 2023 Labs
## Lab 1 
Write a program that reads a sequence of words and prints the index in the sequence of each word that matches the first word.
Your program should use the Scanner's hasNext() method to decide when to stop looping.
The input sequence will always contain at least one word.
If the input sequence is
<pre>
dog cat dogs bear dog pear dog apple orange dog cats and more cats
</pre>
then your program should print out
<pre>
5, 7, 10
</pre>
If the input sequence is
<pre>
what where why when who what ever
</pre>
then your program should print out
<pre>
6
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String first = in.next();
      String word;
      int i = 1;
      String indices = "";
      
      while (in.hasNext())
      {
         i++;
         word = in.next();
         if (first.equals(word))
         {
            indices += i + ", ";
         }
      }
      indices = indices.substring(0, indices.length() - 2);
      System.out.print(indices);
   }
}
```
## Lab 2 
Wite a program that reads a sequence of integers and prints out the first input integer and then prints each following integer if it is greater than the last integer that was printed.

The sequence of integers will always have at least one number.

If the input sequence is
<pre>
1 2 1 3 2 1 2 3 4 5 4 3 2 3 4 5 6 7 6 5 4 5 6 7 8 9
</pre>
then your program should print out
<pre>
1 2 3 4 5 6 7 8 9
</pre>
If the input sequence is
<pre>
5 5 5 5 5 5
</pre>
then your program should print out
<pre>
5
</pre>
If the input sequence is
<pre>
5 1 2 3 4 5 6
</pre>
then your program should print out
<pre>
5 6
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {  
      Scanner in = new Scanner(System.in);
      int largest = in.nextInt();
      int nextNum;
      String values = "";
      
      System.out.print(largest);
      while (in.hasNext())
      {
         nextNum = in.nextInt();
         if (largest < nextNum)
         {
            values += " " + nextNum;
            largest = nextNum;
         }
      }
      System.out.println(values);
   }
}
```
## Lab 3
Write a program that reads a sequence of integers and then prints three lines of output. The first line of output is the minimum number from the sequence. The second line of output is the maximum number from the sequence. The third line of output is the word True if the first occurrence of the max occurs after the last occurrence of the min in the sequence, and the word False otherwise.

The input sequence will always contain at least two numbers.

Hint: As you read the sequence, keep track of the max and min values and also keep track of where you found each of them. In particular, keep track of the last index where you found the min and keep track of the first index where you find the max.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n = in.nextInt();
      int Max = n;
      int Min = n;
      int lastMin = 1;
      int firstMax = 1;
      int count = 1;
      
      while (in.hasNextInt())
      {
         count++;
         n = in.nextInt();
         if (n > Max)
         {
            Max = n;
            firstMax = count;
         }
         else if (n <= Min)
         {
            Min = n;
            lastMin = count;
         }
      }
      System.out.print(Min + "\n" + Max + "\n");
      if (lastMin < firstMax) 
      {
         System.out.println("True");
      }  
      else 
      {
         System.out.println("False");
      }
   }
}
```