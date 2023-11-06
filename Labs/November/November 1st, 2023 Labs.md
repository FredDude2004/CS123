# November 11th, 2023 Labs

## Lab 1
In the code given below, complete the definition of the static method called drawRectangle so that it prints a rectangle made up of * characters with the appropriate number of rows and columns.

The given main method calls your version of drawRectangle. You should not make any changes to the main method. It reads two input numbers and then uses them as parameters to your drawRectangle.

So, for example, if the two input numbers to main are 3 and 5, then your drawRectangle should print this rectangle.
<pre>
*****
*****
*****
</pre>
If the two input numbers to main are 5 and 9, then your drawRectangle should print this rectangle.
<pre>
*********
*********
*********
*********
*********
</pre>

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      
      int n = in.nextInt();
      int m = in.nextInt();
      
      drawRectangle(n, m);
   }
   
   
   /**
      Print a rectangle, made of '*' characters,
      with a rows and b columns.

      @param a  number of rows
      @param b  number of coluuns
   */
   public static void drawRectangle(int rows, int columns)
   {
      for (int i = 1;  i <= rows; i++) {
         for (int j = 1; j <= columns; j++) {
            System.out.print("*");
         }
         System.out.println();
      }
      return;
   }
}
```

## Lab 2
Fix the program given below so that it compiles and then passes all of its tests.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      double x = in.nextDouble();
      System.out.println( twoTimes(x) );
      System.out.println( triple(n) );
      System.out.println( addThem(n, x) );
      System.out.println( addThem(triple(n), twoTimes(x)));
   }


   /**
      Return twice the value of the input.

      @param x  decimal number to be doubled
      @return twice the value of x
   */
   public static double twoTimes(double x)
   {
      return 2.0 * x;
   }


   /**
      Return triple the value of the input.

      @param n  integer to be tripled
      @return triple the value of n
   */
   public static int triple(int n)
   {
      return 3 * n;
   }


   /**
      Add two input numbers.

      @param d  decimal input number
      @param i  integer input number
      @return the sum of d and i
   */
   public static double addThem(int d, double i)
   {
      return i + d;
   }
}
```

## Lab 3

Add to the program below a static method called triangle that takes two parameters, an int parameter n and a char parameter c.

The method triangle should do two things. It should print a picture of a triangle with n rows, the first row having one character c and the last row having n characters c.

The triangle method should also return the number of characters it printed in the triangle picture.

The program below has a main method that tests your triangle method. You should not modify the main method. The main method reads an input integer and an input character and uses them to call triangle.

If the input integer to the program is 5 and the input character is '$', then the out of the program should look like this.
<pre>
$
$$
$$$
$$$$
$$$$$

There are 15 $'s in the triangle.
</pre>

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      char c = in.next().charAt(0);
      int num = triangle(n, c);
      System.out.println();
      System.out.println("There are " + num + " " + c + "'s in the triangle.");
   }
   
   
   /**
      Write the definition for the triangle method.

      @param n  number of rows in the triangle picture
      @param c  char to use in the triangle picture
      @return the number of characters printed in the triangle picture
   */
   
   public static int triangle(int rows, char c)
   {
      int count = 0;
      for (int i = 1; i <= rows; i++) 
      {
         for (int j = 1; j <= i; j++) 
         {
            System.out.print(c);
            count++;
         }
         System.out.println();
      }
      return count;
   }
}
```