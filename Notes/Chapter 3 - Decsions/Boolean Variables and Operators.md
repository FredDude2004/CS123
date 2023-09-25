# Boolean Variables and Operators
Boolean operators help us write more complicated 'if' statments

Say we wanted to test if a variable is in between two numbers, in algebra we would write something like this 
32 < t < 212 (water is in liquid form if it is in between 32 F and 212 F)
This is basically saying that the variable 't' is in between 32 and 212, Java doesn't understand this notation so we have to make it a little but more complicated 

```java
if (t > 32 && t < 212)
{
    System.our.println("liquid");
}
```

We have to use the Boolean 'and' operator which in java is '&&'

We can also use the 'or' operator which tests if one or the other or both are on. In java or is denoted by | |

```java
if (t <= 32 || 212 <= t)
{
    System.out.println("not liquid");
}
```
This tests if t is less than or equal to 32 or if t is < or equal to 212

The last Boolean operation is the 'not' operator which is denoted in java by an exclam '!'

```java 
if !(32 < t && t < 212)
{
    System.out.println("not liquid");
}
```
This program and the last one do the exact same thing 


## Truth Table for the Boolean Operator 
- && reports true if both cases are true <br>
- | | Reports true if either cases are true <br>
- 'Excluseive Or' denoted by ^ only reports true if only one of the cases is true
- ! reports true if the operation is false, 
 ![Truth Tables](https://www.realdigital.org/img/228d4788d26e286b5706f6d644ddee8b.svg)

 ## Examples of Boolean Operators 
 ```java 
 import.java.util.Scanner;
 public class Compare2
 {
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);

        double x = in.nextDouble();
        double y = in.nextDouble();

        if (x == y)
        {
            System.out.println("They are the same.");
        }
        else // x != y
        {
            System.out.print("The first number is ");
            if (x > y)
            {
                System.out.println("larger");
            }
            else
            {
                System.out.println("smaller");
            }
            if (-0.01 < x - y && x - y < 0.01)
            {
                System.out.println("The numbers are close together");
            }
            if (x == y + 1 || x == y -1)
            {
                System.out.println("The numbers are one apart");
            }
            if (x > 0 && y > 0 || x < 0 && y < 0)
            {
                System.out.println("The numbers have the same sign");
            }
            else
            {
                System.out.println("the numbers have different signs");
            }
        }
    }
 }
 ```
 Suppose you wanted to write a program that prints green or red depending on where a variable is on the number line, 
  <pre>
      2       4     6       8 
<-----[-------]-----[-------]------>
  red   green   red   green   red </pre>
  
before we had to use a lot of 'if' and 'else if' statments to do this, but with Boolean operators we can do it very simply . . . 

```java
if (2 <= 4 && <= 4 || 6 <=x && x <= 8)
{
    System.out.println("green");
}
else
{
    System.out.println("red");
}
```
Like this, <br> or . . . 
```java
if (x < 2 || 4 < x && x < 6 || x > 8)
{
    System.out.println("red");
}
else 
{
    System.out.println("green");
}
```
This