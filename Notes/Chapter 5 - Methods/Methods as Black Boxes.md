# Methods as Black Boxes
We've been working with methods a lot, but now we are going to start writing methods. 

```java
public class ClassNameHere
{
    public static void main(Srting[] args)
    {
        String s = "hello there".substring(4, 8); /* call a method
                                                     pass it parameters
                                                     get back a return value */
    }
}
```

In most other languages 'methods' are called 'functions' 
here is an example of a function that converts Fahrenheit to Celsius

```java
public class F2C
{
   public static void main(String[] args)
   {
      // Print a table of temperature conversions.
      for (double t = 0.0; t <= 100.0; ++t)
      {
         System.out.println(t + " degrees F is " + f2c(t) + " degrees C" );
      }
   }

   // Convert Fahrenheit temperatures to Celsius temperatures.
   public static double f2c(double t)
   {
      return (t - 32.0) * 5.0/9.0;
   }
}
```

This is how you write a method, and you can call the method inside the program. 

Here is a WRONG way to wrote a mathod. 

```java
public class F2C_bad
{
   public static void main(String[] args)
   {
      // Print a table using the bad version of f2c.
      for (double t = 0.0; t <= 100.0; ++t)
      {
         System.out.print(t + " degrees F is "); // Print part of our output.
         f2c_bad(t);                             // Print the converted temperature.
         System.out.println( " degrees C" );     // Print the rest of our output.
      }
   }

   // This is a BAD way to define a method.
   // This method computes a result and then
   // prints the result instead of returning
   // the result to whoever called this method.
   public static void f2c_bad(double t) // Notice that this is a void method.
   {
      System.out.print( (t - 32.0) * 5.0/9.0 );
   }
}
```

This has a method that prints something, which is bad. Its bad becuase if you ever wanted to change something in
the program it wouldn't work. Because of the 'void' it wouldn't return a value. 