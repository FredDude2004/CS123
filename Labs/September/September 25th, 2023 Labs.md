
# September 25th, Labs

## Lab 1 
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String word = in.next();
      
      if (word.equals("a") || word.equals("e") || word.equals("i") || word.equals("o") || word.equals("u")) 
      {
         System.out.println("vowel");   
      }
      else
      {
         System.out.println("not a vowel");   
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
      
      int int1 = in.nextInt();
      int int2 = in.nextInt();
      int int3 = in.nextInt();
      
      if (int1 != int2 && int1 != int3 && int2 != int3)
      {
         System.out.print(0);   
      }
      else if (int1 == int2 && int1 == int3)
      {
         System.out.print(3); 
      }
      else 
      {
         System.out.print(2);   
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
      
      int month1 = in.nextInt();
      int day1 = in.nextInt();
      int month2 = in.nextInt();
      int day2 = in.nextInt();
      
      if (month1 == month2 && day1 == day2)
      {
         System.out.println("equal");   
      }
      else if (month1 < month2 || month1 == month2 && day1 < day2)
      {
         System.out.println("before");   
      }
      else
      {
         System.out.println("after");   
      }
   }
}
```