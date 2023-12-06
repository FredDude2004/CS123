
# CS 12300-001 Final Exam Review

The final exam is on Monday, December 11.

The final exam is over the whole semester.

Be sure to review the review problems for each of the first
two midterm exams and also review the two exams themselves.

The sections covered since the second midterm exam are from
Chapters 6 and 8 in the textbook, https://learn.zybooks.com/zybook/PNWCS12300Fall2023/
   Sections 6.1, 6.4, 6.7, 6.9, 6.10, 6.12, 6.13.
   Sections 8.1, 8.2, 8.3, 8.5, 8.6, 8.7, 8.14.


The topics covered since the second midterm exam are:
   1) array objects,
      array reference variables,
      aliases,
      array initialization,
      partially filled arrays,
      basic array algorithms (sum, max, min, search, copy, print, etc),
      array parameters to a method,
      array return value from a method,
      two-dimensional arrays.
   2) classes & objects,
      instance variables (fields)
      instance methods (instead of static methods),
      constructors,
      this keyword,
      dot notation,
      accessor methods,
      variable scope.


Below are review problems for the material we have covered
since the second midterm exam. For the final exam you should
also study Exam 1 and Exam 2 plus the review problems for
those two exams.



### Problem 1 
If variable a is a reference to an array, what happens if the
following statement is executed? Briefly explain why.
```java
    System.out.println(a[a.length]);
```

### Problem 2 
Assume that arr is a reference to an array containing integers.
Write a for-loop that multiplies every element in arr by 10.


### Problem 3 
Write a program segment that declares an array reference variable,
constructs an array object, assigns the array object to the array variable,
and then uses a loop to fill the array object with the following integers.
<pre>
   -50, -40, -30, -20, -10, 0, 10, 20, 30, 40, 50.
</pre>

### Problem 4
Write a method called sumArray that accepts a reference to an array
of doubles and returns the sum of the values stored in the array.


### Problem 5 
Write a method called sumSubArray that accepts a reference to an
array of doubles and two ints. If the two ints are valid indices, then the

method should return the sum of the values stored in the array whose indices

are between the two ints (inclusive). If the two ints are not valid indices, then the method should return zero.


### Problem 6 
Suppose that the variables a and b are references to arrays of
integers with length at least two. What is the value of b[0] and b[1] after
the following statements have been executed? Explain why. Your explanation
should include an appropriate drawing of Java’s memory.
```java
   a[0] = 1;
   b[0] = 2;
   b = a;
   b[1] = 3;
   a[1] = 4;
```

### Problem 7 
After the following code has executed its last line,
how many array objects have reference variables referring to them?
Explain your answer with a drawing of Java's memory.
```java
   int[] a = {21, 11, 10, 9};
   int[] b = new int[6];
   int[] c = a;
   a = new int[5];
   b = a;
   int[] d = b;
```

### Problem 8 
Show the output of the following program.
Explain what the second for-loop is doing.
```java
   public class Problem
   {
      public static void main(String[] args)
      {
         int[] a = new int[8];
         for (int i = 0; i < a.length; i++)
         {
            a[i]=i+1;
            System.out.println(a[i]);
         }
         int result = 0;
         for (int i = 0; i < a.length / 2; i++)
         {
            result += a[i] * a[a.length-i-1];
         }
         System.out.println("Result = " + result);
      }
   }
```

### Problem 9 
Suppose that the parameter arr is always a reference to
an array of size n >= 2 containing integers from 1 to n-1, inclusive,
with exactly one number repeated. Write the method
```java
   public static int findRepeatedNumber(int[] arr)
```
that returns the value of the repeated number in the array arr.
(Hint: Use two nested for-loops.)



### Problem 10 
Suppose I have defined a class called Thing.
The following line performs three distinct steps. What
are they? How would you rewrite this single line as two
lines? What distinct steps do each of those two lines perform?
```java
   Thing rose = new Thing();
```


### Problem 11
Consider the following class definition.
```java
   class Thing
   {
      private int x = 0;
      private double y = 0.0;
      public void setX(int x) { this.x = x; }
      public void setY(double y) { this.y = y; }
      public int getX() { return x; }
      public double getY() { return y; }
      public int methodA() { return 2*x; }
      public double methodB() { return 3*y; }
   }
```

Suppose that we have the following declarations.
```java
   Thing a = new Thing();
   Thing b = new Thing();
```
Explain why each of the following statements is either OK or not OK.
```java
   b.x = 5;

   int u = a.getY();

   double v = b.getX();

   a.setX(3.2);

   b.getY();

   double w = b.setY(4.5);

   int x = Thing.methodA();

   int y = a.methodB(5);

   a = b.methodA();

   a = b;
```



### Problem 12
There are several mistakes in the following class definition.
Explain what the mistakes are and show how to correct them.
```java
/* 1*/   public class Liquid
/* 2*/   {
/* 3*/      private int currentTemperature;
/* 4*/
/* 5*/      public Liquid()
/* 6*/      {
/* 7*/         currentTemperature = ct;
/* 8*/      }
/* 9*/
/*10*/      public void getCurrentTemperature(int ct)
/*11*/      {
/*12*/         return ct;
/*13*/      }
/*14*/
/*15*/      public void setCurrentTemperature(int ct)
/*16*/      {
/*17*/         currentTemperature + ct;
/*18*/      }
/*19*/   }
```

### Problem 13
In the Liquid class below, the raiseTemperature() method is
intended to mutate the value of the instance variable currentTemp by
the value of the parameter increase. The method does not work as intended.
Explain what is wrong and show how to correct it.
```java
/* 1*/   public class Liquid
/* 2*/   {
/* 3*/      private int currentTemp;
/* 4*/
/* 5*/      public Liquid(int ct)
/* 6*/      {
/* 7*/         currentTemp = ct;
/* 8*/      }
/* 9*/
/*10*/      public int raiseTemperature(int increase)
/*11*/      {
/*12*/         return currentTemp + increase;
/*13*/      }
/*14*/   }
```

### Problem 14
In the following class, implement two boolean methods
isFrozen() and isBoiling().
```java
public class Liquid
{
    private double freezingPoint;
    private double boilingPoint;
    private double currentTemp;

    public Liquid(double fp, double bp, double ct)
    {
        freezingPoint = fp;
        boilingPoint = bp;
        currentTemp = ct;
    }

    /* write the isBoiling() and isFrozen() methods */

}
```


### Problem 15
Below is the outline of a simple class called BusyWork.
In the blank space provided in the class, add two methods to the class.
The two methods that you add can make use of the two given methods
setNumber() and getNumber().

(a) Add a method increment() that adds 1 to the value of m.


(b) Add a method decrement() that returns a BusyWork object whose
value of m is one less than the value stored in the called object.
This method should not modify the m in the object the method is called on.

```java
   class BusyWork
   {
      int m = 0;

      public void setNumber(int m)
      {
         this.m = m;
      }

      public int getNumber()
      {
         return this.m;
      }

      // write the methods increment() and decrement()


   }//BusyWork
```