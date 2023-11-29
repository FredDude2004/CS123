# November 29th Labs
## Lab 1
In the Main class below, write a public static method called labMethod that has one parameter that is a two-dimensional array of integers. The method should return a two-dimensional array of integers.

The array returned by the method should have the same number of rows as the input array. Each row of the output array should be the same as its equivalent row from the input array but with any 0 entries removed. If a row of the input array is all 0's, then that row in the output array should be an empty row (a row of length 0).

The method should not make any changes to the input array.

If the method's input array looks like this,
<pre>
1 1 1 1 1 1 1
1 1 0 0 0 1 1
1 0 1 0 1 0 1
1 0 0 1 0 0 1
1 0 1 0 1 0 1
1 1 0 0 0 1 1
1 1 1 1 1 1 1
</pre>
then the method's output array should look like the following.
<pre>
1 1 1 1 1 1 1
1 1 1 1
1 1 1 1
1 1 1
1 1 1 1
1 1 1 1
1 1 1 1 1 1 1
</pre>
If the method's input array looks like this,
<pre>
1 0 2 0 3 0 4 0
1 2 3 4 5 6
0 0 0 0 0 0
0 0 1 0 0 0
</pre>
then the method's output array should look like the following.
<pre>
1 2 3 4
1 2 3 4 5 6

1
</pre>
Hint: In class on Monday we did an example program called BuildAndInitializeTriangularArray that shows how to build, row-by-row, a ragged, two-dimensional array.

You do not need to write any code that calls your method. Your method will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 5. The Tester.java program then runs one of its five built in test cases.

```java
public class Main
{
   /**
      Define your method in this class.
   */
   public static int[][] labMethod(int[][] arr)
   {
      int count = 0;
      int[][] result = new int[arr.length][]; // initialize an array of rows
      for (int i = 0; i < arr.length; i++)
      {
         for (int j = 0; j < arr[i].length; j++) // count the # of values != to 0
         {
            if (arr[i][j] != 0){count++;}
         }
         result[i] = new int[count]; // set the row length
         count = 0; // reset count
      }
     
      int resIndex = 0;
      for (int i = 0; i < arr.length; i++) // filling the array
      {
         for (int j = 0; j < arr[i].length; j++)
         {
            if (arr[i][j] != 0)
            {
               result[i][resIndex] = arr[i][j];
               resIndex++;
            }
         }
         resIndex = 0;
      }
      return result;
   }
}
```

## Lab 2
Write three new methods for the Counter class defined below.

Write a method called countTwo that increments a Counter object's value by 2.

Write a method called unCount that decrements a Counter object's value, but does not let the object's value become negative. So if a Counter object's value is 0 and the unCount method is called on that object, then the counter object's value stays 0.

Write a method called unCountTwo that decrements a Counter object's value by 2, but does not let the object's value become negative. So if a Counter object's value is 0 and the unCountTwo method is called on that object, then the counter object's value stays 0. If a Counter object's value is 1 and the unCountTwo method is called on that object, then the counter object's value becomes 0 (not -1).

You do not need to write any code that calls your methods. Your methods will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 3. The Tester.java program then runs one of its three built in test cases.

Note: You can test your Counter methods by copying your Counter class into the Java Visualizer, as we did in class.


```java
/**
   This class models a tally counter.
*/
public class Counter
{
   private int value;

   /**
      Advances the value of this counter by 1.
   */
   public void count()
   {
      value += 1;
   }

   /**
      Resets the value of this counter to 0.
   */
   public void reset()
   {
      value = 0;
   }

   /**
      Gets the current value of this counter.
      @return the current value
   */
   public int display()
   {
      return value;
   }

   /**
      Increment the value of this counter by 2.
   */
   public void countTwo()
   {
      value += 2;
   }
   
   /**
      Decrement the value of this counter by 1. But do not
      let this counter's value become negative.
   */
   public void unCount()
   {
      if (value > 0) {value -= 1;}
   }

   /**
      Decrement the value of this counter by 2. But do not
      let this counter's value become negative.
   */
   public void unCountTwo()
   {
      if (value > 1) {value -= 2;}
      else {value = 0;}
   }
}
```