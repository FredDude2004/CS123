# September 11th, 2023 Labs
## Lab 1 :
```java
public class Lab1 
{
   public static void main(String[] args) 
   {
      // Figure out what the String values need to be.
      String str1 = "01apple01are great";
      String str2 = "0123 deals";
      String str3 = "01!grape78s";
      String str4 = "skyscrapers";
      String str5 = "01==!=r6";

      // Do not change the following code.
      System.out.println( str1.substring(2, 7) );
      System.out.println( str1.substring(9) );
      System.out.println( str1.substring(13) + str2.substring(4, 10) );
      System.out.println( str3.charAt(10) + str3.substring(3, 8) + str3.charAt(2) );
      System.out.println( str4.substring(0, 5) + str5.substring(3, 6) + str4.substring(5) );
   }
}
/*
The output should look exactly like the following:

apple
are great
great deals
sgrape!
skysc=!=rapers

*/
```
## Lab 2:
```java
public class Lab2
{
   public static void main(String[] args) 
   {
      // Do not change these String values.
      String str1 = "apples";
      String str2 = "coconut tree";
      String str3 = "**!!!==";
      String str4 = "\\--/";

      // Use only String methods on str1 through str4
      // to get the exact output should below.
      System.out.println( str2.substring(0,1) + str1.substring(0,1) + str2.substring(6,7) );
      System.out.println( "" + str4.substring(0,3) + str4.charAt(2) + str4.substring(2,4)  );
      System.out.println( "" + str2.substring(0,7) + str3.charAt(2) + str3.substring(0,2) + str3.charAt(1) + str3.charAt(2) + str2.substring(8,12) );
      System.out.println( str1.substring(0,1).toUpperCase() + str1.substring(1,5) + " " + str2.substring(8,9).toUpperCase() + str2.substring(9) );  
      System.out.println( "" + str2.substring(0,7) + str1.charAt(5) + str3.charAt(3) ) ; 
   }
}
/*
The output should look exactly like the following:

cat
\----/
coconut!***!tree
Apple Tree
coconuts!

*/
```

## Lab 3:
```java
//
// NOTE: You only need to modify line 20 below!
//
public class Reformat1
{
   public static void main(String[] args)
   {
      // A list of phone numbers.
      String[] phoneNumbers = {"(219) 989-2273",
                               "(800) 111-2222",
                               "(123) 456-7890",
                               "(121) 212-1212"};

      // Go through the list of phone numbers.
      for (String n : phoneNumbers)
      {
         // Use String methods on the variable n to reformat
         // each phone number into the form xxx-xxx-xxxx.

         String reformatted = n.substring(1,4) + "-" + n.substring(6);

         System.out.println( reformatted );
      }
      
   }
}
/*
The output should look exactly like this:

219-989-2273
800-111-2222
123-456-7890
121-212-1212

*/
```


## Lab 4:
```java
//
// NOTE: You only need to modify line 20 below!
//
public class Reformat2
{
   public static void main(String[] args)
   {
      // A list of phone numbers.
      String[] phoneNumbers = {"219-989-2273",
                               "800-111-2222",
                               "123-456-7890",
                               "121-212-1212"};

      // Go through the list of phone numbers.
      for (String n : phoneNumbers)
      {
         // Use String methods on the variable n to reformat
         // each phone number into the form (xxx) xxx-xxxx.

         String reformatted = "(" + n.substring(0,3) + ") " + n.substring(4);

         System.out.println( reformatted );
      }
      
   }
}
/*
The output should look exactly like this:

(219) 989-2273
(800) 111-2222
(123) 456-7890
(121) 212-1212

*/
```
## Lab 5:
```java
public class Lab5
{
   public static void main(String[] args) 
   {
      // Figure out what the String values need to be.
      String str1 = "0@       @,";
      String str2 = "0rstuvwxy0";
      String str3 = "4=56=789=dogs=";
      String str4 = "           elephants";
      String str5 = "apples";
      String str6 = "pears";

      // Do not change the following code.
      int n1 = str1.indexOf("@");
      int n2 = str1.lastIndexOf("@");
      System.out.println( str2.substring(n1, n2) );
      char c1 = '=';
      char c2 = str1.charAt(10);
      System.out.println( str3.replace(c1, c2) );
      System.out.println( str4.substring(str1.length()) );
      System.out.println( str5.concat(" are not as good as " + str6) );
   }
}
/*
The output should look exactly like the following:

rstuvwxy
4,56,789,dogs,
elephants
apples are not as good as pears

*/
```


