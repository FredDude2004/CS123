## Searching in Java
```java
public class ClassNameHere 
    public static void main(String[] args)
    {
        //       01234567890
        int n = "hello there class".indexOf("e");
    }
```
<pre>
n = 1
</pre>
```java
indexOf() // takes in a string and reports an index
charAt() // takes an int and gives you back a string

int n = "hello there class".indexOf("there");
char o = "hello there class".charAt(n);
```
<pre>
n = 6
o = 't'
</pre>

Also there is a way to find the last of a character or string
```java
int p = "hello there class".lastIndexOf("e");
```
<pre>
p = 10
</pre>

These are the basics of searching with java, but usually you will use a loop to find something
```java
boolean found = false;
char ch = '?';
int position = 0;

while(!found && position < str.length())
{
    ch = str.charAt(position);
    if (ch == 'A' || ch == 'a') { found = true; }
    else { position++ }
}
```
"Declare variable WHERE YOU NEED THEM, not at the beggining of your program."
 <br>\- Roger Kraft 2023 

 <br>
 when you are searching for something and you find it you stop. But computers are stoopid and have to be told when to stop, you can use a boolean, and set it to 'true' when you find what your looking for, or you can use a 'break' <br>
 Here is an example using a boolean: 

 ```java
 public class SearchString
 {
    public static void main(String[] args)
    {
        String str = "Max had a little lamb";

        char lookFor = 't';
        boolean found = false;
        int pos = 0;

        while (!found && pos < str.length()) // stop looping when you find the character
        {
            char ch = str.charAt(pos);
            if (ch == lookFor)
            {
                found = true;
            }
            else
            {
                pos++;
            }
        }

        if (found)
        {
            System.out.print("Found at pos: " + pos);
        }
        else
        {
            System.out.print("Not found");
        }
    }
 }
 ```
Here is an example using 'break'
 ```java
 public class SearchString
 {
    public static void main(String[] args)
    {
        String str = "Max had a little lamb";

        char lookFor = 't';
        int pos = 0;

        while (pos < str.length())
        {
            char ch = str.charAt(pos);
            if (ch == lookFor)
            {
                break; // stop looping when you find the character
            }
            else
            {
                pos++;
            }
        }

        if (pos < str.length())
        {
            System.out.print("Found at pos: " + pos);
        }
        else
        {
            System.out.print("Not found");
        }
    }
 }
 ```

 Java indicates that something isn't found with '-1'
 ```java
 int n = "hello there class".indexOf("z");
 int m = "hello there class".indexOf("w");
 ```
 <pre>
 n = -1
 m = -1
 </pre>

 Heres how we can use this in a program
 ```java
 public class SeachStringForFirst
 {
    public static void main(String[] args)
    {
        String str = "Max had a little lamb";

        char lookFor = 't';

        int pos = -1; // use -1 to mean "not found"

        for (int i = 0; i < str.length(); ++i)
        {
            char ch = str.charAt(i);
            if (ch == lookFor)
            {
                pos i;
                break; // stop looping when you find the char
            }
            System.out.println(pos);
            System.out.println(str.indexOf(lookFor));
        }
    }
 }
 ```
 ```java
 public class SeachStringForLast
 {
    public static void main(String[] args)
    {
        String str = "Max had a little lamb";

        char lookFor = 't';

        int pos = -1; // use -1 to mean "not found"

        for (int i = str.length() - 1; i >= 0; --i)
        {
            char ch = str.charAt(i);
            if (ch == lookFor)
            {
                pos i;
                break; // stop looping when you find the char
            }
            System.out.println(pos);
            System.out.println(str.lastIndexOf(lookFor));
        }
    }
 }
 ```
These programs can be simplified into 
```java
str.indexOf();
str.lastIndexOf();
```