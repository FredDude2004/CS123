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

