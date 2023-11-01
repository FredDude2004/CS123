# Methods
There are words that we use when describing methods that we have to understand. 

### <b>Method Definition:</b>
 Just like in math we need to define a method, or in math we call it a 'function'.

<pre>
f(x) = x<sup>2</sup> + x + 2 
</pre>

### <b>Method Call:</b>
 Now that we have a method defined we need to 'call' it, in math we would do that like this ->

<pre>
f(3)
</pre>
This would 'call' the method and it would do this ->
<pre>
f(3) = (3)<sup>2</sup> + (3) + 2 
f(3) = 14</pre>
We called the functiona and it returned us a value. 

### <b>Formal Parameter:</b>
 The formal parameter in this case would be the 'x' in f(x)

<pre>        f(x)
          |
    Formal Parameter
</pre>

### <b>Actual Parameter:</b>
 The actual parameter would be '3'
<pre>        f(3)
          |
    Actual Parameter
</pre>

### <b>Return Value:</b>
 The return value is what the method gives back to the main class. In this case its 14.

<pre>
f(3) = (3)<sup>2</sup> + (3) + 2 
f(3) = 14
       |
  Return Value
</pre>

### <b>Parameter Type:</b>
 Parameter type is what data type the parameter is, in this case its an 'int'.

### <b>Return Type:</b>
 The data type of the return value, which in this case is also 'int'. 

Heres what all of this would look like in Java: 
```java
public class Formula {
    public static void main(String[] args) {
        System.out.println(f(3));   // method call
    }

    public static int f(int x) {    // method definition
        int y = x * x;      // y is a local variable
        return y + x + 2;   // x^2 + x + 2
    }
}
```
We could get really fancy like this:
```java
public class Formula {
    public static void main(String[] args) {
        int w1 = 1 + f(3);      // method call
        int w2 = f(3) + f(4);   // method calls
        int w3 = f(f(5));       // method composition
        int w4 = f(f(f(6)));    // method composition
    }

    public static int f(int x) { // method definition
        int y = x * x;    // y is a local variable
        return y + x + 2;     // x^2 + x + 2
    }
}
```
Theres a big difference between a method and a variable: 

<b>Varable:</b> A memory location that holds a value

<b>Method:</b> Instructions for what to do
