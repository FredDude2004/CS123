# Else If Statement 

```java
if (condition that is wither true or false) // a boolean expression
{
    // what to do if he condition is true
}
else if (another condition that is either true or false)
{
    // what to do if that condition is true 
}
else if (another condition that is either true or false)
{
    // what to do if that condition is true 
}
else
{
    // what to do if none of the conditions are true 
}
```
The else if statement gives you another condition that you can use in an if statment, you can use as many 'else if's as you want in a single if statment 

## Richter Scale 
[Section 3.8 zyBooks](https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/8)

We saw how to program a two-way branch with an if statement. In many situations, there are more than two cases. In this section, you will see how to implement a decision with multiple alternatives.

For example, consider a program that displays the effect of an earthquake, as measured by the Richter scale

```java
import java.util.Scanner;

public class EarthquakeStrngth
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      double richter = in.nextDouble();
      
      if (richter >= 8.0)
      {
         System.out.println("Most structures fall");
      }
      else if (richter >= 7.0)
      {
         System.out.println("Many buildings destroyed");
      }
      else if (richter >= 6.0)
      {
         System.out.println("Many buildings considerably damaged, some collapse");
      }
      else if (richter >= 4.5)
      {
         System.out.println("Damage to poorly constructed buildings");
      }
      else 
      {
         System.out.println("No destruction of buildings");
      }
   }
}
```

