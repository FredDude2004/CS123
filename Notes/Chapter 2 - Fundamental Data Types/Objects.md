# Objects 
[Instances of Classes](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-1-objects-intro-turtles.html) <br>
[Creating and Initializing Objects: Constructors](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-2-constructors.html) <br>
[Calling Object Methods Without Parameters](https://runestone.academy/ns/books/published/csjava/Unit2-Using-Objects/topic-2-3-methods-no-params.html) <br>

## Turtle Graphics and Turtle Methods 
[Turtle Methods Help Sheet](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/Turtle-methods.txt) <br>
```java

import java.awt.Color;
public class TurtleGraphics
{
   public static void main(String[] args)
   {
      World world = new World(500, 500);

      Turtle t1 = new Turtle(world);

      t1.forward(100);
      t1.turnLeft();
      t1.forward(100);

      t1.setColor(Color.red);
      t1.forward(100);

      t1.setHeight(40);
      t1.setWidth(40);

      t1.turnToFace(250, 250); // (250, 250) is the center of the World

      System.out.println( t1.getDistance(250, 250) ); // (250, 250) is the center of the World
      System.out.println( t1.getDistance(0, 0) );     // (0, 0) is the upper left-hand corner

      System.out.println( "(" + t1.getXPos() + ", " + t1.getYPos() + ")" );

      System.out.println( t1.getName() );
      t1.setName( "redTurtle" );
      System.out.println( t1.getName() );

      world.show(true);
   }
}

```