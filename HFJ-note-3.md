# Chapter 3 primitives and reference
## Know Your Variables
### Primitive Types

|Type|BitDepth|Value Range|
|-----|-----|-----|
|boolean|JVM-specified|true or false|
|char|16 bits|0 to 65535|
|byte|8 bits|-128 to 127|
|short|16 bits|-32768 to 32767|
|int|32 bits| -2147483648 to 2147483647|
|long| 64 bits|-huge to huge|
|float| 32 bits| varies|
|double| 64 bits| varies|

### Primitive declarations with assignments:
> double d = 3456.98  
> char c = 'f'  
> float f = 32.5f

**Back away from that keyword!**  

## Object reference
### Controlling your Dog object
+ There is  actually no such thing as an OBJECT variable
+ There's only an object reference variable.
+ An object reference variable holds bits that represent a way to access an Object
+ It doesn't hold the object itself, but it holds something like a pointer. Or an address. Except, in Java we don't really know what is inside a reference variable. We do know that whatever it is, it represents one and only one object. And the JVM knows how to use the reference to get to the object.  

### Controlling your Dog object
```Java
myDog.bark();
```
means, "use the object referenced by the variable myDog to invoke the bark() method"

#### The three steps of object declarations, creation and assignment
![](https://github.com/diyichen789/java-learning/blob/master/c3-1.png)
1. Declare a reference variable  
2. Create an object  
3. Link the object and the reference

### Objects on the heap
#### Life and death on the heap
```Java
b = c;
```
![](https://github.com/diyichen789/java-learning/blob/master/c3-2.png)
Both b and c refer to the same object. Object 1 is abandoned and eligible for Garbage Collector(GC).
>+ Active reference: 2
>+ Reachable Objects: 1
>+ Abandoned Objects: 1

The first object that b referenced, object 1, has no more references. It's ***unreachable***
***
```Java
c = null;
```
Object 2 still has an active reference(b), and as long as it does, the object is not eligible for GC.
>+ Active Reference: 1
>+ null Reference: 1
>+ Reachable Objects: 1
>+ Abandoned Objects: 1

![](https://github.com/diyichen789/java-learning/blob/master/c3-3.png)  

### An array is like a tray of cups
```Java
  int[] nums = new int[7];
  num[0] = 6;
  ...
  num[6] = 1;
```
> Remember elements in an int array are just int variables.

### Make an array of Dogs
1. Declare a Dog array variable and create a new Dog array with a length of 7, and assign it to the previously-declared Dog[] variable pets.
```Java
Dog[] pets = new Dog[7];
```
#### What's missing ?
Dogs! We have an array of Dog references, but no actual Dog objects!
 
2. Create new Dog objects, and assign them to the array elements.
Remember, elements in a Dog array are just Dog reference variables. We still need Dogs!
```Java
  pets[0] = new Dog();
  ...
  pets[6] = new Dog();
```
![](https://github.com/diyichen789/java-learning/blob/master/c3-4.png)

### Exercise
Note that an array start with index 0.
