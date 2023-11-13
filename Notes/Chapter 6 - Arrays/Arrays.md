# Arrays
Suppose you were writing a program where you needed to store over 1000 different values, now it would be silly to write a different variable for each value. Instead you would use an array. 

```java
public class ArrayDemo {
    public static void main(String[] args) {
        int[] x = new int[100]; // initailizing an array. 

    }
}
```
Now its important to understand that 'x' is not an array, its just the name of the array. 
```java
public class ArrayDemo {
    public static void main(String[] args) {
        int[] x = new int[100]; // initailizing an array. 
        int[] y =x;
    }
}
```
Now 'y' isn't an array its just the name of an array, and both 'x' and 'y' point to the same array. 

So if you were to change the 5th value in 'x', it would also change the fifth value or 'y'.

```java
1 int[] a = { 3, 1, 4, 1, 5, 9 }; 
2 int[] b = a; 
3 a[0] = 1; 
4 b[1] = 0;
```
What is the value of a[0] after line 3 executes?
<pre>1</pre>
What is the value of b[0] after line 3 executes?
<pre>Also 1</pre>
What is the value of b[1] after line 4 executes?
<pre>0</pre>
What is the value of a[1] after line 4 executes?
<pre>Also 0</pre>

Just like strings, arrays have indexes starting at 0. 
```java
public class ArrayIndexes {
    public static void main(String[] args) {
        int[] x = new int[100];
        for (int i = 0; i < x.length; i++) {
            x[i] = i;
        }
    }
}
```
This will fill the array with its indexes. 

## A string array is not an array of strings, it is an array of string references.