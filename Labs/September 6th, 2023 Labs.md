# September 6th, 2023 Labs

## Lab 1 
```java
import java.awt.Color;

public class Lab0
{
   public static void main(String[] args)
   {
      World world = new World(600, 600);

      Turtle t1 = new Turtle(world);
      t1.turnRight();
      t1.forward(250);
      t1.penUp();
      t1.backward(250);
      t1.penDown();
      t1.setColor(Color.red);
      t1.backward(250);
      t1.moveTo(300,300); t1.setColor(Color.green); 
      t1.turnLeft();
       
      world.show(true);
   }
}
```
[Output](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/lab1.png)
## Lab 2
```java
import java.awt.Color;

public class Lab0
{
   public static void main(String[] args)
   {
      World world = new World(600, 600);

      Turtle t1 = new Turtle(world);
       
      t1.forward(250); t1.backward(250);
      t1.setColor(Color.red);
      t1.moveTo(550,300); t1.moveTo(300,300);
      t1.setColor(Color.blue);
      t1.moveTo(300,550); t1.moveTo(300,300);
      t1.setColor(Color.black);
      t1.moveTo(50,300); t1.moveTo(300,300);
      t1.setColor(Color.green);
      t1.moveTo(300,300);
       
      world.show(true);
   }
}
```
[Output](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/lab2.png)
## Lab 3 
```java
import java.awt.Color;

public class Lab0
{
   public static void main(String[] args)
   {
      World world = new World(600, 600);
      
        Turtle t1 = new Turtle(world);

      t1.moveTo(550,300); t1.setPenWidth(5);
      t1.moveTo(550,50); t1.setPenWidth(10);
      t1.moveTo(300,50); t1.setPenWidth(15);
      t1.moveTo(300,300); 
       
      world.show(true);
   }
}
```
[Output](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/lab3.png)
## Lab 4 
```java
import java.awt.Color;

public class Lab0
{
   public static void main(String[] args)
   {
      World world = new World(600, 600);
      
        Turtle t1 = new Turtle(world);
       
       t1.turnRight(); t1.forward(100); t1.penUp();
       t1.forward(50); t1.penDown(); t1.forward(100);
       
       t1.turnLeft(); t1.forward(100); t1.penUp();
       t1.forward(50); t1.penDown(); t1.forward(100);
       
       t1.turnLeft(); t1.forward(100); t1.penUp();
       t1.forward(50); t1.penDown(); t1.forward(100);
       
       t1.turnLeft(); t1.forward(100); t1.penUp();
       t1.forward(50); t1.penDown(); t1.forward(100);

      
       
      world.show(true);
   }
}
```
[Output](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/lab4.png)
## Lab 5 
```java
import java.awt.Color;

public class Lab0
{
   public static void main(String[] args)
   {
      World world = new World(600, 600);
      
       Turtle t1 = new Turtle(400,300, world);
       Turtle t2 = new Turtle(300,200, world); t2.setColor(Color.red);
       Turtle t3 = new Turtle(100,400, world); t3.setColor(Color.blue);
       Turtle t4 = new Turtle(200,500, world); t4.setColor(Color.black);
       
       t1.turnRight(); t2.turnRight(); t3.turnRight(); t4.turnRight();
       
       t1.forward(100); t1.turnLeft();
       t1.forward(100); t1.turnLeft();
       t1.forward(100); t1.turnLeft();
       t1.forward(100); t1.turnLeft(); t1.turnLeft();
       
       t2.forward(100); t2.turnLeft();
       t2.forward(100); t2.turnLeft();
       t2.forward(100); t2.turnLeft();
       t2.forward(100); t2.turnLeft(); t2.turnLeft();
       
       t3.forward(100); t3.turnLeft();
       t3.forward(100); t3.turnLeft();
       t3.forward(100); t3.turnLeft();
       t3.forward(100); t3.turnLeft(); t3.turnLeft();
       
       t4.forward(100); t4.turnLeft();
       t4.forward(100); t4.turnLeft();
       t4.forward(100); t4.turnLeft();
       t4.forward(100); t4.turnLeft(); t4.turnLeft();
       
      world.show(true);
   }
}
```
[Output](http://math.pnw.edu/~rlkraft/cs12300/from-class/2023-09-06/lab5.png)