Problems in Shivam's OOP Solution:
1. Encapsulation is not present as data(i.e coordinates of points) and the behavior
(i.e finding distance and direction between origin point and destination point) are not 
binded together.
2. Class Point has getter and setter functions whose only task is to set and get the value 
of x and y coordinates of points.

Changes made:
1. Binding of data and behavior in class Point- deleted class DistanceAndDirectionCalculator 
as it had behaviors(methods) that has already been included in class Point.
2. Removal of getter and setter functions.

Further Thoughts:
1. I wanted to keep the class DistanceAndDirectionCalculator with the methods distance
and direction, and keep the data inside it in the form of class Point
(i.e class Point inside class DistanceAndDirectionCalculator) so that I can use this class
to find distance and direction between two lines as well!! Is it a good option?

Given Task:
So Shivam had just learned about OOP. He had written a program before that did two things,
- Find distance between two points
- Find direction (angle) between two points in Radians.

He has this code in the `org.procedural.DistanceAndDirectionCalculator` It looks like this for the reference - 

```java
public class DistanceAndDirectionCalculator {
    public static double distance(double x1, double y1, double x2, double y2) {
        double xDistance = x1 - x2;
        double yDistance = y1 - y2;
        return Math.sqrt(Math.pow(xDistance, 2) + Math.pow(yDistance, 2));
    }

    public static double direction(double x1, double y1, double x2, double y2) {
        double xDistance = x2 - x1;
        double yDistance = y2 - y1;
        return Math.atan2(yDistance, xDistance);
    }
}
```
He thought it'll be a good idea to convert this to Object Oriented Programming. So he wrote a new implementation in package `org.oop`, he got 2 classes - 
- `org.oop.DistanceAndDirectionCalculator`
- `org.oop.Point`

However, his trainer told him that what he did is not Object Oriented programming and asked Shivam to try again. 
- Try to articulate problems with Shivam's OOP solution. (Write it somewhere and share it with your trainer)
- Fork the project and fix the design related problem with Shivam's OOP solution. Share that with your trainer too.