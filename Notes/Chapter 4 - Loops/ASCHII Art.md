```java
public class NestedForLoops_10
{
    public static void main(String[] args)
    {
        int width = 5;
        int height = 5;

        for (int j = 1; j <= width; ++j)
        {
            System.out.print("*");
        }
        System.out.println();

        for (int i = 1; i <= height - 2; ++i)
        {
            System.out.print("*");
            for (int j = 1; j <= width - 2; ++j)
            {
                System.out.print(" ");
            }
            System.out.println("*");
        }

        for (int j =1; j <= width; ++j)
        {
            System.out.print("*");
        }
        System.out.println();
    }
}
```

<pre>
*****
*   *
*   *
*   *
*****
</pre>

```java
public class NestedForLoops_10
{
    public static void main(String[] args)
    {
        int width = 15;
        int height = 7;

        for (int i = 1; i <= height; ++i)
        {
            for (int j = 1; j <= width; ++j)
            {
               if (i == 1)
               {
                  System.out.print("*"); // top border
               }
               else if (i == height)
               {
                  System.out.print("*"); // bottom border
               }
               else if (j == 1)
               {
                  System.out.print("*"); // left border
               }
               else if (j == width)
               {
                  System.out.print("*"); // right border
               }
               else
               {
                  System.out.print(" ");
               }
            }
            System.out.println();
        }
    }
}
```
<pre>
***************
*             *
*             *
*             *
*             *
*             *
***************  
</pre>

```java
/* Size = 6
          i   size-i    i
         row  spaces  stars
       *  1      5      1
      **  2      4      2
     ***  3      3      3
    ****  4      2      4
   *****  5      1      5     
  ******  6      0      6
*/
public class ClassNameHere 
{
   public static void main(String[] args) 
   {
      int size = 6;
      
      for (int i = 1; i <= size; ++i)
      {
         for (int j = 1; j <= size - i; ++j)
         {
            System.out.print(" ");
         }
         for (int j = 1; j <= i; ++j)
         {
            System.out.print("*");
         }
         System.out.println();
      }
   }
}
```
<pre>
       *
      **  
     *** 
    **** 
   *****     
  ******
  </pre>