# December 4th, 2023 Labs
## Lab 1
Modify the Counter class from last week so that each Counter object has a limiting value on how high it can count.

Write a method called setLimit that takes an integer value. The value of this method's parameter should be used to set the Counter object's limiting value field.

If a Counter object has reached it's limiting value and it's count() method is called, then the count() method should not increase the counter's value. Instead, the count() method should print an error message that says "Limit exceeded!".

The limiting value for a counter should default to 10. That is, if a Counter object is constructed but setLimit is not called on it, then the limiting value on that Counter object is 10.

You do not need to write any code that calls your methods. Your methods will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 3. The Tester.java program then runs one of its three built in test cases.

Note: You can test your Counter methods by copying your Counter class into the Java Visualizer, as we did in class.

```java
/**
   This class models a tally counter with a limiting value.
   
   The limiting value defaults to 10.
*/
public class Counter
{
   private int value;
   private int limit = 10;
   
   public void setLimit(int n)
   {
      limit = n;
   }

   /**
      Advance the value of this Counter object by
      1 as long as the counter has not reached
      its limit. Otherwise, this method prints
      an error message.
   */
   public void count()
   {
      if (value < limit) {value++;}
      else {System.out.println("Limit exceeeded!");}
     
     
   }

   /**
      Reset the value of this Counter object to 0.
   */
   public void reset()
   {
      value = 0;
   }

   /**
      Gets the current value of this Counter object.
      @return the current value
   */
   public int display()
   {
      return value;
   }


   /**
      Set the limiting value on this Counter object.
      @param max  an integer value for this Counter's limit
   */
}
```

## Lab 2
Modify the CashRegister class so that it keeps track of the total number of items sold to all the cutomers, the total amount purchased by all the customers, and the numuber of customers.

The CashRegister should consider each call to the clear() method as the signal to count one customer (the cash register must be cleared after one customer is finished and before another customer can begin).

Write a method called reset() that sets to zero all the values that the cash register keeps track of.

Write methods getTotalSales(), getTotalItemCount(), and getCustomerCount() that return the appropriate fields of the cash register.

You do not need to write any code that calls your methods. Your methods will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 3. The Tester.java program then runs one of its three built in test cases.

Note: You can test your CashRegister methods by copying your CashRegister class into the Java Visualizer, as we did in class.
```java
/**
   A simulated cash register that tracks a customer's item count,
   the custormer's total amount due, the number of customer's served,
   the total number of items sold, and the total value of all items sold.
*/
class CashRegister
{
   private int ItemCount, TotalItemCount, CustomerCount = 0;
   private double Sales, TotalSales = 0.0;

   /**
      Adds an item to this cash register.
      @param price the price of this item
   */
   public void addItem(double price)
   {
      Sales += price;
      TotalSales += price;
      ItemCount++;
      TotalItemCount++;
   }

   /**
      Gets the price of all items in the current sale.
      @return the total amount
   */
   public double getTotal()
   {
      return Sales;
   }
   
   /**
      Gets the number of items in the current sale.
      @return the item count
   */
   public int getCount()
   {
      return ItemCount;
   }

   /**
      Clears the current customer's item count and amount due.
   */
   public void clear()
   {
      Sales = 0.0;
      ItemCount = 0;
      CustomerCount++;
   }

   /**
      Gets the total sales for all customers.
      @return the total sales value
   */
   public double getTotalSales()
   {
      return TotalSales;
   }
   
   /**
      Gets the total number of items for all customers.
      @return the total number of items sold
   */
   public int getTotalItemCount()
   {
      return TotalItemCount;
   }

   /**
      Gets the number of customers who have purchased items.
      @return the number of customers
   */
   public int getCustomerCount()
   {
      return CustomerCount;
   }
   
   /**
      Clears the customer's item count and amount due and
      also resets the customer count, the total item count,
      and the total sales value.
   */
   public void reset()
   {
      TotalSales = 0;
      TotalItemCount = 0;
      CustomerCount = 0;
   }
}
```

## Lab 3
Implement the Point and Circle classes that are outlined below.

Implement each class method according to the method's given Javadoc comment.

You do not need to write any code that calls your methods. Your methods will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 3. The Tester.java program then runs one of its three built in test cases.

```java
/**
   This class represents points in the plane.
*/
class Point
{
   private double x = 0.0;
   private double y = 0.0;

   /**
      Change this Point object to have the given x-coordinate.

      @param newX  new x-coordinate for this Point object
   */
   public void setX(double newX)
   {
      x = newX;
   }

   /**
      Get the x coordinate of this Point object.

      @return this Point's x-coordinate
   */
   public double getX()
   {
      return x;
   }

   /**
      Change this Point object to have the given y-coordinate.

       @param newY  new y-coordinate for this Point object
   */
   public void setY(double newY)
   {
      y = newY;
   }

   /**
      Get the y-coordinate of this Point object.

      @return this Point's y-coordinate
   */
   public double getY()
   {
      return y;
   }

   /**
      Determine if this Point object has the same x-coordinate
      and the same y-coordinate as the given Point.

      @param p  a reference to a second Point object
      @return true if the given Point is equal to this Point
   */
   public boolean equals(Point p)
   {
      boolean Same = false;
      if (p.getX() == x && p.getY() == y) {Same = true;}
      return Same;
   }

   /**
      Determine which quadrant of the plane this Point is in.
      Quadrant 1 has positive x and y coordinates.
      Quadrant 2 has negative x coordinates and positice y coordinates.
      Quadrant 3 has negative x and y coordinates.
      Quadrant 4 has positive x coordinates and negative y coordinates.

      Note: The positive x and y axes are in quadranr 1.
            The negative x axis is in quarant 2.
            The negative y axis is in quadrant 3.

      @return the quadrant number of this Point object
   */
   public int quadrant()
   {
      int Quadrant = 0;
      if (x > 0 && y > 0) {Quadrant = 1;}
      if (x < 0 && y > 0) {Quadrant = 2;}
      if (x < 0 && y < 0) {Quadrant = 3;}
      if (x > 0 && y < 0) {Quadrant = 4;}
      return Quadrant;
   }


   public String toString()
   {
      return "Point: [" + x + ", " + y + "]";
   }
}


/**
   This class represents circles in the plane.
*/
public class Circle
{
   private Point center = null;
   private double radius = 0.0;
   
   public void setCenter(Point center)
   {
      this.center = center;
   }
   
   public Point getCenter()
   {
      return center;
   }
   
   public void setRadius(double r)
   {
      radius = r;
   }
   
   public double getRadius()
   {
      return radius;
   }


   /**
      Translate the center of this circle by the given
      amounts in the x and y directions.
   
      @param dx how much to move the center in the x direction
      @param dy how much to move the center in the y direction
   */
   public void translateBy(double dx, double dy)
   {
      center.setX(center.getX() + dx);
      center.setY(center.getY() + dy);
   }


   public String toString()
   {
      return "Circle: r = " + radius + ", center = [" + center.getX() + ", " + center.getY() + "]";
   }
}
```
