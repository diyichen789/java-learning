# Methods use instance variables
## How Objects Behave   

Remember: a class describe what an object ***knows*** and what an object ***does***   

 Every instance of a particular class has the same methods, but the methods can behave differently based on the value of the instance variables.  

 ### You can send things to a method  
 A method uses parameters. A caller passes arguments.
 > Arguments are the things you pass into the methods. An argument(a value like 2, "Foo", or a reference to a Dog)lands face-down into a *parameter*  

 ![](https://github.com/diyichen789/java-learning/blob/master/c4-1.png)

 ### You can get things back from a method  
 ```java
    int giveSecret(){
      return 42;
    }
 ```
 If you declare a method to return a value, you must return a value of the declared type!
 ![](https://github.com/diyichen789/java-learning/blob/master/c4-2.png)  
 ### You can send more than one thing to a method
 ### Java is pass-by-value. That means pass-by-copy
 ![](https://github.com/diyichen789/java-learning/blob/master/c4-3.png)
 ### Cool things you can do with parameters and return types
 ![](https://github.com/diyichen789/java-learning/blob/master/c4-4.png)
 ```Java
 public class Electricguitar {
     int numOfPickups;
     String brand;
     boolean rockStarUsesIt;

     String getBrand(){
         return brand;
     }

     void setBrand(String newBrand){
         brand = newBrand;

     }
     int getNumOfPickups(){
         return numOfPickups;
     }
     void setNumOfPickups(int newNumber){
         numOfPickups = newNumbwe;
     }
     boolean getRockstarUsesIt(){
         return rockStarUsesIt;
     }
     void setRockStarUsesIt(boolean trueorfalse){
         rockStarUsesIt = trueorfalse;
     }
 }
 ```  
 ### Encapsulation(封装)  
 ```Java
  public void setHeight(int ht){
    if(ht>9){
      height = ht;
    }
  }
 ```

 > Make instance variables private
 > Make getters and setters public  

 Any place where a particular value can be used, a method call that returns that type can be used.  
```Java
  // instead of:
  int x = 3+24;
  // you can say:
  int x = 3+one.getSize();
```
### Declaring and initializing instance variables
> Instance variables always get a default value. If you don't explicitly assign a value to an instance variable, or you don't call a setter method, the instance variable still has a value!  

|type|value|
|-----|-----|
|intergers|0|
|floating points|0.0|
|booleans|false|
|references|null|

### The difference between instance and local variables

1.Instance(实例变量) variables are declared inside a class but no within a method.
```Java
  class Horse{
    private double height = 15.2;
    private String breed;
  }
```
2.Local variables are declared within a method.
```java
  class AddThing{
    int a;
    int b =12;
    public int add(){
      int local = a+b;
      return total;
    }
  }
```
3.Local variables MUST be initialized before use!
![](https://github.com/diyichen789/java-learning/blob/master/c4-5.png)  

### Comparing variables(primitives or references)
> Use "==" to compare two primitives or to see if two references refer to the same object.
> Use the "equals()" method to see if two different objects are equal.
