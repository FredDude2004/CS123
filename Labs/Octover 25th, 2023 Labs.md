# October 25th, 2023 Labs
## Lab 1
Write a program that reads a single strictly positive integer n and then prints a table with n+1 rows and 2*n columns of characters.

Instead of describing in words what the table should look like, here is an example with n being 8.
<pre>
++++++++++++++++
\++++++++++++++/
\\++++++++++++//
\\\++++++++++///
\\\\++++++++////
\\\\\++++++/////
\\\\\\++++//////
\\\\\\\++///////
\\\\\\\\////////
</pre>
Notice that there are 8+1 = 9 lines of output. The table has 2*8 = 16 columns.

The number n is the number of '\' characters in the last line (and also the number of '/' characters in the last line).

In the top line of the table the number of '+' characters is 2*n. In every other line of the table, there is one more '\', one more '/', and two less '+''s than in the line above it.

Hint: Write an outer loop that chooses the row number (from row 0 to row n). Then write three loops nested in the outer loop (but NOT nested in each other) that print the three parts of a line, the \ part, the + part, and then the / part.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n = in.nextInt();
      
      for (int i = 1; i <= n + 1; i++)
      {
         for (int j = 1; j <= n * 2; j++)
         {
            if (j > (-1 + i) && j < ((n*2) + 2) - i)
            {
               System.out.print("+");
            }
            else if (j > n)
            {
               System.out.print("/");
            }
            else
            {
               System.out.print("\\");
            }
         }
         System.out.println();
      }
   }
}
```

## Lab 2 
Write a program that reads a strictly positive integer n and then draws two pictures of a "fence" with n+1 fence posts and n sections of fencing.

Here is an example of the picture of a "fence". If n is 4, the picture should look like this.
<pre>
|==|==|==|==|
</pre>
If n is 1, then the picture of the fence looks like this.
<pre>
|==|
</pre>
This is the "fencepost problem". You can solve it two ways.

You can place the first post, |, and then iterate on fence-post, ==|.

Or you can iterate on post-fence, |==, and then place the last post, |.

For each input integer n, solve the fencepost problem both ways, so you produce two (identical) pictures of the fence.

This problem is a "warm up" problem for the next lab, which will have several "fencepost" problems in it.
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
         if (i < n)
         {
            System.out.print("|==");
         }
         else
         {
            System.out.print("|==|");
            System.out.println("\n");
         }
      }
      for (int i = 1; i <= n; i++)
      {
         if (i < n)
         {
            System.out.print("|==");
         }
         else
         {
            System.out.print("|==|");
            System.out.println();
         }
      }    
   }
}
```
## Lab 3 
Write a program that reads two strictly positive integers, n and m. Your program should print an n-by-m table of "cells".

A single "cell" looks like this.
<pre>
+--+
|  |
+--+
</pre>
A 3-by-5 table of cells has 3 rows and 5 columns of cells and looks like this.
<pre>
+--+--+--+--+--+
|  |  |  |  |  |
+--+--+--+--+--+
|  |  |  |  |  |
+--+--+--+--+--+
|  |  |  |  |  |
+--+--+--+--+--+
</pre>
This problem contains several fencepost problems. Every row of the table is a (horizontal) fencepost problem. There is also a vertical fencepost problem with the rows.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n = in.nextInt();
      int m = in.nextInt();
      
      for (int i = 1; i <= (n * 2) + 1; i++)
      {
         for (int j = 1; j <= m; j++)
         {
            if (i % 2 != 0 && j != m)
            {
               System.out.print("+--");
            }
            else if (i % 2 != 0 && j == m)
            {
               System.out.print("+--+");
               System.out.println();
            }
            else if (i % 2 == 0 && j != m)
            {
               System.out.print("|  ");
            }
            else
            {
               System.out.print("|  |");
               System.out.println();
            }
         }
      }
   }
}
```