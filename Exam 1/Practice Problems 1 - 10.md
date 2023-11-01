# Practice Test: Questions 1 - 21
### Question 1 
<pre>
**
***
**
**
</pre>

### Question 2 
<pre>
**
***"*"

**
*\*\
</pre>
### Question 3 
<pre>
String s = "one two three four";
a) 10
b) one 5
c) twotf
d) 5
e) one2three four
f) Two
</pre>
### Question 4
<pre>
String x = "2" + 2;
String y = x + 2;
Output: 222
</pre>
### Question 5
<pre>
a) 3 * (101) - (-3) / (1)
   int, 306
b) (2.0 + (1)) / (1 - (-3))
   double, .75
c) x + 2 <= y
   boolean, false
d) x + y + "z"
   String, -2z
e) String, 1-3z
</pre>
### Question 6
<pre>
String ssn2 = ssn.substring(7);
</pre>
### Question 7 
<pre>
String pn2 = "(" + pn.substring(0,3) + ") " + pn.substring(3,6) + "-" + pn.substring(6);
</pre>
### Question 8 
<pre>
String d2 = d.substring(3,5) + "-" + d.substring(0,2) + "-" + d.substring(6)
</pre>
### Question 9 
<pre>
s1 = "123" <br>// in.next(); takes the next 'token' and saves it to s1, but the data type is a string so it saves it as a string <br>
s2 = "" <br>// Collects the rest of the empty spaces from line 1 <br>
n1 = 456 <br>// because it takes the next int in the std.in
</pre>
### Question 10
<pre>
a) 2
b) 6
</pre>

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