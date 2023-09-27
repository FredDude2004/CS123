# Poorly Written If Statments
```java
public class ClassNameHere 
{
    public static void main(String[] args)
    {
        if (n < 100)
        {
            System.out.println("blue");
        }
        else if (n < 200)
        {
            System.out.println("yellow");
        }
        else if (n < 150)
        {
            System.out.println("green");
        }
        else if (n >= 200)
        {
            System.out.println("orange");
        }
        else
        {
            System.out.println("red");
        }
    }
}
``` 
This if statment is written poorly, there are 5 clausees in the if statment, but only three of them have an effect on the program. For example 
```java
 else if (n < 150)
        {
            System.out.println("green");
        }
```
This clause doesn't do anything, because it is already asked if n is less than 200 and prints yellow, so it skips over it. It is pointless. 
<br> <br>
This clause is also pointless
```java
else
        {
            System.out.println("red");
        }
```
Because everything is already covered on the numberline so the program will never print out red. It's pointless
<br> <br>
Here would be a simplified version of the program
```java
public class ClassNameHere 
{
    public static void main(String[] args)
    {
        if (n < 100)
        {
            System.out.println("blue");
        }
        else if (n < 200)
        {
            System.out.println("yellow");
        }
        else 
        {
            System.out.println("orange");
        }
    }
}
```
This accomplishes the same task as the previous program just in a much simpler way

## Equivelent Pieces of Code
```java

```

## Puzzle 
```java
public class ClassName Here
{
//For which values of the in n does the following nested if-else-statment print out "peach"?
    public static void main(String[] args)
    {
        if (n < 0)
        {
            System.out.println("pear");
        }
        else if (100 <= n && n <=200)
        {
            System.out.println("plum");
        }
        else 
        {
            SYstem.out.println("peach");
        }
    }
}
```

If we draw the number line we can solve this problem

<pre>
       0      100    200   
<------[-------[------]------->
  pear   peach   plum   peach
</pre>

We can see that peach will print out when (0 <= n < 100) || (n > 200). So a good idea is to coment what the else clause does so we don't have to figure it out

```java
else // (0 <=n < 100) || (n > 200)
{
    SYstem.out.println("peach");
}
```

Let's try another one 

```java
public class ClassNameHere 
{
    public static void main(String[] args)
    {
//For which values of the int n does the following nested if-else-if-statment print out "peach"?
        if (n < 0)
        {
            System.out.println("pear");
        }
        else if (100 <= n && n <= 200)
        {
            System.out.println("plum");
        }
        else if (n > 300)
        {
            System.out.println("pineapple");
        }
        else
        {
            System.out.println("peach");
        }
    }
}
```
Again we can make a number line
<pre>
       0      100    200     300
<------[-------[------]-------]----------->
  pear   peach   plum   peach   pineapple
</pre>

We can see what values of n will print out peach
<br> 0 <= n < 100 Or 200 < n <= 300 <br>so we can comment it on the default clause 

```java
else // 0 <= n < 100 || 200 < n <= 300
{
    System.out.println("peach");
}
```