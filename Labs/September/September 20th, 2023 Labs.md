# September 20th, 2023 Labs
## Lab 1 
```java 
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      double n1 = in.nextDouble();
      double n2 = in.nextDouble();
      double n3 = in.nextDouble();
      
      if (n1 + n2 < n3)
      {
         System.out.println("not enough");   
      }
      else 
      {
         System.out.println("good enough");   
      }
      
   }
}
```
## Lab 2 
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      
      if (n < 5)
      {
         System.out.println("apple");   
      }
      else if (n == 5)
      {
         System.out.println("pear");
      }
      else // if n > 5 
      {
         System.out.println("orange");   
      }
      
   }
}
```
## Lab 3 
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n1 = in.nextInt();
      int n2 = in.nextInt();
      
      if (n1 >= 0)
      {
         if (n2 >= n1)
         {
            System.out.println("outside");
         }
         else if (n2 < n1)
         {
            System.out.println("inside");   
         }
      }
      else 
      {
         if (n2 < n1)
         {
            System.out.println("outside");   
         }
         else if (n2 >= n1)
         {
            System.out.println("inside");   
         }
      }
      
   }
}
```
## Lab 4 
```java
public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n1 = in.nextInt();
      
      if (n1 < 0)
      {
         if (n1 < -10)
         {
            System.out.println("pear");   
         }
         else
         {
            System.out.println("apple");   
         }
      }
      else if (n1 >= 0)
      {
      if (n1 <= 3)
      {
         System.out.println("orange");   
      }
      else if (n1 < 6) 
      {
         System.out.println("grape");
      }
      else if (n1 <= 10)
      {
         System.out.println("dog");
      }
      else
      {
         System.out.println("grape");   
      }
   }  
   }
}
```