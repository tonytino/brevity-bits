---
layout: post
title:  "Object Oriented Ideas"
date:   2015-05-05
categories: DBC Notes
---

<!-- https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet -->
<!-- https://gist.github.com/stujo/78798dab0e4d5426847b -->

Object-Oriented ("OO") Design is not about modeling the real-world completely in entirety (e.g. we don't need a sub class for every cookie type).
It's about creating abstractions necessary to get a job done.


*When creating a MVP program, make sure you're only building what's necessary **__based on the user stories__**. The program should support the ability to have infinite customizability rather than having all things already accounted for (e.g. making every type of cookie rather than just the template for such).*

Code is a liability, not an asset. The more complex you make it, the more problematic it will become. *When creating an abstraction of a real-world object, only model what is absolutely necessary.* Imagine building a really detailed program as a solution to a client's request, only to find out that they miscommunicated their needs, meaning you have to wipe half of your program or more.

### Important OO Terms
* Abstraction - Figuring out what abstractions express our requirements
* Polymorphism - Using multiple abstractions in the same way
* Inheritance - Sharing Implementation
* Encapsulation - Hiding Implementation Details

One of your number one jobs is *reducing complexity*. The Law of Demeter: principle of least knowledge; a guideline of software dev. Only talk to your immediate friends.

**Encapsulation**: is the packing of data and functions into a single component. The features of encapsulation are supported using classes in most object-oriented programming languages, although other alternatives also exist.

An abstract class is an incomplete class. If you have a cookie class and subclasses that represent the different cookie flavors, you cannot create a cookie instance because it doesn't know what kind of cookie it is; it's built for the purpose of inheritance only (i.e. a template).

Law of Demeter: Don't reach into another object through an object to invoke a method. In other words, don't chain like: oven.cookies.bake!