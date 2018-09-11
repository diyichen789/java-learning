#Homework 1
## ME570 Yichen Di
### September, 10th, 2018
#### Question 1.1
I use a for-loop to make a traversal of all vertex in vertices. And I call the function polygon_isFilled to make a patch.

#### Question 1.2
I use a for-loop to compute the sum of the angle of the polygon to decide if it is filled in. (according to the hint)

#### Question 1.3
I implement this function according to the hint, and also discuss several situation:  
1. the edge length is zero.
2. one of the slope is infinite
3. two edge is parallel.

#### Question 1.4 (provided)
#### Question 1.5
Because
$$cAngle = vec1'*vec2$$
$$\vec {v_1}\cdot \vec{v_2} = |v_1||v_2|cos\theta$$
And
$$vec1 = \frac { vec1 } { normVec1 } $$
So in this case
$$|vec1| = |vec2| =1$$
$$cos\theta = vec1 * vec2$$
So, cAngle indicate the cosine value of the angle which formed by vec1 and vec2

*****
Because
$$sAngle = [0;0;1]'*cross([vec1;0],[vec2;0])$$
$$|vec1| = |vec2| =1$$
And
$$\vec {v_1}\times \vec{v_2} = |v_1||v_2|sin\theta$$
So, obviously sAngle indicates the sine value of the angle formed by vec1 and vec2.

*****
Theta is computed as follows:
$$tan\theta = \frac{ sin\theta }{ cos\theta }$$
$$\theta = arctan(\frac{ sin\theta }{ cos\theta })$$
And we already got the value of cAngle and sAngle. So just plug in the value we can get the result.   
There is a tiny tricks to deal with the 'unsigned' situation: By using $mod(edgeAngle+2\pi,2\pi)$, we make sure that the interval of theta is $[0,2\pi)$

#### Question 1.6
Using the function **edge_angle()** to check the angle, and it returns true if it is occulated or invisible.

#### Question 1.7 (optional)
#### Question 1.8
This function combine the result of function **poly_isSelfOccluded()** and function **edge_isCollision()**.
The output of function **polygon_isSelfOccluded()** is true if and only if the outputs of the two function mentioned above are both false.

#### Question 1.9 (provided)
#### Question 1.10 (optional)
#### Question 1.11

#### Question 1.12
I implement this function according to the hint.
#### Question 1.13(optional)
#### Question 1.14
First, using 5 testpoints:

Moreover, using 100 testpoints:

Last, revise the function to display a random triangle and test it with 100 random points:

####Question 3.1

####Question 4.1
30 hours!
####Question 4.2(optional)
The easy part is that I am good at coding and math, and I am familiar with the data structure priority queue.

The hard part is that although I am good at coding, I am annoyed with the Matlab syntax because I have used Java and python for a long time.
