# November 13th, 2023 Labs
## Lab 1
Write a program that reads one strictly positive integer n and then creates an array that holds the numbers from n down to 1.

After your code creates and fills the array, it should call the method Tester.printArray with the name of your array as the method's argument.

If the input number is 5, then your array should hold the following numbers.
<pre>
5 4 3 2 1
</pre>
Your program can assume that the single input integer will always be strictly positive.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int[] arr = new int[n];
      for (int i = 0; i < arr.length; i++)
      {
         arr[i] = n;
         n--;
      } 
      Tester.printArray( arr);
   }
}
```

## Lab 2 
Write a program that reads one strictly positive integer n and then creates an array that holds the numbers from 1 up to n and then the numbers from 1 up to n again (a second time).

After your code creates and fills the array, it should call the method Tester.printArray with the name of your array as the method's argument.

If the input number is 5, then your array should hold the following numbers.
<pre>
1 2 3 4 5 1 2 3 4 5
</pre>
Your program can assume that the single input integer will always be strictly positive.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int o = n;
      int[] arr = new int[n + n];
      for (int i = 0; i < n; i++)
      {
         arr[i] = i + 1;
      }
      for (int i = 0; i < n; i++ , o++)
      {
         arr[o] = i + 1;
      }
      
      Tester.printArray(arr);
   }
}
```

## Lab 3 
Write a program that reads a strictly positive integer n and then two other integers, a and b. Your program should create an array of size 2*n filled with alternating values of a and b.

After your code creates and fills the array, it should call the method Tester.printArray with the name of your array as the method's argument.

If the input numbers are 5, 3 and 11, then your array should hold the following numbers.
<pre>
3 11 3 11 3 11 3 11 3 11
</pre>
Your program can assume that the first input integer will always be strictly positive.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int a = in.nextInt();
      int b = in.nextInt();
      int[] arr = new int[n * 2];
      for (int i = 0; i < n * 2; i++)
      {
         arr[i] = a;
         i++;
         arr[i] = b;
      }
      Tester.printArray(arr);
   }
}
```

## Lab 4 
Write a program that reads a strictly positive integer n and then your program should create two arrays of size n, call them a and b. Then your program should continue to read 2*n more integers and it should alternate putting an input number into a and then b.

After your code creates and fills the two arrays, it should call the method Tester.printArray with the name of each array as the method's argument.

If the input numbers are
<pre>
 5 1 2 3 4 5 6 7 8 9 0
</pre>
then your first array should hold
<pre>
1 3 5 7 9
</pre>
and your second array should hold
<pre>
2 4 6 8 0
</pre>
If the input numbers are
<pre>
3  8  6 10  3  5  2
</pre>
then your first array should hold
<pre>
8 10 5
</pre>
and your second array hould hold
<pre>
6 3 2
</pre>
Your program can assume that the first input integer will always be strictly positive.

```java
import java.util.Scanner;

public class Main
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      int[] a = new int[n];
      int[] b = new int[n];
      
      for (int i = 0; i < n; i++)
      {
         a[i] = in.nextInt();
         b[i] = in.nextInt();
      }
      Tester.printArray(a);
      Tester.printArray(b);
   }
}
```