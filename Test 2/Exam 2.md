
             CS 12300 Exam 2 Review

The exam is on Wednesday, November 8.

The exam is over Chapters 4 and 5 from the textbook, https://learn.zybooks.com/zybook/PNWCS12300Fall2023

The most important ideas from those chapters are in these sections.
   Sections 4.1, 4.4, 4.6, 4.10, 4.13, 4.28.
   Sections 5.2, 5.3, 5.4, 5.5, 5.7.



Here are a few review problems.


Problem 1) What does the following code fragment print out?
Briefly explain why.

   String s = "************";
   int i = 0;
   while ( i < s.length() )
   {
      System.out.println( s.substring( i++ ) );
   }
   while ( i > 0 )
   {
      System.out.println( s.substring( --i ) );
   }




Problem 2) Write a single (not nested) for-loop that uses substrings
of these two strings,

   String s1 = "************";
   String s2 = "            ";

to create the following 12 lines of output.
************
 ***********
  **********
   *********
    ********
     *******
      ******
       *****
        ****
         ***
          **
           *




Problem 3) Let s be the following string of nine spaces.

   String s = "         ";

For each part below, write a single (not nested) for-loop that
uses substrings of s to create the given picture.

a) Create the following ten lines of output.
         *
        *
       *
      *
     *
    *
   *
  *
 *
*

b) Create the following ten lines of output.
*
 *
  *
   *
    *
     *
      *
       *
        *
         *

c) Create the following six lines of output.
*         *
 *       *
  *     *
   *   *
    * *
     *




Problem 4) Write a code fragment, using nested for-loops, whose output
will look like the following.
(Hint: Don't try to compute the output numbers from the loop indices.
To get the output numbers, just have a counter variable that counts up
from 10, and print out the counter.)

10
11 12
13 14 15
16 17 18 19
20 21 22 23 24
25 26 27 28 29 30
31 32 33 34 35 36 37
38 39 40 41 42 43 44 45




Problem 5) Write nested for-loops to produce the following output.
Your for-loops only need to produce exactly these seven lines (your
for-loops can use "magic numbers", there is no size parameter).

      6
     55
    444
   3333
  22222
 111111
0000000




Problem 6) Write a code fragment that prints a pattern based
on a variable called "size" where the pattern looks like this,

|/\|/\|/\|/\|/\|/\|/\|/\|

when the variable size has the value 8, and the pattern looks
like this,

|/\|/\|

when size has the value 2. You should be able to write this
fragment two ways. Why?




Problem 7) Write nested for-loops that print a pattern based
on a variable called "size". When the variable size has the
value 8, the pattern looks like this.

*******************
*        *       *
*        *      *
*        *     *
*        *    *
*        *   *
*        *  *
*        * *
*        **
**********

When the variable size has the value 3, the pattern looks like this.

*********
*   *  *
*   * *
*   **
*****

When the variable size has the value 4, the pattern looks like this.

***********
*    *   *
*    *  *
*    * *
*    **
******




Problem 8) What is printed out by the following program segment?

   for (int i = 0; i < 4; ++i)
   {
      for (int j = 0; j < 5; ++j)
      {
         if ( (i+j) % 2 == 0 )
         {
            System.out.print("0 ");
         }
         else
         {
            System.out.print("1 ");
         }
      }
      System.out.print("\n");
   }




Problem 9) Here are two code fragments. Below them are three pictures.
These fragments draw two of the three pictures. Determine which fragment
draws which picture. Explain your answer by detailing which part of the
if-statements draw which part of the pictures. Be very specific about how
you can tell which fragment draws which picture. (In each code fragment,
assume that n is an odd integer.)


// Assume that n is odd.                     // Assume that n is odd.
for (int i = 1; i <= n; ++i)                 for (int i = 1; i <= n; ++i)
{                                            {
  for (int j = 1; j <= n; ++j)                 for (int j = 1; j <= n; ++j)
  {                                            {
     if ( i == 1 || i == n                        if ( i == 1 || i == n
       || j == 1 || j == n                          || j == 1 || j == n
       || (i==(n/2)+1 && j>=(n/2)+1)                || (i==(n/2)+1 && j<=(n/2)+1)
       || (i==j && i<=(n/2)+1) )                    || (i==j && i>=(n/2)+1) )
     {                                            {
        System.out.print("*");                       System.out.print("*");
     }                                            }
     else                                         else
     {                                            {
        System.out.print(" ");                       System.out.print(" ");
     }                                            }
  }                                            }
  System.out.println();                        System.out.println();
}                                            }


***************        ***************        ***************
*             *        **            *        *      *      *
*             *        * *           *        *      *      *
*             *        *  *          *        *      *      *
*             *        *   *         *        *      *      *
*             *        *    *        *        *      *      *
*             *        *     *       *        *      *      *
********      *        *      ********        *      *      *
*       *     *        *             *        *       *     *
*        *    *        *             *        *        *    *
*         *   *        *             *        *         *   *
*          *  *        *             *        *          *  *
*           * *        *             *        *           * *
*            **        *             *        *            **
***************        ***************        ***************




Problem 10) In the following program, complete the definition of the
main method so that the program, when it is run, would produce the
following output.

*
 *
  *
   *
    *
12345-12345-12345-12345-12345-12345-12345-12345-12345-12345-12345-12345-12345-12345-
    *
   *
  *
 *
*


public class Problem6
{
   public static void methodA()
   {
      System.out.print("12345");
   }
   public static void methodB()
   {
      System.out.println("    *");
      System.out.println("   *");
      System.out.println("  *");
      System.out.println(" *");
      System.out.println("*");
   }
   public static void methodC()
   {
      System.out.println("*");
      System.out.println(" *");
      System.out.println("  *");
      System.out.println("   *");
      System.out.println("    *");
   }
   public static void main(String[] args)
   {




   }
}




Problem 11) Fill in the blanks so that the following method
definition is correct.

   public static  ________  max2( _______ a, int ______ )
   {
      if ( ______ >= ______ )
      {
         return _______ ;
      }
      else
      {
         _______ b;
      }
   }




Problem 12) Fill in the blanks so that the following method
definition is correct.

   public static  ________  min2( _______ a, double ______ )
   {
      _______ result;

      if ( a - b < ______ )
      {
         result = _______ ;
      }
      else
      {
         result =  b;
      }

      return result;
   }




Problem 13) The following method takes a String value as its input
and the method returns a new String value as its output. How does
the output String compare with the input String? Give a few examples.

   public static String mystery(String str)
   {
      String result = "";
      for (int i = 0; i < str.length(); ++i)
      {
         if ( ' ' != str.charAt(i) )
         {
            result = result + str.charAt(i);
         }
      }
      return result;
   }




Problem 14) Write a complete definition for a public static method
called closeEnough that takes a double and an integer and returns true
if the double is within one unit of the integer. For example

   closeEnough(3.9, 5)  ->  false
   closeEnough(4.1, 5)  ->  true
   closeEnough(6.0, 5)  ->  true
   closeEnough(6.1, 5)  ->  false




Problem 15) Write a definition for a public static void method that
has a parameter called size and prints a line with 1+size number of
characters on the line and with the first character being an asterisk,
the last character being an equal sign, and the rest of the characters
being ampersands.




Problem 16) The following method contains a single error.
Describe the error and show how to fix it.

   public static boolean isMillionaire(int netWorth)
   {
      if (netWorth >= 1000000)
      {
         return true;
      }
   }




Problem 17) The body of the following method has three statements.
Rewrite the body so that it has just a single statement which is
the simplest statement that will work. (Hint: When does the
method return true and when does the method return false?)

   public static boolean isInside(int n)
   {
      boolean inside = false;
      if (0 < n && n < 100){ inside = true; }
      return inside;
   }