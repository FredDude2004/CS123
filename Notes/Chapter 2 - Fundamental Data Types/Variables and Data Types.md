# Variables and Data Types
Here is a reading that explains variables and the different data types <br>
[Variables and Data Types](https://runestone.academy/ns/books/published/csjava/Unit1-Getting-Started/topic-1-3-variables.html)

## Example Code From Class 
```java
public class Examples
{
   public static void main(String[] args)
   {
      int x; // declaring x
      //System.out.println( x ); // x doesn't have a value (yet)
      x = 7;
      System.out.println( x );
      x = 10;
      double Y = 2.7;   // declaring y AND initializing y
      double z = 56.9;
      boolean b = false;
      String str = "hello class";
      str = "whats up";
      int x2 = x;         // x2 is a copy of x
      double y2 = Y;      // y2 is a copy of Y
      String str2 = str;  // str2 is not really a copy of str
      str = "bye class";
      //str2 = str;
      System.out.println( str2 );
      System.out.println( str );

      System.out.println(2 + 2 + "cat" );
      System.out.println("cat" + 2 + 2 );
      System.out.println("cat" + (2 + 2) );
   }
}
```