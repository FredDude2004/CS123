# While Loops 
We've been using if statment which are quite simple and test a condition, and if that condition is true, the program will do something
```java
if (condition) // condition is something true or false
{
    // do something
}
```
Now we will start using the different types of loops, such as the 'while' loop. <br>
The while loop tests a condition, and while that condition is still true it will repeat a program.

```java
while (condition) // condition is something true or false
{
    // do something
}
```
While loops are generally used when we are NOT counting something. 
While loops have lots of uses, lets look at an example of its use.

### Example 1 

```java
public class Squares
{
    public static void main(String[] args)
    {
        int n = 0;
        System.out.println(n + " squared is " + n*n);
        ++n; // ++n; is the same as n = n + 1;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
        System.out.println(n + " squared is " + n*n);
        ++n;
    }
}
```
This is a terrible way to repeat code, its just the same thing copies over and over again which makes the program needlessly long and hard to read. Instead we can use a loop.

```java
public class Squares2
{
    public static void main(String[] args)
    {
        int n = 0;
        while (n < 10)
        {
            System.out.println(n + " squared is " + n*n);
            ++n; // ++n; is the same as n = n + 1;
        }
    }
}
```

This is a lot simpler and more effecient than the method we used before. We can also rewrite this program with a for loop

```java
public class Squares3
{
    public static void main(String[] args)
    {
        for (int n = 0; n < 10; ++n) // ++n; is the same as n = n + 1;
        {
            System.out.println(n + " squared is " + n*n);
        }
    }
}
```
Loops make it a lot easier to change small things in code. For example if we were using this our original program and we wanted to change it from adding 1 to n, to adding 3 to n. It would be a real pain because we would have to change each individual line. 

```java
public class Squares
{
    public static void main(String[] args)
    {
        int n = 0;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
        System.out.println(n + " squared is " + n*n);
        n = n + 3;
    }
}
```
Very painful and time consuming, where if we had used a loop wit would be a lot easier 

```java
public class Squares2
{
    public static void main(String[] args)
    {
        int n = 0;
        while (n < 10)
        {
            System.out.println(n + " squared is " + n*n);
            n = n + 3;
        }
    }
}
```
This makes it a whole lot easier. 

### Where we would use a while loop 
Say we wanted to write a program that would take an input and print out the first posotive value.
There could be any number of negative values before there is a single posotive, it would be really cumbersome and inefficient to just use a bunch of 'if' statments, so we can use a while loop 
```java
import java.util.Scanner;

public class FindPositiveInteger
{
    Public static void main(String[] args)
    {
        Sanner in = new Scanner(System.in);

        int n = in.nextInt();

        while (n < 0)
        {
            n = in.nextInt();
        }

        System.out.println(n);
    }
}
```
std.in
<pre>
-1 -2 -1 -4 -5 -1 5 -1 -1 -1 6 -3 -7 -4 
</pre>

