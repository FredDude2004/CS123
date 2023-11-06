# 9/13/2023 Labs

## Lab 1 
```java
/*
   Write a program that reads three integers.

   If the sum of the first two integers is equal
   to the third integer, output "You win".

   If the sum of the first two integers is less
   than the third integer, output "You lose".

   If the sum of the first two integers is greater
   than the third integer, output "Try again".
*/
import java.util.Scanner;
public class Game
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      int n3 = in.nextInt();
      
      if (n1 + n2 == n3)
      {
         System.out.println("You win");
      }
      if (n1 + n2 < n3)
      {
         System.out.println("You lost");
      }
      if (n1 + n2 > n3)
      {
         System.out.println("Try again");
      }  
   }
}
```
## Lab 2
```java
/*
   Write a program that reads two words and
   prints out the longer of the two words but
   shortened to the length of the shorter of
   the two words.
   
   If the two words are "bird" and "orange"
   the output should be "oran".
*/
import java.util.Scanner;
public class Truncate
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      String word1 = in.next();
      String word2 = in.next();
      String word3;
      
      int n1 = word1.length();
      int n2 = word2.length();
      
      if (n1 > n2)
      {
         word3 = word1.substring(0,n2);
      }
      
      else (n1 < n2)
      {
         word3 = word2.substring(0,n1);
      }    
      System.out.println(word3);
   }
}
```
## Lab 3
```java
/*
   Write a program that reads five integers.

   Print the first number.
   Print the second number if it is greater than the first number.
   Print the third number if it is greater than the last printed number.
   Print the fourth number if it is greater than the last printed number.
   Print the fifth number if it is greater than the last printed number.
*/
import java.util.Scanner;
public class Increasing
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      int n3 = in.nextInt();
      int n4 = in.nextInt();
      int n5 = in.nextInt();
      
      System.out.print(n1);
      int lastPrinted = n1;
      
      if (n2 > lastPrinted)
      {
         lastPrinted = n2;
         System.out.print(n2);
      }
      if (n3 > lastPrinted)
      {
         lastPrinted = n3;
         System.out.print(n3);
      }
      if (n4 > lastPrinted)
      {
         lastPrinted = n4;
         System.out.print(n4);
      }
      if (n5 > lastPrinted)
      {
         lastPrinted = n5;
         System.out.print(n5);
      }  
   }
}
```
## Lab 4
```java
/*
   Write a program that reads seven integers. Output the count
   of how many numbers are greater than the first number.
   
   If the input is
     3  7  4  0  6  3  8
   then the output should be 4.

   If the input is
     0  5  -1  10  -6  -3  0
   then the output should be 2.
   
*/
import java.util.Scanner;
public class Counting
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      int n3 = in.nextInt();
      int n4 = in.nextInt();
      int n5 = in.nextInt();
      int n6 = in.nextInt();
      int n7 = in.nextInt();
      int count = 0;
      
      if (n2 > n1)
      {
         count = count + 1;
      }
      if (n3 > n1)
      {
         count = count + 1;
      }
      if (n4 > n1)
      {
         count = count + 1;
      }
      if (n5 > n1)
      {
         count = count + 1;
      }
      if (n6 > n1)
      {
         count = count + 1;
      }
      if (n7 > n1)
      {
         count = count + 1;
      }
      
      System.out.println(count + " numbers are greater than " + n1);      
   }
}
```