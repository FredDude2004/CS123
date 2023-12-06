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
The second for loop multiplies the value on the first half of the array with its mirrored value on the second half of the array. 

### Problem 9
```java
public static int findRepeatedNumber(int[] arr)
{
    boolean found = false;
    int temp = 0;
    for (int i = 1; !found; i++)
    {
        temp = arr[i - 1];
        if (temp == arr[i])
        {
            found = true;
        }
    }
    return temp;
}
```

### Problem 10
1. It names a reference variable rose
2. It creates a new Thing object
3. It makes that reference variable rose point/refer to that Thing object

```java
Thing rose;
rose = new Thing();
```

### Problem 11
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