# Introduction to Design Patterns

This is a small guide to help you understand Adapter Design Pattern


# Adapter Design Pattern
We already learned that structural design patterns represent the composition of classes and objects, so let’s review one of them,the adapter pattern

“This pattern allows the interface of an existing class to be used as another interface. It is often used to make existing classes work with others without modifying their source code.”

In other words:

Adapter pattern converts the interface of a class into an interface that is required by the client. 
The design pattern enables the classes of incompatible interfaces to work together in a single program. 
In the adapter design pattern, you write a class that has a desired interface and communicates with the class of a different interface. 

# The advantages of using the adapter design pattern are:
It enables two or more incompatible objects to interact with each other.
It makes an existing functionality reusable.

It’s like this adapter.. it’s a ‘bridge’ between two objects
![alt text][adapter]

[adapter]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/adapterImage.png


Let’s practice, we are going to follow a pretty simple example that helped me to understand this pattern easily, we are not going to adapt complex classes/objects since the goal here is to understand the pattern itself.
The goal is to follow the example and create it with any language you’re like to try.
If you don’t have anything installed at this moment, you can try with the C# code in examples and this page csharppad.com
I’m placing some code examples in C#, they are really expressive and it should be easy to read, but if you never worked with C# before and have questions about what it’s doing then you can ask me, also you can work in teams.


# 1 Create a class for a Rectangle
![alt text][rectangle]

[rectangle]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/rectangle.png

# 2 Create a class for Operations
![alt text][operations]

[operations]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/Operations.png


# 3 we calculate the Rectangle area 
We can do this by consuming current method in Operations class… 
![alt text][GetARea]

[GetArea]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/initialMain.png

so far so good, right?


but now we add the new class for a square
# 4 create a class for square
![alt text][Square]

[Square]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/square.png


if we want to calculate Square’s area, we can not do it with the current method in Operations class since we only have the value of one size and our method is expecting to have 2 values, one for the width and one for the height.

# 5 we create an adapter 
the adapter is going to assign to width and height the same value in our square size, we know square’s sizes are the same value and we can reuse the formula in rectangle are by simply converting the square in a rectangle object and passing the size value in both parameters.

![alt text][AreaAdapter]

[AreaAdapter]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/adapter.png



# 6 Now we can consume it to get our results:
![alt text][execution]

[execution]: https://github.com/JannethAmaya/DesignPatternsIntro/blob/master/main.png



# Summary
You can use the adapter design pattern when an object wants to reuse a class with an incompatible interface. The pattern can also be used where you want to reuse a previously existing functionality.


Ok, this was a simple example and as you noticed we are not even using interfaces, to create an adapter is kind of the situation of the guy going from his house to his neighbors. The goal was to understand the pattern so if you have such a simple situation maybe a pattern will add unnecessary complexity.

Now let’s think in an example in your current project..
Can you identify some class inside your code expecting an specific type of object and you actually have that object but with a different interface?
let’s now to think in our adapter, if we are able to create one we’ll allow the classes work together.

This is a very common pattern and maybe you already implemented it wit out know it was a pattern, didn't you?

Warning: you should implement this pattern only if your classes/objects are similar, if you are creating a very big and complex adapter maybe that’s not the best solution.




