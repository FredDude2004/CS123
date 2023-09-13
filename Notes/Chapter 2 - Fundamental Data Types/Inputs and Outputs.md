# Inputs and Outputs
[Input and Output](https://books.trinket.io/thinkjava2/chapter3.html) <br>
[Storing User Input in Variables](https://runestone.academy/ns/books/published/csjava/Unit1-Getting-Started/topic-1-4-assignment.html#storing-user-input-in-variables)
## Code Examples
### Output Formating 1
```java
public class OutputFormatting1
{
   public static void main(String[] args)
   {
      int n1 = 1;
      int n2 = -22;
      int n3 = 333;
      int n4 = -44555;
      int n5 = 5;
      int n6 = -66;

      System.out.print(n1+"\n");
      System.out.print(n2+"\n");
      System.out.println(n3);
      System.out.println(n4);
      System.out.println(n5);
      System.out.println(n6);
      
      System.out.println();

      System.out.printf("% 6d\n", n1);
      System.out.printf("% 6d\n", n2);
      System.out.printf("% 6d\n", n3);
      System.out.printf("% 6d\n", n4);
      System.out.printf("% 6d\n", n5);
      System.out.printf("% 6d\n", n6);
   }
}
```
### Output Formating 2
```java
public class OutputFormatting2
{
   public static void main(String[] args)
   {
      double x1 = 1_234.56789;
      double x2 = -9_876_543_210.0123456789;

      System.out.println(x1);
      System.out.println(x2);  // Java uses scientific notation
      System.out.println();
      
      System.out.printf("%0+,19.4f\n", x1);
      System.out.printf("%0+,19.4f\n", x2);
      System.out.println();
   }
}
```

### Scanner Input
```java
/*
   nextInt()      Reads the next "token" as an integer.
   nextDouble()   Reads the next "token" as a double.
   next()         Reads the next "token".
   nextLine()     Reads the rest of the current line.

A "token" is a consecutive sequence of non "whitespace" characters.

The "whitespace" characters are ' ', '\n', '\t' (space, newline, tab).
*/

import java.util.Scanner;

public class ScannerInput
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);

      int n = in.nextInt();
      double d = in.nextDouble();
      String s1 = in.next();
      String s2 = in.nextLine();
   }
}
```

