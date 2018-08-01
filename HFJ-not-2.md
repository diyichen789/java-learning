# Class and Objects
## A Trip to Objectville
![](https://github.com/diyichen789/java-learning/blob/master/c2.png)

The Shape class is called the superclass of the other four classes. The other four are the subclasses of Shape. The subclasses inherit the methods of the superclass. In other words, if the Shape class has functionality, then the subclasses automatically get that same functionality.

### Thinking about Objects
Things an object knows about itself are called **instance variables**.  
Things an object can do are called **methods**

### Making your first Object
1. Write your class
```java
class Dog{
  int size;
  String breed;
  String name;

  void bark(){
    System.out.println("Ruff!Ruff!")
  }
}
```

2.In your tester, make an object and access the object's variables and methods

```java
class DogTestDrive{
  public static void main(String[] args){
    Dog d = new Dog();
    d.size = 40;
    d.bark();
  }
}

```

## Quick! Get out of main!
> A real Java application is nothing but objects talking to other objects.
In this case, talking means objects calling methods on one another.   
