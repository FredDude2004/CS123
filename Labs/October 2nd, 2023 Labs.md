# October 2, 2023 Labs
## Lab 1
Write a program that reads one integer number n and one boolean value outsideMode.

Output the boolean value true if n is in the range 1 to 10, inclusive, and output false otherwise. Unless the boolean outsideMode is true, in which case output the boolean value true if the number is less or equal to 1 or greater or equal to 10, and output false otherwise.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      boolean outsideMode = in.nextBoolean();
      
      if (outsideMode)
      {
         if (n >= 1 || n <= 10)
         {
            System.out.println("true");   
         }
         else
         {
            System.out.println("false");  
         }
      }
      else
      {
         if (n >= 1 && n <= 10)
         {
            System.out.println("true");
         }   
         else
         {
            System.out.println("false");  
         }
      }
   }
}
```
## Lab 2 
Write a program that reads two integer values, a and b. You can assume that both of the integer values are positive.

Output the sum of the two integers so long as the sum has the same number of digits as a (the first integer). If the sum has more digits than a, then just output a.

Note: an easy way to compute the number of digits of a non-negative int n is to convert it to a String with the method String.valueOf(n) and then check the length of the String.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int a = in.nextInt();
      int b = in.nextInt(); 
      int lengthA = String.valueOf(a).length();
      int lengthAPlusB = String.valueOf(a + b).length();
      
      if (lengthAPlusB == lengthA)
      {
         System.out.println(a + b);   
      }
      else
      {
         System.out.println(a);   
      } 
   }
}
```
## Lab 3
Write a program that reads two integer values. You can assume that both of the integer values are positive.

Output the input number that is closest to 21 without going over 21. Output 0 if both input values go over 21.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int x = in.nextInt();
      int y = in.nextInt();
      
      if (x == y && x < 22)
      {
         System.out.println(x);   
      }
      else if ((x > y && x <= 21) || (y > 21))
      {
         System.out.println(x);
      }
      else if ((x < y && y <= 21) || (x > 21))
      {
         System.out.println(y);   
      }
      else
      {
         System.out.println(0);   
      }
   }
}
```
## Lab 4 
Write a program that reads three integer values.

Output the sum of the distinct input values.

For example, if the inputs are 1, 2, and 3, then the output is 6. If the inputs are 2, 3, and 3, then the putput is 5. If the inputs are 2, 2, and 2, then the output is 2.
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      int n3 = in.nextInt();
      
      if (n1 == n2 && n2 == n3)
      {
         System.out.println(n1);   
      }
      else if (n1 == n2)
      {
         System.out.println(n1 + n3);
      }
      else if (n2 == n3)
      {
         System.out.println(n1 + n3);
      }
      else if (n1 == n3)
      {
         System.out.println(n2 + n3);
      }
      else
      {
         System.out.println(n1 + n2 + n3);   
      }
   }
}
```