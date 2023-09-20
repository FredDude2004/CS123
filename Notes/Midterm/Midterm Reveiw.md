# Midterm Reveiw

     CS 12300-001 Exam 1 Review

### The exam is on Wednesday, October 4.

#### The exam is over the following sections:

[Section 1.3 Variables and Data Types](https://runestone.academy/ns/books/published/csjava/Unit1-Getting-Started/topic-1-3-variables.html) <br>
[Section 1.4 Expressions and Assignment Statements](https://runestone.academy/ns/books/published/csjava/Unit1-Getting-Started/topic-1-4-assignment.html) <br>
[Chapter 2 Variables and Operators]( https://books.trinket.io/thinkjava2/chapter2.html) <br>
[Chapter 3 Input and Output](https://books.trinket.io/thinkjava2/chapter3.html) <br>
[Sections 2.1 through 2.7](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-1-objects-intro-turtles.html )<br>
[Chapter 3 Decisions]( https://learn.zybooks.com/zybook/PNWCS12300Fall2023)


Here are a few review problems.

## Problem 1
 What does the following program print out when it is run?
If there are any blank lines in the output, be sure to clearly state that.
```java
   public class Program1
   {
      public static void main(String[] args)
      {
         System.out.print( "*" );
         System.out.print( "*\n" );
         System.out.println( "***" );
         System.out.print( "**\n*" );
         System.out.println( "*" );
      }
   }
```

## Problem 2
What does the following program print out when it is run?
If there are any blank lines in the output, be sure to clearly state that.
```java
   public class Program2
   {
      public static void main(String[] args)
      {
         System.out.print( "*" );
         System.out.print( "*\n" + "**" );
         System.out.println( "*\"*\"" );
         System.out.print( "\n**\n*" );
         System.out.println( "\\*\\" );
      }
   }
```



## Problem 3
Suppose that
```java
   String s = "one two three four";
```
What is the value for each of the following expressions?

(a)  s.substring(0, 4).length() + s.substring(8, 13).length() <br>
(b)  (s.substring(0, 4) + s.substring(8, 13)).length()<br>
(c)  s.substring(4, 7) + s.charAt(8) + s.charAt(14) <br>
(d)  s.substring(3, 8).length()<br>
(e)  s.substring(0, 3) + "2" + s.substring(8) <br>
(f)  s.substring(4, 5).toUpperCase() + s.substring(5, 7) <br>



## Problem 4
What should be the data type for the variable x and the data
type for the variable y in order that the following two lines of code
compile correctly (enter the data type into the blank space in the
variable's declaration). Also, what will be the value of y after the
two lines are executed? Briefly explain your answer.
```java
   ______ x = "2" + 2;

   ______ y = x + 2;
```



## Problem 5
 Assume that.
 ```java
   int x =   1;
   int y =  -3;
   int z = 101;
 ```
 
What is the type and value for each of the following expressions?

(a)   3 * z - y / x <br>
(b)   (2.0 + x) / (1 - y) <br>
(c)   x + 2 <= y <br>
(d)   x + y + "z" <br>
(e)   x + (y + "z") <br>



## Problem 6
 Suppose the String variable ssn holds a social security number
in the form "xxx-xx-xxxx". Define a String variable ssn2 whose value is the
last four digits of the social security number contained in ssn.



## Problem 7
 Suppose the String variable pn is a 10-digit phone number in
the form "xxxxxxxxxx". Define a String variable pn2 whose value is the phone
number contained in pn converted into the format "(xxx) xxx-xxxx". So, as
an example, the String "2199892273" should be converted to "(219) 989-2273".



## Problem 8
Suppose that a String variable d is a date in the European format
"dd.mm.yyyy". Define a String variable d2 whose value is the date contained
in d converted into the format "mm-dd-yyyy". So, as an example, the String
"29.10.2016" should be converted to "10-29-2016".



## Problem 9
 If the input to this Java program,
```java
import java.util.Scanner;
public class ScannerQuestion
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);

      String s1 = in.next();
      String s2 = in.nextLine();
      int n1 = in.nextInt();
   }
}
```

is these three lines,

123 <br>
456 <br>
789 <br>

then what are the values in the variables s1, s2, and n1?
Briefly explain why.



## Problem 10
 Give the output of the following program segment if:
(a)  x=1 and y=1,
(b)  x=2 and y=2.
```java
   if (x > 1)
   {
      if (y > 2)
      {
         System.out.println(2*x - y);
      }
      else
      {
         System.out.println(2*x + y);
      }
   }
   else
   {
      if (y > 2)
      {
         System.out.println(x - y);
      }
      else
      {
         System.out.println(x + y);
      }
   }

```



## Problem 11
 Explain all the possible values that the variable w can
have after the following code is executed. Assume that u and v are
int's defined elsewhere in the program.

   int w = 0;
   if (u > 0) w++;
   if (v > 0) w++;



## Problem 12
Explain all the possible values that the variable w can
have after the following code is executed. Assume that u and v are
int's defined elsewhere in the program.

   int w = 0;
   if (u > 0)
   {
      w++;
   }
   else if (v > 0)
   {
      w++;
   }



## Problem 13
 Consider the following code fragment.
```java
   if ( p < 0 )  { System.out.println( "p is negative" ); }
   if ( p == 0 ) { System.out.println( "p is zero" ); }
   if ( p > 0 )  { System.out.println( "p is positive" ); }
```

Rewrite this code fragment using an if-elseif-else-statement.




## Problem 14
 What is printed out by the following code fragment?
```java
   int n = 15;
   if ( n >= 10 && n <= 20 )
   {
      System.out.println( "A" );
   }
   else
   {
      System.out.println( "B" );
   }
   if ( n < 10 || n < 20 )
   {
      System.out.println( "C" );
   }
   else
   {
      System.out.println( "D" );
   }
   if ( !(n < 100) )
   {
      System.out.println( "E" );
   }
   if ( (n == 25) || (n != 15) )
   {
      System.out.println( "F" );
   }
   if ( !( (n != 100) && (n < 50) ) )
   {
      System.out.println( "G" );
   }
   else
   {
      System.out.println( "H" );
   }

```



## Problem 15
What is printed out by the following code fragment?
Also, indicate which of the following boolean operators get short circuited? <br> 
See [Section 3.16](https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/16)
and [Section 3.42](https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/42)
in the textbook.
```java
   boolean b1 = true;
   boolean b2 = false;
   if ( b1 || !b1 )
   {
      System.out.println("One.");
   }
   if ( !b1 && b1 )
   {
      System.out.println("Two.");
   }
   if ( !b2 && b1 )
   {
      System.out.println("Three.");
   }
   if ( !(b1 || !b2) )
   {
      System.out.println("Four.");
   }
   if ( !(b1 && b2) )
   {
      System.out.println("Five.");
   }
   if ( (!b2 || b1) && b1 )
   {
      System.out.println("Six.");
   }
```



## Problem 16
 Find and correct the error in the following if-statement.
```java
   if ( 0 <= x <= 5 )
   {
      System.out.println( "x is between 0 and 5" );
   }

```



## Problem 17
 Find and correct the error in the following if-statement.
```java
   if ( x && y == 0 )
   {
      System.out.println( "x and y are both zero" );
   }

```



## Problem 18
 Explain what the following program segment does.
Then add a pair of braces so that what the resulting code
prints out is always correct.
```java
   if ( x == y )
      if ( x == 0 )
         System.out.println("x and y are both zero");
      else
         System.out.println("x and y are not equal");

```

Hint: See [Participation Activity 3.10.3](
https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/10?content_resource_id=68552714)
and [Common Error 3.10.1](https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/3/section/10?content_resource_id=78475302
)


## Problem 19
Suppose that n is a number that must be between 0 and 50.Rewrite the following nested if-else-statement so that it does the
same thing but is easier to understand. (Hint: Use a number line to
figure out what this code is doing.)

```java
   if ( n > 40 )
   {
      System.out.println( "plum" );
   }
   else if ( n <= 10 )
   {
      System.out.println( "apple" );
   }
   else if ( n > 30 )
   {
      System.out.println( "pear" );
   }
   else if ( n <= 20 )
   {
      System.out.println( "banana" );
   }
   else
   {
      System.out.println( "grape" );
   }
```
## Problem 20
What is wrong with the following program?
Describe the error and show a way to fix it.
```java
   import java.util.Scanner;
   public class Program19
   {
      public static void main(String[] args)
      {
         Scanner in = new Scanner(System.in);
         int age = in.nextInt();
         boolean adult;
         if (age < 21)
         {
            adult = false;
         }
         System.out.println(adult);
      }
   }
```

## Problem 21

 Simplify the code in the following program as much as you can.
(Hint: Use a number line to determine what are the mutually exclusive cases.)
```java
   import java.util.Scanner;
   public class Program20
   {
      public static void main(String[] args)
      {
         Scanner in = new Scanner(System.in);
         double n = in.nextDouble();

         if (n < 0)
         {
            System.out.println( -1 );
         }
         else if (0 <= n && n <= 1)
         {
            System.out.println( 0 );
         }
         else if (n > 1)
         {
            System.out.println( 1 );
         }
         else
         {
            System.out.println( 42 );
         }
      }
   }
```
