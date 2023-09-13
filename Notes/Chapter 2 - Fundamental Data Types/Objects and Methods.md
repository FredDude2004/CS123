# Objects and Methods
### 9/11/2023 CS123 JAVA LEC

Objects are like the turtles and the methods are the data that you use to manipulate the object 

```javaScript
t1.backward(3.5)
```

(comment): it has to be an integer in the method, it wont allow a double 
so you would need to write for example

```javaScript
t1.backward(3)
```

the coordinates have to be ints, they can not be inbetween two integers 

```javaScript 
penDown()
penUp() 
```

(comment): these are methods, so they have to be called onto a specific object
if I just leave it as it is right now there will be an error message bcause you haven't 
called onto an object

Strings are objects as well 

Ex. of turtle calling methods
```javaScript
public class TurtleGraphics
{
  public static void main(String[] args)
  {
	World world = new World(300,300);
	Turtle yertle = new Turtle(world);

	yertle.forward();
	yertle.getXPos();
	yertle.getYPos();

	world.show(true);
  }
}
```
(comment): notice how we ask for the information, x cord and y cord, but we didn't do anything with the information
we didnt store it or use it, so it just dissapears into the ether, never to be seen again

```javaScript
public class TurtleGraphics
{
  public static void main(String[] args)
  {
	World world = new World(300,300);
	Turtle yertle = new Turtle(world);

	yertle.forward();
	System.out.println(yertle.getXPos());
	System.out.println(yertle.getYPos());

	world.show(true);
  }
}
```
(comment): this will report the data out to us so that way it won't just disappear. 


```javaScript
public class TurtleGraphics
{
  public static void main(String[] args)
  {
	World world = new World(300,300);
	Turtle yertle = new Turtle(world);

	yertle.forward();
	System.out.println(yertle.getXPos() + "," + yertle.getYPos());

	world.show(true);
  }
}
```
(comment): This will print it out in a way that is easier to understand

#Weird Quirks With Numbers in Java

```javaScript
public class ClassNameHere
{
   public static void main(String[] args) 
   {
      System.out.println( + - + - - + 5);
   }
}
```
(comment): This prints out the integer -5, because the pluses in front of the number don't do anything 
you can't use the increment operator or decrament oporator on an integer, you can only use it on variables

```javaScript
public class ClassNameHere {
   public static void main(String[] args)
   {
      String s1 =  "hello";
      String s2 =  "bye";
      String s3 =  "apples";
   }
}
```




