---
layout: post
title:  "Putting Enumerables on the Map"
date:   2015-03-22
categories: technical
---

### When Provided a Block of Code</h4>

When you take an enumarable (such as a range: e.g. (1..5)) and apply the map method to it, it will take each element and apply an algorithm to it (i.e. the block of code corresponding to the map method), the results of which will be returned within an array.
Example:
(1..5).map {|element| element * 2} => creates an array with each number from 1 through 5 doubled, such as [2,4,6,8,10]

### When NOT Provided a Block of Code</h4>

If you do NOT provide the enumerable a block of code when applying the map method on it, an enumerator is created instead.
Example:
[1,2,3].map => creates the following enumerator: [1,2,3].map

You may be wondering what the difference is... I know I was. Essentially, you just made an object out of "[1,2,3].map", which means you can now apply a method on such object! However, you may want to create a variable for such object to be stored in so that you can easily apply a method on the variable holding the enumerator you just created.
