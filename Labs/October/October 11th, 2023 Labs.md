# October 11, 2023 Labs
## Lab 1 
Write a program that reads two integers.

Print out all the integers between the two inputs (inclusive).

Your program can assume that the first input integer must be less than the second input integer.
```java
public class Main 
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      
      while (n1 <= n2)
      {
         System.out.println(n1);
         ++n1;
      }
   }
}
```

## Lab 2 
Write a program that reads two integers.

Output all the even integers between the two input integers (inclusive).

Your program can assume that the first input integer must be less than the second input integer.

The two input integers need not be even numbers.

Remember that a number n is even if n % 2 is equal to 0.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      
      while (n1 <= n2)
      {
         if (n1 % 2 == 0)
         {  
            System.out.println(n1);
            ++n1; ++n1;
         }
         else
         {
            ++n1;   
         }
      }
   }
}
```

## Lab 3 
Write a program that reads integer values and prints out the square of each input.

If there are no input integers, then your program should not print anything.

Your program can determine if the Scanner object has another input integer by calling the boolean method hasNextInt(). See https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/18

For example, if the input is
<pre>
2 5 7
</pre>
then the output should be
<pre>
2 squared is 4
5 squared is 25
7 squared is 49
</pre>

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n;
      while (in.hasNextInt())
      {
         n = in.nextInt();
         System.out.println(n + " squared is " + n*n);
      }
   }
}
```

## Lab 4 
Write a program that reads integer values and prints out the second strictly positive integer found in the input values.

Your program can assume that the input values must contain at least two strictly positive integers.

For example, if the input is
<pre>
-2 -3 -1 0 -5 6 0 -1 -7 8 -4 -3 9 -2
</pre>
then the output should be 
<pre>
8
</pre>

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int temp;
      
      while (n < 1)
      {
         n = in.nextInt();   
      }
      temp = n;
      n = in.nextInt();
      while (n < 1)
      {
         n = in.nextInt();   
      }
      
      System.out.println(n);
   
   }
}
```