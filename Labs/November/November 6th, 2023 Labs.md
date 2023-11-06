# November 6th, 2023 Labs

## Lab 1 
In the program below, define a static method called hyphenate that takes one String parameter and returns a String value.

The string returned by hyphenate should be made up of all the characters from the input string but with a hyphen character, '-', placed between every two characters.

So, for example,
<pre>
hyphenate("hellothere")
</pre>
whould return the string

<pre>
h-e-l-l-o-t-h-e-r-e
</pre>
Hint: This is another "fencepost" problem.

The program below contains a main method that tests your definition of the hyphenate method. Do not make any changes to the main method.

```java
import java.util.Scanner;

public class Main
{
   /**
      Hyphenate all the characters of a string.
      
      @param str  the String to hyphenate
      @return the hyphenated version of str
   */
   public static String hyphenate(String str)
   {
      String finale = "";
      for (int i = 0; i < str.length() - 1; i++)
      {
         finale += str.charAt(i) + "-"; 
      }
      finale += str.charAt(str.length() - 1);
      
      return finale;
   }

   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String input = in.nextLine();
      String output = hyphenate(input);
      System.out.println(output);
   }
}
```

## Lab 2
In the program below, define a public static method called repeatWords that has two String parameters word1 and word2 and an int parameter n and that returns a String value.

The method should return the string made up of word1 repeated n times with word2 between each of the repititions of word1.

For example,
<pre>
repeatWords("pear", "X", 3)
</pre>
should return the string
<pre>
"pearXpearXpear"
</pre>
And
<pre>
repeatWords("X", "pear", 4)
</pre>
should return the string
<pre>
"XpearXpearXpearX"
</pre>
And
<pre>
repeatWords("apple", "pear", 1)
</pre>
should return the string
<pre>
"apple"
</pre>
The program below has a main method that tests your version of swapChars. Do not make any changes to the main method.
```java
import java.util.Scanner;

public class Main
{
   /**
      A method that repeats a word with another word between the repitition.
      
      @param word1  a String that will be repeated n times
      @param word2  a String that goes between the repititions of word1
      @parame n   the number of times to repeat word1
      @return word1 repeated n times with word2 between the repititions
   */
   public static String repeatWords(String word1, String word2, int n)
   {
      String finish = "";
      if (0 < n)
      {
         for (int i = 1; i < n; i++)
         {
            finish += (word1 + word2);
         }
         finish += (word1);
      }  
      return finish;
   }
   
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String input1 = in.next();
      String input2 = in.next();
      int n = in.nextInt();
      String output = repeatWords(input1, input2, n);
      System.out.println(output);
   }
}
```

## Lab 3
In the program below, define a public static method called weirdMult that has an int input n and a double input x and returns the double value that is n times the fraction part of x.

For example,
<pre>
weirdMult(2, 1.3)
</pre>
should return
<pre>
0.6
</pre>
And
<pre>
weirdMult(3, 5.7)
</pre>
should return
<pre>
2.1
</pre>
The program below has a main method that tests your version of weirdMult. Do not make any changes to the main method.

```java
import java.util.Scanner;

public class Main
{
   /**
      Multiply an integer with the fractional part of a double.

      @param n an int
      @param x a double
      @return the double that is the product of n with the fractional part of x
   */
   public static double weirdMult(int n, double x)
   {
      double decimal = x - (int)x;
      return n * decimal;
   }
   
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      double x = in.nextDouble();
      double y = weirdMult(n, x);
      System.out.println(y);
   }
}
```

## Lab 4 
In the program below there is a methodA a methodB, a methodC, and a main methhod. Do not change any of these methods.

Fill in the definition of the method yourMethod so that it uses methodA, methodB, and methodC to print a pattern of size n.

If n has the value 3, then the pattern looks like this.
<pre>
>
1>
11>
111>
11>
1>
>
2>
22>
222>222>
22>
2>
>
3>
33>
333>333>333>
33>
3>
>
</pre>
If the value of the parameter n is 2, then the pattern looks like this.
<pre>
>
1>
11>
111>
11>
1>
>
2>
22>
222>222>
22>
2>
>
</pre>

```java
import java.util.Scanner;

public class Main
{
   /**
      Define this method to print the pattern described above.
   */
   public static void yourMethod(int n)
   {
      for (int i = 1; i <= n; i++)
      {
         methodC(i);
         for (int j = 1; j <= i; j++)
         {
            methodA(i);
         }
         System.out.println();
         methodB(i);
      }
      System.out.println(">");
   }



   public static void methodA(int a)
   {
      System.out.print("" + a + a + a + ">");
   }

   public static void methodB(int a)
   {
      System.out.println("" + a + a + ">");
      System.out.println("" + a + ">");
   }

   public static void methodC(int a)
   {
      System.out.println(">");
      System.out.println("" + a + ">");
      System.out.println("" + a + a + ">");
   }

   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      yourMethod(n);
   }
}
```