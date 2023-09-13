# Expressions
## Using expressions to assign values to variables
[Here's a reading explaining expressions](https://runestone.academy/ns/books/published/csjava/Unit1-Getting-Started/topic-1-4-assignment.html)

## Notes
Every variable has
   1) name
   2) type
   3) value
   4) location

The type can be any of
   a) int
   b) double
   c) boolean
   d) String

The types int, double, boolean are called "primitive types".

The type String is called a "reference type".

The value for a variable can come from
   1) a literal
   2) an expression
   3) program input

   ### Example Code
```java
public class Examples1
{
   public static void main(String[] args)
   {
      int n = 2_000_000_000;
      double x = 5.2;
      boolean b = true;
      String s = "hello";
      int n2 = n;           // copy 2_000_000_000 into n2
      double x2 = x;        // copy 5.2 into x2
      boolean b2 = b;       // copy true int b2
      String s2 = s;        // copy the arrow in s into s2
      String s3 = "hello";  // a third reference to the same string
      String bob = "hello"; // a fourth reference to the same string
      double y = 2*x + 3;   // an expression
   }
}
   ```

An "expression" is the word we use for what algebra calls a "formula".
Expressions are made up of variables, literals, and operators.

The most basic operators are +, -, *, /, %.
The meaning of each operator depends on the type of its operands!

When we write
   x + y
we call + the operator, and x, y are the operands. What
the operator + does depends on the types of the x and y!
And for some types of x and y, x + y is an error (what
would be an example?).

## Example Code
```java
// Change the declaration of x from
//    int x = 5;
// to
//    boolean x = true;
// Where does the error show up?

// Change the declaration of x from
//    int x = 5;
// to
//    String x = "weird";
// What does this change do?

public class Examples2
{
   public static void main(String[] args)
   {
      int x = 5;       // change the declaration of x
      double y = 6.2;
      int z = 12;
      System.out.println( x + 3*y + z ); // An expression whose meaning
   }                                     // depends on the type of the vars
}
```
```java
public class IntegerQuotientAndRemainder 
{
   public static void main(String[] args)
   {
      System.out.println(97 / 25); // How many quarters are in 97 cents?
      System.out.println(97 % 25); // How many cents are left over?

      System.out.println(97 / 5); // How many nickels are in 97 cents?
      System.out.println(97 % 5); // How many cents are left over?

      System.out.println(127 / 8); // How many cups are in 127 oz?
      System.out.println(127 % 8); // How many oz are left over?

      System.out.println(1_234 / 12); // How many feet are in 1,234 inches?
      System.out.println(1_234 % 12); // How many inches are left over?
   }
}
```

Question: In the following expression, what are the
operands of the * operator?
   x * (3 + y)

Question: Is the following a true or false statement?
  "You cannot give the + operator a boolean operand."

