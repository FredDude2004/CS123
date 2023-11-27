# November 27th, 2023 Labs
## Lab 1
In the Main class below, write a public static method called labMethod that has three parameters, an integer array parameter, and two integer parameters. The method should search the array for occurrences of the first integer parameter and replace any occurrence in the array with the second integer parameter. The method should make the replacements in the input array. The method should have an int return type and the return value should be the number of replacements that were made by the method.

If the method's input array holds the integers
<pre>
1  2  3  4  5  4  3  2  1  2  3  4  5
</pre>
and the method is supposed to replace 3 with 5, then the array should hold the following integers after the method returns,
<pre>
1  2  5  4  5  4  5  2  1  2  5  4  5
</pre>
and the method's return value should be 3.

You do not need to write any code that calls your method. Your method will be called and tested by the Tester.java program.
```java
public class Main
{
   /**
      Define your method in this class.
   */
   public static int labMethod(int[] arr, int a, int b)
   {
      int counter = 0;
      for (int i = 0; i < arr.length; i++)
      {
         if (arr[i] == a)
         {
            arr[i] = b;
            counter++;
         }
      }
      return counter;
   }
}
```

## Lab 2
This lab makes a slight change in Lab 1.

In the Main class below, write a public static method called labMethod that has three parameters, an integer array parameter, and two integer parameters. The method should return an integer array. The method's output array should be a copy of the input array but with every occurrence of the first integer parameter replaced with the second integer parameter. The method should not make any changes to its input array.

If the method's input array holds the integers
<pre>
1  2  3  4  5  4  3  2  1  2  3  4  5
</pre>
and the method is supposed to replace 3 with 5, then the method's output array should hold the following integers.
<pre>
1  2  5  4  5  4  5  2  1  2  5  4  5
</pre>
After the method returns, the method's input array should be exactly like it was before the method was called.

You do not need to write any code that calls your method. Your method will be called and tested by the Tester.java program.

```java
public class Main
{
   /**
      Define your method in this class.
   */
   public static int[] labMethod(int[] inputArr, int a, int b)
   {
      int[] finalArr = new int[inputArr.length];
      for (int i = 0; i < inputArr.length; i++)
      {
         if (inputArr[i] == a)
         {
            finalArr[i] = b;
         }
         else
         {
            finalArr[i] = inputArr[i];
         }
      }
      return finalArr;
   }
}
```

## Lab 3
In the Main class below, write a public static method called labMethod that has one strictly positive integer parameter n. The method should return a two-dimensional array of size n-by-n. In the two-dimensional array, the column with index j should hold the integer j+1 from row 0 up to row j (but if j+1 is larger than 9, then the array should hold the ones-place from the integer). Every other entry in the array should be 0.

If the method's input integer is 6, then the method should return the following two-dimensional array.
<pre>
[1, 2, 3, 4, 5, 6]
[0, 2, 3, 4, 5, 6]
[0, 0, 3, 4, 5, 6]
[0, 0, 0, 4, 5, 6]
[0, 0, 0, 0, 5, 6]
[0, 0, 0, 0, 0, 6]
</pre>
If the method's input integer is 16, then the method should return the following two-dimensional array.
<pre>
[1, 2, 3, 4, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 2, 3, 4, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 3, 4, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 4, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 8, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 9, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 2, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 3, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 4, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 5, 6]
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 6]
</pre>
Hint: Since an array is initialized with zeros, you do not need to write any of the zero values into the array. You only need to worry about the non-zero values.

You do not need to write any code that calls your method. Your method will be called and tested by the Tester.java program.

```java
public class Main
{
   /**
      Define your method in this class.
   */
   public static int[][] labMethod(int n)
   {
      int[][] arr = new int[n][n];
      for (int i = 0; i < arr.length; i++)
      {
         for (int j = 0; j < arr[i].length; j++)
         {
            if (j < i) {arr[i][j] = 0;}
            else if (j >= 9) {arr[i][j] = j - 9;}
            else {arr[i][j] = j + 1;}
         }
      }
      return arr;
      }
}
```

## Lab 4
In the Main class below, write a public static method called labMethod that has one strictly positive integer parameter n. The method should return a two-dimensional array of size n-by-n. In the two-dimensional array there should be the integer 1 in the first and last rows, the first and last columns, and along the two diagonals of the array. Every other entry in the array should be 0.

If the method's input integer is 7, then the method should return the following two-dimensional array.
<pre>
1 1 1 1 1 1 1
1 1 0 0 0 1 1
1 0 1 0 1 0 1
1 0 0 1 0 0 1
1 0 1 0 1 0 1
1 1 0 0 0 1 1
1 1 1 1 1 1 1
</pre>
If the method's input integer is 17, then the method should return the following two-dimensional array.
<pre>
1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
1 1 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1
1 0 1 0 0 0 0 0 0 0 0 0 0 0 1 0 1
1 0 0 1 0 0 0 0 0 0 0 0 0 1 0 0 1
1 0 0 0 1 0 0 0 0 0 0 0 1 0 0 0 1
1 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 1
1 0 0 0 0 0 1 0 0 0 1 0 0 0 0 0 1
1 0 0 0 0 0 0 1 0 1 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 1 0 1 0 0 0 0 0 0 1
1 0 0 0 0 0 1 0 0 0 1 0 0 0 0 0 1
1 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 1
1 0 0 0 1 0 0 0 0 0 0 0 1 0 0 0 1
1 0 0 1 0 0 0 0 0 0 0 0 0 1 0 0 1
1 0 1 0 0 0 0 0 0 0 0 0 0 0 1 0 1
1 1 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1
1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
</pre>
Hint: Since an array is initialized with zeros, you do not need to write any of the zero values into the array. You only need to worry about the non-zero values.

You do not need to write any code that calls your method. Your method will be called and tested by the Tester.java program.

```java
public class Main
{
   /**
      Define your method in this class.
   */
   public static int[][] labMethod(int n)
   {
      int[][] arr = new int[n][n];
      for (int i = 0; i < n; i++)
      {
         for (int j = 0; j < n; j++)
         {
            if (i == 0 || j == 0 ||
                i == n - 1 || j == n - 1 ||
                i == j || j == n - i - 1)
            {
               arr[i][j] = 1;
            }
            else
            {
               arr[i][j] = 0;
            }
         }
      }
      return arr;
      }
}
```
