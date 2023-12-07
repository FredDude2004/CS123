### Problem 1
There will be an error, because indices start counting from zero and the length of the array starts counting from one. So it will go out of bounds and print nothing. 

### Problem 2 
```java
for (int i = 0; i < arr.length; i++){
    arr[i] *= 10;
}
```

### Problem 3

```java
int[] arr;
arr = new int[11];
      
for (int i = 0; i < arr.length; i++)
{
    arr[i] = -50 + (i * 10);
}
```

### Problem 4 
```java
public static double sumArray(double[] arr)
{
    double sum = 0.0;
    for (int value : arr)
    {
        sum += value;
    }
    return sum;
}
```

### Problem 5
```java
public static double sumSubArray(double[] arr, int a, int b)
{
    double sum = 0.0;
    if (arr.length > a && arr.length > b && a >= 0 && b >= 0)
    {
        if (a < b)
        {
            for (int i = a; i <= b; i++)
            {
                sum += arr[i];
            }
        }
        else
        {
            for (int i = b; i <= a; i++)
            {
                sum += arr[i];
            }
        }
    }
    return sum;
}
```

### Problem 6
<pre>
        +---+---+
a ->    | 1 | 4 |
        +---+---+
            ^
b ----------^
</pre>
```java
b[0] = 1
b[1] = 4
```

### Problem 7
<pre>
              +----+----+----+---+
c ------->    | 21 | 11 | 10 | 9 |
              +----+----+----+---+

              +---+---+---+---+---+
a, b, d ->    | 0 | 0 | 0 | 0 | 0 | 
              +---+---+---+---+---+
</pre>

### Problem 8

### Problem 9

### Problem 10
The second for loop multiplies the value on the first half of the array with its mirrored value on the second half of the array. 

### Problem 11
```java
public static int findRepeatedNumber(int[] arr)
{
    for (int i = 0; i < arr.length; i++)
    {
        for (int j = 0; j < arr.length; j++)
        {
            if (arr[i] == arr[j])
            {
                return arr[i];
            }
        }
    }
}
```

### Problem 12
1. It names a reference variable rose
2. It creates a new Thing object
3. It makes that reference variable rose point/refer to that Thing object

```java
Thing rose;
rose = new Thing();
```

### Problem 13
```java
   b.x = 5; // Not OK, x is not a method that you can call

   int u = a.getY(); // Not OK, getY returns a double

   double v = b.getX(); // OK

   a.setX(3.2); // Not OK, setX takes in an int not a double

   b.getY(); // OK

   double w = b.setY(4.5); // Not OK, setY doesn't have a return statment

   int x = Thing.methodA(); // Not OK, Thing is not a reference variable

   int y = a.methodB(5); // Not OK, methodB returns a double 

   a = b.methodA(); // Not OK, a is a thing Object you can't set it equal to an int

   a = b; // OK
```

### Problem 14
```java
/* 1*/   public class Liquid // dpesn't need public --> class Liquid
/* 2*/   {
/* 3*/      private int currentTemperature;
/* 4*/
/* 5*/      public Liquid() // needs an argument --> public Liquid(int ct)
/* 6*/      {
/* 7*/         currentTemperature = ct;
/* 8*/      }
/* 9*/
/*10*/      public void getCurrentTemperature(int ct) // needs a return type and doesn't need an argument --> public int getCurrenttemperature()
/*11*/      {
/*12*/         return ct; // return this.currentTemperature;
/*13*/      }
/*14*/
/*15*/      public void setCurrentTemperature(int ct)
/*16*/      {
/*17*/         currentTemperature + ct; // you need to set the temp not add to it --> currentTemperature = ct;
/*18*/      }
/*19*/   }
```

### Problem 15
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
/*10*/      public int raiseTemperature(int increase) // don't need a return type --> public void raisTemperature(int increase)
/*11*/      {
/*12*/         return currentTemp + increase; // don't need to return anything but you need to multiply currentTemp --> currentTemp *= increase;
/*13*/      }
/*14*/   }
```

### Problem 16
```java

Problem 16) In the following class, implement two boolean methods
isFrozen() and isBoiling().

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
    public boolean isBoiling()
    {
        boolean boiling = false;
        if (this.currentTemp >= this.boilingPoint)
        {
            boiling = true;
        }
        return boiling;
    }

    public boolean isFrozen()
    {
        boolean frozen = false;
        if (this.currentTemp <= this.freezingPoint)
        {
            frozen = true;
        }
        return frozen;
    }
}
```

### Problem 17
```java
   class BusyWork
   {
      private int m = 0;

      public void setNumber(int m)
      {
         this.m = m;
      }

      public int getNumber()
      {
         return this.m;
      }

      // write the method increment()
      public void increment()
      {
        this.m++;
      }
    
      // write the method decrement()
      public BusyWork decrement()
      {
        BusyWork bw = new BusyWork();
        bw.setNumber(this.m - 1);
        return bw;
      }
   }
   //BusyWork
   ```
