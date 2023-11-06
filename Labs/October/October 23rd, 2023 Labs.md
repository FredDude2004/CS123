# October 23rd, 2023 Labs
## Lab 1 
Write a program that reads a sequence of words. Your program should print one line of output for every pair of words. Let w1 and w2 be a pair of input words. The line of output should alternate characters from w1 with characters from w2 but make every letter from w1 be lowercase and make every letter from w2 be uppercase. If one of the two words is shorter than the other, then output a hyphen ('-') followed by the remaining characters from the longer word, using lower case for letters that come from w1 and uppercase for letters that come from w2.

The input sequence will always have an even number of words.

For example, if the input is
<pre>
bear crocodile watermelon plum cat dogs apple pears
</pre>
then the output should be 
<pre>
bCeRaOrC-ODILE
wPaLtUeM-rmelon
cDaOtG-S
aPpEpAlReS
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args) 
   {
      Scanner in = new Scanner(System.in);
      
      while (in.hasNext())
      {
         String w1 = in.next();
         String w2 = in.next();
         w1 = w1.toLowerCase();
         w2 = w2.toUpperCase();
         
         for (int j = 0; j < w1.length() || j < w2.length(); j++)
         {
            if (w1.length() == j)
            {
               System.out.print("-" + w2.substring(j));
               break;
            }
            else if (w2.length() == j)
            {
               System.out.print("-" + w1.substring(j));
               break;
            }
            else
            {
               System.out.print(w1.substring(j, j + 1) + w2.substring(j, j + 1));
            }
         }
         System.out.println();
      }
   }
}
```
Without Breaks
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args) 
   {
      Scanner in = new Scanner(System.in);
      
      while (in.hasNext())
      {
         String w1 = in.next();
         String w2 = in.next();
         w1 = w1.toLowerCase();
         w2 = w2.toUpperCase();
         
         for (int j = 0; j <= w1.length() && j <= w2.length(); j++)
         {
            if (w1.length() == j && w2.length() != j)
            {
               System.out.print("-" + w2.substring(j));
            }
            else if (w2.length() == j && w1.length() != j)
            {
               System.out.print("-" + w1.substring(j));
            }
            else if (w1.length() == j)
            {
               System.out.print("");
            }
            else
            {
               System.out.print(w1.substring(j, j + 1) + w2.substring(j, j + 1));
            }
         }
         System.out.println();
      }
   }
}
```
## Lab 2 
Write a program that reads a single strictly positive integer n and then prints a table with n rows and n columns of characters.

For the purpose of this problem we will think of the table's rows as being numbered from 1 to n and we will think of the columns as also being numbered from 1 to n.

 - Every table entry in an odd numbered row and an odd numbered column should be the character '@'.
 - Every table entry in an odd numbered row and an even numbered column should be the character '/'.
 - Every table entry in an even numbered row and an odd numbered column should be the character '/'.
 - Every table entry in an even numbered row and an even numbered column should be the character 'O'.
 - Remember that a number i is even if i % 2 is equal to 0 (and i is odd if i % 2 is equal to 1).

You need to write two nested for-loops. The outer for-loop chooses the row number. The inner for-loop prints the characters in that row.

Here is an example. If the input is the number
<pre>
8
</pre>
then the output is this 8-by-8 table
<pre>
@/@/@/@/
/O/O/O/O
@/@/@/@/
/O/O/O/O
@/@/@/@/
/O/O/O/O
@/@/@/@/
/O/O/O/O
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      
      for (int i = 1; i <= n; i++)
      {
         for (int j = 1; j <= n; j++)
         {
            if (i % 2 == 0 && j % 2 == 0)
            {
               System.out.print('O');
            }
            else if (i % 2 != 0 && j % 2 != 0)
            {
               System.out.print('@');
            }
            else
            {
               System.out.print('/');
            }
         }
         System.out.println();
      }
   }
}
```