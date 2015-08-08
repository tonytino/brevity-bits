# Ruby Topics Brought Up By Will @ Marqeta

## Constructor

### Literal Constructors

The standard way to create an instance of a built-in Ruby class is by using the #new constuctor. However, many of Ruby's built-in classes include literal constructors as well, which allow you to use syntax to create object instance. For example, you can create an Array instance by using '[]', which can also be prepopulated ('[1,2,3]').

As implied earlier, not all of Ruby's built-in classes include this option, such as the Integer class.

Below are some additional examples of literal constructors:

- **Array:** [1,2,3]

- **Hash:** {'One' => 1, 'Two' => 2, 'Three' => 3}

- **Range:** 1..3 or 1...3

- **Proc (lambda):** ->(a,b) {a * b}

[Check out the Ruby Docs page for creating Arrays](http://ruby-doc.org/core-2.2.0/Array.html)

### The 'Constructor' Method

Ruby uses the initialize method as the constructor method for any class. This method usually accepts parameters that are typically used for setting important variables (particularly instance variables).

The method is invoked by calling #new on a class (e.g. Array.new).

[Read more about it here.](http://www.tutorialspoint.com/ruby/ruby_object_oriented.htm)

## Classical Inheritance

Inheritance in Ruby involves two classes, the superclass and the subclass, the latter being that which inherits behaviors (read: methods) from the former. This means that all instances of the subclass will have access to the methods defined within the superclass.

This can be accomplished when defining the Class by following its name with a less than symbol ('<'), followed by the name of the Class you wish for it to inherit from (e.g. 'class AppleTree < Tree').

### Single Inheritance (The 'Problem' of Inheritance )

**Ruby does not support mulitple inheritance.** However, it does provide modules, which allow you to accomplish something very similar (more on this below).

Although you can chain inheritance (e.g. class BabyAppleTree < AppleTree - AppleTree inherits from Tree, so BabyAppleTree also inherits from Tree), *you cannot have a subclass inherit from two superclasses* (e.g. class BabyAppleTree < AppleTree < Tree - This *would not* work). In the example just provided, Tree would be the super-superclass of BabyAppleTree.

It's worth noting that BabyAppleTree could technically not have any methods of its own if it acquired everything it needed from its superclass and super-superclass, i.e its *ancestors*.

## Include vs Extend

### Modules

In Ruby, you have access to built-in Modules such as Comparable or Enumerable, which you can use to inherit (i.e. '*mixin*') behavior into classes you define. In addition, you can also write your own modules, the structure for which is very similar to writing a class, except the word 'class' is replaced with 'module' (e.g. 'module ModuleName'), and you no longer need to write an initialize method.

The key differences are:

- Unlike with inheritance, you can have a class utilize numerous modules

- You *cannot* create instances of modules

### Include (and Prepend)

If you have a class that you would like to add behaviors to that you have already built, you can separate those behaviors (read: methods) into a module, which you can then 'include' or 'prepend' into your class ('include' and 'prepend' will accomplish the same objective). Your class instances will then have access to the methods defined in the module, meaning you could call such methods on your class instances.

When you want to include a module inside of a class, you simple write 'include ModuleName' on a separate line after defining the name of the class (e.g. class MyClass).

Prepending a module can be accomplished using the same approach (e.g. 'prepend ModuleName'), but prepend comes with an added benefit: if you call a method that is defined in both the module and the class, Ruby will check the module *first* rather than the class.

If you ever want to find out the order in which Ruby will look for a method, you can do so by calling ::ancestors on the class itself, which returns an array that indicates the order by which Ruby will search.

**Note:** In order to be able to include a module within a class, you must require it within the file where you define such class.

**Note:** Although by no means mandatory, it is good practice to use nouns for class names (e.g. Ball) and adjectives for module names (e.g. Bouncy).

### Extend

While you would use include (or prepend) to add behavior (read: methods) to instances of a given class, extend is used to add behavior to the class itself. In other words, use include (or prepend) if you want a set of instance methods to be added to all instances of a class, or extend if you want to add class methods to a class.

A classic example of what this could be used for is accessing all instances of such class, assuming your module gives you a method that accomplishes such.

Just like before, to 'extend' a class, you would use the same methodology as you do for 'include' and 'prepend', replacing either with the word 'extend'.

## Nil vs False

*Coming soon*

## 4 Ways to Invoke a Method in Ruby

The following options are in order of efficiency. The last three allow you to dynamically invoke a method.

1. Call the method directly on your object

    Example: `str.length`

    Example: `str.split`

2. Use #send to invoke a method using a string or symbol representing the method name

    Example: `str.send('size')`

    Example: `str.send(:split, '')`

3. Create a method object and call it

    Assume: `str = "hey hi"`

    Assume: `method_obj = str.method(:split)`

    Example: `method_obj.call # => ['hey', 'hi']`

    Example: `method_obj.call('') # => ['h','e','y',' ','h','i']`

4. Use 'eval' to invoke a method using a string representing the instance name followed by the method name being called

    Example: `eval 'str.count'`

    Example: `eval 'str.split('')'`

## Encapsulation

Encapsulation is accomplished by several means in Ruby, including using modules to collect and isolate behaviors (read: methods) and using objects to collect and isolate actions and data.

In general, you can use encapsulation for any purpose you see fit by enclosing whatever you are encapsulating in something such as a variable, a method, an object, a module, a class, etc.

## Proc

