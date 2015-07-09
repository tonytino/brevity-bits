---
layout: post
title:  "Class Methods: Not to be Confused with Instance Methods"
date:   2015-04-05
categories: technical
---

### What are class methods?

In case you're not familiar with classes, they are used in Ruby to create objects. These objects typically need to have methods (i.e. functions) associated with them, but more importantly, they serve as a type of template. Say you're creating a class that will represent a bouncy ball (named BouncyBall) in a video game that you're making. You know your game will have various bouncy balls, and they will have many similar characteristics (each will have a size, color, pattern, and/or level of bounciness). However, these balls will not be identical. This is where classes come into play. They allow you to create multiple instances of BouncyBall: each will have the same characteristics, but each one will be slightly different from the next.

Now that we have that covered, let's get into class methods. Class methods are the defined functions of the class itself (in this case, BouncyBall) - this is entirely different from instance methods. Instance methods are the defined functions of the instances of a class. To be clear, both classes and their instances are objects. Now, let's look an some more examples to explain how class methods and instance methods are different.

Let's say there are two instances of your class, BouncyBall: the red BouncyBall (named red, since it's color is red) has a level of bounciness equal to 5, and the blue BouncyBall (named blue...) has a level of bounciness equal to 3. This means nothing without some more context. Let's say each instance of BouncyBall has an instance method called *launch*. Launch will cause the ball to go up 5 feet into the air on its own (just go with it), and when it comes back down, it will bounce x times, where x is represented by the ball's level of bounciness. So, if we call the method *launch* on both instances of our BouncyBall class (red and blue), they will both bounce x times (red will bounce 5 times, blue 3 times).

The moment you've been waiting for (and why I explained everything above): why do we need a class method? Let's say you want to know which instance of your class, BouncyBall, has the highest level of bounciess. We can use a class method called *bounciest* to determine so, which will look at as many instances of your class, BouncyBall, as you request and tell you which has the highest level of bounciness. Defining a method like this on a specific instance of BouncyBall could not tell you this as that instance of BouncyBall does not know the level of bounciness of other BouncyBall instances. However, calling it on the class, BouncyBall, makes this possible, because the instances are the "children" of the class, BouncyBall.

### When and how should you use them?

When you should class methods is slightly touched on at the end of the paragraph above. You want to use class methods when the method that you're performing is something that either affects or is based on all (or specific) instances of such class.

But now you may want to know, how exactly do we write class methods? It's very similar to instance methods in that they are defined within the class itself, but rather than writing something like:

def launch # our instance method example

You would write a class method something like:

def BouncyBall.bounciest(*balls) # our class method example

This means that whenever we want to call on this method, rather than doing it like we would with instance methods...

- red.launch # this would perform the launch function on the red BouncyBall

...we call the method on the class.

- BouncyBall.bounciest(red, blue) # this would tell use which ball, red or blue, has the highest level of bounciness