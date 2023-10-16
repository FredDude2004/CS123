# October 16th, 2023 Labs
## Lab 1 
Write a program that reads a sequence of positive integers until it gets a negative sentinel value. Then your program should read another sequence of positive integers until it gets another negative sentinel value. Your program should print out the quotient of the sum of the first sequence with the sum of the second sequence (not including the sentinel values).

So, for example, if the input is
<pre>
1 2 3 -1 4 5 -2
</pre>
then your program should print out
<pre>
0.6666666666
</pre>
which is (1+2+3)/(4+5).
If the input is
<pre>
5  4  3  2  1  -4  1  0  1  0  1  -2
</pre>
then your program should print out
<pre>
5.0
</pre>
which is (5+4+3+2+1)/(1+1+1) = 15/3.
```java
import java.util.Scanner;

public class Main 
{
   public static void main(String[] args) 
   {
      Scanner in = new Scanner(System.in);
      double sum1 = 0;
      double sum2 = 0;
      
      for (int i = in.nextInt(); i >= 0; i = in.nextInt())
      {
         sum1 = sum1 + i;
      }
      for (int i = in.nextInt(); i >= 0; i = in.nextInt())
      {
         sum2 = sum2 + i;
      }
      
      System.out.println(sum1 / sum2);
   }
}
```
## Lab 2 

Write a program that reads words until it reads the sentinel word "stop". Your program should print the total number of characters in all the words that it read except for the sentinel word "stop".

For example, if the input is
<pre>
one apple two pears three grapes stop
</pre>
then your program should print the number
<pre>
27
</pre>
```java
import java.util.Scanner;

public class Main 
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String word = in.next();
      int sum = 0;
      while (!(word.equals("stop")))
      {
         sum = sum + word.length();
         word = in.next();
      }
      
      System.out.print(sum);
   }
}
```
## Lab 3 

Write a program that reads one line of input as a (single) String value and then prints, on one line, the input string but with every space character replaced by a period character.

For example, if the input is the line
<pre>
One two three, then some more words.
</pre>

then your program should print
<pre>
One.two.three,.then.some.more.words.
</pre>
If the input is the line
<pre>
This  line  has  double  spaces  every  where  except here!
</pre>
the your program should print
<pre>
This..line..has..double..spaces..every..where..except.here!
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String s = in.nextLine();
      
      for (int index = 0; index < s.length(); index++)
      {
         if (s.charAt(index) == ' ')
         {
            System.out.print('.');
         }
         else
         {
            System.out.print(s.charAt(index));
         }
      }
      System.out.print("\n");
   }
}
```
## Lab 4 
Write a program that reads words until it reads the sentinel word "stop". For each word that your program reads, your program should print the number of vowels that are in the word (for this problem, the vowels are a, e, i, o, u).

For example, if the input is
<pre>
apple  pears  plums  orange  watermelon stop
</pre>
then your program should print
<pre>
2
2
1
3
4
</pre>
```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      String s = in.next();
      int v = 0;
      
      while (!(s.equals("stop")))
      {
         v = 0;
         for (int index = 0; index < s.length(); index++)
         {
            char c = s.charAt(index);
            if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u')
            {
               v++;
            }
         }
         System.out.println(v);
         s = in.next();
      }
   }
}
```