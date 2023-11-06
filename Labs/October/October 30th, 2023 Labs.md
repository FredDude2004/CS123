# October 30th, 2023 Labs
## Lab 1 
Write a program that reads a strictly positive integer n and then prints a triangle pattern of size n.

Here are several examples of the triangle pattern. First, assume that n is less than 9.

If n has the value 6, then the triangle pattern looks like this.
<pre>
65432123456
 543212345
  4321234
   32123
    212
     1
</pre>
If n has the value 4, then the triangle pattern looks like this.
<pre>
4321234
 32123
  212
   1
</pre>
Here is an example with n equal to 14. For numbers that are larger than 9, your should only print the ones-place from the number. So, instead of printing the number 14, you should print just the number 4. And for 13 you should print just the number 3.
<pre>
432109876543212345678901234
 3210987654321234567890123
  21098765432123456789012
   109876543212345678901
    0987654321234567890
     98765432123456789
      876543212345678
       7654321234567
        65432123456
         543212345
          4321234
           32123
            212
             1
</pre>
For any integer i, you get its ones-place using the expression i % 10.

You need to write nested for-loops. The outer loop prints n lines of output. Inside of that loop will be three loops, one to print the leading spaces, then a loop to count down to 1, and then a third loop to count back up.

Create a small table, for n equal to 6, that records, for each line of output, the line number, the number of leading spaces in that line, and where that line starts counting down from. Use the table to help you write the limits for each loop.

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
         for (int j = 0; j != i + 1; j++)
         {
            if (j > 1)
            {
               System.out.print(" ");
            }
         }
         for (int k = n - i + 1; k != 0; k--)
         {
            if (k >= 10)
            {
               System.out.print(k - 10);
            }
            else
            {
               System.out.print(k);
            }
         }
         for (int l = 2; l <= n - i + 1; l++)
         {
            if (l >= 10)
            {
               System.out.print(l - 10);
            }
            else
            {
               System.out.print(l);
            }
         }
         System.out.println();
      }
   }
}
```

## Lab 2
Write a program that reads a strictly positive integer size and then prints an hourglass pattern of the given size.

Here are some examples of the hourglass pattern.

If size is equal to 6 then the hourglass looks like this.
<pre>
+------------+
|\........../|
| \......../ |
|  \....../  |
|   \..../   |
|    \../    |
|     \/     |
|     /\     |
|    /..\    |
|   /....\   |
|  /......\  |
| /........\ |
|/..........\|
+------------+
</pre>
If size is equal to 4 then the hourglass looks like this.
<pre>
+--------+
|\....../|
| \..../ |
|  \../  |
|   \/   |
|   /\   |
|  /..\  |
| /....\ |
|/......\|
+--------+
</pre>
If size is equal to 3 then the hourglass looks like this.
<pre>
+------+
|\..../|
| \../ |
|  \/  |
|  /\  |
| /..\ |
|/....\|
+------+
</pre>
If size is equal to 1 then the hourglass looks like this.
<pre>
+--+
|\/|
|/\|
+--+
</pre>
Notice that size is the number of rows in the top (or bottom) half of the hourglass (not including the "frame").

You need to write a lot of loops.

Your first loop prints the top line.

Your second loop prints the lines in the top half of the hour glass. For each line it needs to have three nested loops, the leading spaces, then the dots, and then the last spaces. Create a small table (for size equal to 6) to help you figure out the limits for each of the three nested loops.

Your third loop prints the lines in the bottom half of the hour glass. It should have three nested loops, the leading spaces, then the dots, and then the last spaces. This is very much like the second loop, but in "reverse" (it should count down).

The last loop prints the bottom line.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int size = in.nextInt();
      
      // first line
      for (int i = 1; i <= size * 2 + 2; i++)
      {
         if (i == 1 || i == size * 2 + 2)
         {
            System.out.print("+");
         }
         else 
         {
            System.out.print("-");
         }
      }
      System.out.println();
      
      // Top half of hour glass
      for (int i = 1; i <= size; i++)
      {
         System.out.print("|");
         for (int j = 1; j <= i; j++)
         {
            if (j == i)
            {
               System.out.print("\\");
            }
            else
            {
               System.out.print(" ");
            }
         }
         for (int k = size * 2 - (2 * i); k > 0; k--)
         {
            System.out.print(".");
         }
         System.out.print("/");
         for (int l = 1; l <= i - 1; l++)
         {
            System.out.print(" ");
         }
         System.out.println("|");
      }
      
       // Bottom half of hour glass
       for (int i = size; i >= 1; i--)
       {
         System.out.print("|");
         for (int j = 1; j <= i; j++)
         {
            if (j == i)
            {
               System.out.print("/");
            }
            else
            {
               System.out.print(" ");
            }
         }
         for (int k = size * 2 - (2 * i); k > 0; k--)
         {
            System.out.print(".");
         }
         System.out.print("\\");
         for (int l = 1; l <= i - 1; l++)
         {
            System.out.print(" ");
         }
         System.out.println("|");
       }
      
      // Bottom line
      for (int i = 1; i <= size * 2 + 2; i++)
      {
         if (i == 1 || i == size * 2 + 2)
         {
            System.out.print("+");
         }
         else 
         {
            System.out.print("-");
         }
      }
      System.out.println();
   }
}
```


