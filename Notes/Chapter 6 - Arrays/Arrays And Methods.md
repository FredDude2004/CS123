# Arrays in Methods
We started with common loop algorithms, then we moved onto common 
array algorithms, and now we are going to put these into methods. 

Here is the code for the average 
```java
public static double avg(double[] array)
{
    double sum = 0.0;
    for (int i = 0; i < array.length; ++i)
    {
        sum += array[i];
    }
    return sum / array.length;
}
```
We've used this same pattern to find the average many times, now we are 
going to put it into a method so that we can call it anytime we need it.

```java
public class Average
{
   public static double avg(double[] array)
   {
      double sum = 0.0;
      for (int i = 0; i < array.length; ++i)
      {
         sum += array[i];
      }
      return sum / array.length;
   }

   public static void main(String[] args)
   {
      double[] a1 = {5, 6, 7, 8, 9};
      double avg1 = avg(a1);
      System.out.println(avg1);

      double[] a2 = {-3, -2, -1, 1, 2, 3};
      double avg2 = avg(a2);
      System.out.println(avg2);
   }
}
```

Now its important to note that the array in the main method will be the 
SAME array that will be in the method 'avg'. So if you change the values 
in the array during the method call of 'avg' it will change the values of 
the array in the main method as well. 

So if we canged the code like this
```java
public static double avg(double[] array)
{
    double sum = 0.0;
    for (int i = 0; i < array.length; ++i)
    {
        sum += array[i];
        array[i] = 0.0;
    }
    return sum / array.length;
}
```

This would be problamatic, because you now just lost all of the data that was inside of that array. 
