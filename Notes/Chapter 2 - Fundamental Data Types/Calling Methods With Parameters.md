# Calling Methods With Parameters and Return Values
## Strings and String Methods

[Calling Methods With Parameters](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-4-methods-with-params.html) <br>
[Calling Methods that Return Values](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-5-methods-return.html) <br>
[Strings](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-6-strings.html) <br>
[String Methods](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-7-string-methods.html) <br>

[String Methods Cheat Sheet](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-11/Some_useful_methods_of_String_objects_v2.pdf)

### Turtle Graphics Example
```java 
public class TurtleGraphics
{
  public static void main(String[] args)
  {
      World world = new World(300,300);
      Turtle yertle = new Turtle(world);

      yertle.forward();

      System.out.println( yertle.getXPos() + "," + yertle.getYPos() );

      System.out.println( yertle.getName() );
      yertle.setName("");
      System.out.println( yertle.getName() );
      yertle.setName("I have no name");
      System.out.println( yertle.getName() );
      yertle.setName("sally");
      System.out.println( yertle.getName() );

      double d = yertle.getDistance(0, 0);
      System.out.println( d );

      world.show(true);
  }
}



public class ClassNameHere
{
   public static void main(String[] args)
   {
      System.out.println(  + +-+- -+5 );
   }
}
```

# String Methods Examples
```java
public class StringCode
{
   public static void main(String[] args)
   {
      //           01234
      String s1 = "hello";
      String s2 = "bye";
      String s3 = "apples";
      //           012345

      System.out.println( s1.length() );
      System.out.println( s2.length() );

      System.out.println( s1.substring(1, 3) );
      System.out.println( s1.substring(2) );

      System.out.println( (s1 + s3).length() );
      System.out.println( (s1 + s3).substring(2, 9) );

      System.out.println( s3.toUpperCase() );    // this doesn't change s3
      System.out.println( s1.replace('l','#') ); // this doesn't change s1
   }
}
```
