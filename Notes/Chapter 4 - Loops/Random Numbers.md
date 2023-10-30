# Random Numbers
[Section 4.16](https://learn.zybooks.com/zybook/PNWCS12300Fall2023/chapter/4/section/16)

Random numbers are very important in everything tech. Communicating in private, gaming, gambling, etc. 
```java
/*
   This program prints ten random numbers between 0 and 1.
*/
public class RandomDemo
{
   public static void main(String[] args)
   {
      for (int i = 1; i <= 10; ++i)
      {
         double r = Math.random();
         System.out.println(r);
      }
   }
}
```
You can use random numbers to flip a coin. 
```java
/* This program "flips a coin" ten times. */
{
    public class RandomDemo3
    {
        public static void main(String[] args)
        {
            for (int i = 1; i <= 10; i++)
            {
                double r = Math.random(); // 0 < r < 1
                if (r < 0.5)
                {
                    System.out.println("H");
                }
                else
                {
                    System.out.println("T");
                }
            }
        }
    }
}
```
Math.random() works can be used to get random numbers from different ranges and we can also use it to generate random integers
```java
Math.random()                    // random number between 0 and 1
  a + Math.random()                // random number between a and a+1
  b * Math.random()                // random number between 0 and b
  a + b * Math.random()            // random number between a and a+b
  a + (b-a) * math.random()        // random number between a and b
  (int)(a + (b-a) * Math.random()) // random integer between a and b-1
  (int)(n * Math.random())         // random integer between 0 and n-1
  (int)(n * Math.random() + 1)     // random integer between 1 and n
```

The "(int)" is called a 'cast' and all it does is remove the decimal, or trunkates the rest.
THis isn't very useful beacuse it loses all of the information, 1.7 will become 1. 1.2 will become 1. 
There aren't that many uses of (int) most of the time we use rounding.


```java
/*
   This program "rolls" a six-sided die ten times.
*/
public class RandomDemo4
{
   public static void main(String[] args)
   {
      for (int i = 1; i <= 10; ++i)
      {
         int n = (int)(1 + 6 * Math.random());  // 1 <= n <= 6
         System.out.println(n);
      }
   }
}
  ``` 