# Nested Loops 
Nested Loops as we will see are really just tables, and different ways to process tables.

```java
public class NestedForLoops_1
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 3; i++)
        {
            for (int j = 1; j <= 5; j++)
            {
                System.out.println("hello from i=" + i + " and j=" + j);
            }
        }
    }
}
```
Output
<pre>
hello from i=1 and j=1
hello from i=1 and j=2
hello from i=1 and j=3
hello from i=1 and j=4
hello from i=1 and j=5
hello from i=2 and j=1
hello from i=2 and j=2
hello from i=2 and j=3
hello from i=2 and j=4
hello from i=2 and j=5
hello from i=3 and j=1
hello from i=3 and j=2
hello from i=3 and j=3
hello from i=3 and j=4
hello from i=3 and j=5
</pre>
Now this doesn't look like a table but pretty soon we will even make it look like a table. 

You can also do something like this 
```java
public class NestedForLoops_2
{
    public static void main(String[] args)
    {
        for (int i = 2; i <= 3; i++)
        {
            for (int j = 3; j <= 5; j++)
            {
                System.out.println("hello from i=" + i + " and j=" + j);
            }
        }
    }
}
```
This shortens the rectangle 
<pre>
hello from i=2 and j=3
hello from i=2 and j=4
hello from i=2 and j=5
hello from i=3 and j=3
hello from i=3 and j=4
hello from i=3 and j=5
</pre>

Now we can make the code print out what really looks like a table. 
```java
public class NestedForLoops_2
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 3; i++)
        {
            for (int j = 1; j <= 5; j++)
            {
                System.out.print("(" + i + ", " + j + ")");
            }
           System.out.println();
        }
    }
}
```
<pre>
(1, 1)(1, 2)(1, 3)(1, 4)(1, 5)
(2, 1)(2, 2)(2, 3)(2, 4)(2, 5)
(3, 1)(3, 2)(3, 3)(3, 4)(3, 5)
</pre>
But this isn't like the 'x' , 'y' coordinate plane instead its on a table. where the 'x's are the rows and the 'y's are the columns. This can be confusing, if you are used to thinking of an (x , y) plane. 

```java
public class NestedForLoops_2
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 7; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print("*");
            }
           System.out.println();
        }
    }
}
```
<pre>
*
**
***
****
*****
******
*******
</pre>
Prints half of the square, or a triangle

Heres a way to flip the triangle
```java
public class NestedForLoops_3
{
    public static void main(String[] args)
    {
        for (int i = 7; i > 0; i--)
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print("*");
            }
           System.out.println();
        }
    }
}
```
<pre>
*******
******
*****
****
***
**
*
</pre>
This is a little bit of a quirky way of thinking about it becuase you reverse the rows, and they are now counting down. 

<pre>
7
6
5
4
3
2
1
</pre>
like this now if we wanted to write it like we've been working with 
<pre>
1
2
3
4
5
6
7
</pre>
its a little bit trickier
```java
public class NestedForLoops_3
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 7; i++)
        {
            for (int j = 1; j <= 8 - i; j++)
            {
                System.out.print("*");
            }
           System.out.println();
        }
    }
}
```
We have to use a little formula <pre> 8 - i </pre>
<pre>
*******
******
*****
****
***
**
*
</pre>
