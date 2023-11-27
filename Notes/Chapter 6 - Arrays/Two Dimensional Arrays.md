```java
public class TwoDimArrays
{
   public static void main(String[] args)
   {
      int[][] arr1 = new int[3][4];
      double[][] arr2 = new double[5][2];
      boolean[][] arr3 = new boolean[4][4];

      int [][] arr4 = {{1,2,3}, {4,5,6}};
      double [][] arr5 = {{1.0},
                          {2.0,3.0},
                          {4.0,5.0,6.0},
                          {7.0,8.0,9.0,10.0}};
   }
}
```



```java
public class TwoDimArray
{
   public static void main(String[] args)
   {
      int[][] arr = new int[5][5];

      // How to loop through a 2D array.
      for (int i = 0; i < arr.length; ++i)
      {
         for (int j = 0; j < arr[i].length; ++j)
         {
            if (i == j)
            {
               arr[i][j] = 1;
            }
         }
      }
      print2Darray(arr);
   }

   public static void print2Darray(int[][] arr)
   {
      // How to loop through a 2D array.
      for (int i = 0; i < arr.length; ++i)
      {
         for (int j = 0; j < arr[i].length; ++j)
         {
            System.out.print(arr[i][j]);
         }
         System.out.println();
      }
   }
}
```
```java
// int[][] arr = {{0},{0,0},{0,0,0},{0,0,0,0},{0,0,0,0,0}};

// if (i == j || j == 0 || i == arr.length-1 )


      int size = 15;
      int[][] arr2 = new int[size][];
```