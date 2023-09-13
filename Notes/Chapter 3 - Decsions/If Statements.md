# If Statements 
the word "if" is a keyword in java

## What is an If Statment?
An if statement lets your program know whether or not it should execute a block of code. Comparison-based branching is a core component of programming. The concept of an if-else or switch block exists in almost every programming language.

```java
if (condition_that_is_either_true_or_false ) // a boolean expression
{
    // what to do if the condition is true
}
else
{
    // what to do if the condition is false
}
```
these are very common boolean expressions, and what can go inside of the if statment is very vast. For right now we will use different types of boolean expressions. 

## Boolean Expressions in Java
there aren't enough keys on the keyboard to allow for all of the boolean expressions so they have to get creative and make up representations of the boolean expression 

(<) : Less than <br>
(>) : Greater than <br>
(<=) : Less than or Equal to <br>
(>=) : Greater than or Equal to <br>
(==) : Here you are asking the question if these    two values are equal <br>
(!=) : Not equal

```java
import java.util.Scanner;

public class PositiveNegative
{
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);

        int n = in.nextInt();

        if (n >= 0) // a condition that is either true or false
        {
            // what to do if the condition is true
            System.out.println("posotive");
        }
        else
        {
            // what to do if the condition if false
            System.out.println("negative");
        }
        System.out.println("bye");
    }
}
```
This program will take in an inpute, and compare it to zero. Using the 'if' statment we can tell the user whether the number that was in putted is negative or posotive. 

```java 
public class ClassNameHere 
{
    public static void main(String[] args)
    {
        boolean b = "hello".equals("bye");
        System.out.println("hello".equals("bye"));

        String s1 = "hello";
        String s2 = "hello";
        String s3 = new String("hello");

        boolean b2 = s1 == s2
        boolean b3 = s1 == s3    

        boolean b4 = s1.equals(s2);
        boolean b5 = sq.equals(s3);
    }
}
```
This code demonstrates the difference between '==' and '.equals();'
'==' tests if they are the exact same object when you are testing for strings, it does not test if they are literally the same word, Ex. 'hello' is the same as 'hello' but the program tells us that they are different because they are not a part of the same object. 


### What if you want to test if the two strings are not equal?

```java
boolean b5 = "bird".notEquals("birds");
)
```
This makes sense but '.notEquals' is not an actual method 
so instead we would have to do this 
```java
boolean b5 = ! "bird".equals("birds");
```
The exclamation point tells us that it is NOT equal

### Dictionary Order
We all hopefully know what dictionary order is, so how can we do this in Java? <br>
Java Gives us an easy way of doing this with the '.compareTo();' method. 'compareTo();' does four boolean operations to a string at once, <, >, <=, >=, and tells us which word comes later in the dictionary. 
```java
import java.util.Scanner;

public class PositiveNegative
{
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);

        String word1 = in.next();
        String word2 = in.next();

        if (word1.compareTo(word2) > 0 ) // a condition that is either true or false
        {
            // what to do if the condition is true
            System.out.println("word1"); // word1 is after word2 
        }
        else
        {
            // what to do if the condition if false
            System.out.println("word2"); // word2 is after word1
        }
        System.out.println("bye");
    }
}
```