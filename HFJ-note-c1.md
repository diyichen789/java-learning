# Chapter 1 Dive in A Quick Dip
## Code Structure in java
![](https://github.com/diyichen789/java-learning
/blob/master/java-1-1.png)

Put a class in a source file.   
Put methods in a class.   
Put statements in a method.

## Anatomy of a class
![](https://github.com/diyichen789/java-learning/blob
/master/32dbfaae98bf77ddedcbdc5d1622322.png)

```java
public class MyFirstApp{
  public static void main(String [] args){
    System.out.println("I Rule!");
    System.out.println("I Rule!");

  }
}
```
### Syntax Fun
> Variables are declared with a *name* and a
*type*

#### There are no dumb questions

 Q: In my other language I can do a boolean test
 on a integer. In java, can I say something like:
 ```java
 int x = 1;
 while(x){}
 ```  
 A: ***No***.  
 A boolean and an integer are not compatible types in java. Since the result of a conditional test must be a boolean, the only variable you can directly test(without using a comparison operator) is a ***boolean***. For example, you can say:
 ```java
 boolean isHot = true;
 while(isHot){}
 ```  
 #### println VS print
 > System.out.println inserts a newline while System.out.print keeps printing to the same line.

 #### Note
Never hit the return key when you're typing a String(a thing between "quotes") or it won't compile. 
