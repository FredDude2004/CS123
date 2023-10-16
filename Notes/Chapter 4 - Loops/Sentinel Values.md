# Sentinel Values
suppose you wanted to read in a bunch of numbers and find the average. But you don't know how many numbers there are going to be. 
What we can do is just read until there are no more numbers like this 
```java
while (in.hasNextInt())
{
    // compute average
}
```
This would work fine but we don't normally want to do this suppose we had a scenario like this 
<pre>
1 2 3 4 5    6 7 8 9 
</pre>
Where we want to compute the average of the first set of numbers and then the average of the second set of numbers. We can use a 'Sentinel' value, which we can tell the computer when to stop reading the numbers. We would have to ask the user to enter a sentinel value with a statment such as "Enter numbers, -1 to finish: "
<pre>
1 2 3 4 5 -1 6 7 8 9
</pre>
Now we can compute the averages with the sentinel values. 
```java
import java.util.Scanner;

public class AverageOfInputs
{
   public static void main(String[] args)
   {
      Scanner in = new Scanner(System.in);
      int sum = 0;
      int input = in.nextInt();
      int count = 0;
      System.out.print("Enter values, -1 to quit: ");

      while (input != -1)
      {
        sum = sum + input;
        count++;
      }
      int average = sum / count;

      System.out.println("average: " + average);
   }
}
```