# Exam 2 Answers

## Problem 1

<pre>
************
***********
**********
*********
********
*******
******
*****
****
***
**
*
**
***
****
*****
******
*******
********
*********
**********
***********
************
</pre>

## Problem 2 

```java
for (int i = 0; i < s1.length(); i++) {
    System.out.print(s2.substring(0, i));
    System.out.println(s1.substring(i));
}
```

## Problem 3

a)
```java
for (int i = 0; i < s.length(); i++) {
    System.out.println(s.substring(i) + "*");
}
```
b)
```java
for (int i = s.length(); i > 0; i--) {
    System.out.println(s.substring(i) + "*");
}
```
c) 
```java
String s = "         ";
        int innerSpace = 0;
        for (int i = s.length(); i > 0; i--) {
           System.out.print(s.substring(i) + "*");
           System.out.println(s.substring(innerSpace) + "*");
           innerSpace += 2;
        }
```

## Problem 4

```java
int count = 10;
for (int i = 0; i < 8; i++) {
    for (int j = 0; j <= i; j++) {
        System.out.print(count + " ");
        count++;
    }
    System.out.println();
}
```

## Problem 5

```java
String s1 = "      ";
int magic = 6;

for (int i = 0; i <= s1.length(); i++) {
    System.out.print(s1.substring(i));
    for (int j = 0; j <= i; j++) {
        System.out.print(magic);
    }
    magic--;
    System.out.println();
} 
```

## Problem 6

```java
import java.util.Scanner;

public class FencePosts 
{
    public static void main(String[] args) 
    {
        Scanner in = new Scanner(System.in);
        int size = in.nextInt();

        for (int i = 0; i < size; i++) {
            if (!(i == size - 1)) {
                System.out.print("|/\\");
            }
            else {
                System.out.print("|/\\|");
            }
        }
    }
}
```

## Problem 7

```java
import java.util.Scanner;

public class RectangleTriangle {
   public static void main(String[] args) {
    Scanner in = new Scanner(System.in);
        int size = in.nextInt();

        for (int i = 0; i < size * 2 + 3; i++) {
            System.out.print("*");
        }
        System.out.println();
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < (size * 2 + 2) - i; j++) {
                
                if (0 < j && j < size + 1) {
                    System.out.print(" ");
                }
                else if (size + 1 < j && j < (size * 2 + 1) - i) {
                    System.out.print(" ");
                }
                else {
                    System.out.print("*"); 
                }
            }
            System.out.println();
        }
        for (int i = 0; i < size + 2; i++) {
            System.out.print("*");
        }
   }
}
```

## Problem 8 

0 1 0 1 0
1 0 1 0 1
0 1 0 1 0
1 0 1 0 1 

## Problem 9

bro idk

## Problem 10

```java
public static void main(String[] args)
{
    methodC();
    for (int i = 0; i < 14; i++)
    {
        methodA();
        System.out.print("-");
    }
    methodB();

}
   ```

## Problem 11
```java 
public static int max2(int a, int b) 
{
    if (a >= b)
    {
        return a;
    }
    else
    {
        return b;
    }
}
```

## Problem 12
```java
public static double min2(double a, double b)
{
    double result;
    if (a - b < 0)
    {
        result = a;
    }
    else
    {
        result = b;
    }
    return result;
}
```

## Problem 13
It removes the spaces

```java
"what the fish";
"whatthefish";
"This Is A Sentence";
"ThisIsASentence";
```

## Problem 14 
```java
public static boolean closeEnough(double a, int b)
{
    if (b - 1.0 <= a && a <= b + 1.0)
    {
        return true;
    }
    else
    {
        return false;
    }
}
```

## Problem 15 
```java
public static void linePrint(int size)
{
    System.out.print("*");
    for (int i = 1; i < size; i++)
    {
        System.out.print("&");
    }
    System.out.print("=");
}
```

## Problem 16
it doesn't have a return statement for if the person is not a millionire. 

```java
public static boolean isMillionaire(int netWorth)
{
    if (netWorth >= 1000000)
    {
        return ture;
    }
    else 
    {
        return false;
    }
}
```
This should fix the problem

## Problem 17
```java
public static boolean isInside(int n)
{
    return (0 < n && n < 100);
}
```