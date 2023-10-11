# Practice Test: Questions 11 - 20
### Question 11 
<pre>
0,1, or 2 <br>
if u is greater than 0 then it will add one to w <br>
if v is greater than 0 then it will add one to w <br>
</pre>
### Question 12 
<pre>
0 or 1 <br>
Because it uses an else-if statement, it will only ever execute one of the clauses 
</pre>
### Question 13 
```java
if (p < 0) {System.out.println("p is negative");}
else if (p > 0) {System.out.println("p is posotive");}
else {System.out.println("p is zero");}
```

### Question 14 
<pre>
A
C
H

</pre>
### Question 15 
<pre>
One. // Short circuts at b1 
Three. // Doesn't short circut
Five. // Doesn't short circut
Six. // Short circuts at !b2, and then it doesn't short cirut
</pre>
### Question 16 
<pre>
They tried to write the if clause like algebra, which won't compile 
you need to write it using Boolean Logic <br>
</pre>
```java
if (x >= 5 && x <= 5)
{
    System.out.println("x is between 0 and 5");
}
```
<pre>
This fixes the error
</pre>
### Question 17 
<pre>
if (<font color="#00FF00">x && y</font> == <font color="red">0</font>)
<font color="#00FF00">x and y</font> are booleans, which are true or false. You can't compare booleans to an <font color="red">integer</font> 
</pre>
```java
if (x == 0 && y == 0)
{
    System.out.println("x and y are both zero");
}
```
### Question 18 
<pre>
This program prints "x and y are both zero" if they both equal 0, and it prints "x and y are not equal if they are not equal <br>
</pre>
```java
if (x == y)
{
    if (x == 0)
        System.out.println("x and y are both zero");
}
else 
    System.out.println("x and y are not equal");
```
### Question 19 
<pre>
    apple     banana       grape      pear      plum
<----------]-----------]----------]----------]---------->
 0        10          20         30         40        50 
</pre>
```java
if (n <= 10)
{
    System.out.println("apple");
}
else if (n <= 20)
{
    System.out.println("banana");
}
else if (n <= 30)
{
    System.out.println("grape");
}
else if (n <= 40)
{
    System.out.println("pear");
}
else 
{
    System.out.println("plum");
}
```
### Question 20 
<pre>
This program has an issue because it only covers half of the number line so the boolean 'adult' wont have a value if the input is on the other half of the number line <br>
        false              ???? 
<------------------|-------------------> 
                  21 <br>
To fix this you would just need to add an else clause
</pre>
```java
import java.util.Scanner;
   public class Program19
   {
      public static void main(String[] args)
      {
         Scanner in = new Scanner(System.in);
         int age = in.nextInt();
         boolean adult;
         if (age < 21)
         {
            adult = false;
         }
         else
         {
            adult = true;
         }
         System.out.println(adult);
      }
   }
```
### Question 21
<pre>
    "-1"     "0"   "1" 
<-----|----[-----]----->
     -1    0     1
This can be simplified by removing the default clause, simplifying the first 'else if' statment to (n <= 1), and changing the second 'else if' statment to the default clause
</pre>
```java
import java.util.Scanner;
   public class Program20
   {
      public static void main(String[] args)
      {
         Scanner in = new Scanner(System.in);
         double n = in.nextDouble();

         if (n < 0)
         {
            System.out.println( -1 );
         }
         else if (n <= 1)
         {
            System.out.println( 0 );
         }
         else // (n > 1)
         {
            System.out.println( 1 );
         }
      }
   }
```