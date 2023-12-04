---
description: Abstraction Concept in Object Oriented Programming
---

# Abstraction

The main usage of abstraction is to simplify code complexity by hiding the unnecessary detail logic implementation.

To understand about abstraction concept, I will use the example of **vehicle**.

We can say that the **vehicle** is an abstraction of  the **car**, **bicycle**, **motorcycle**, **plane**, or even **ship.**

Basically, all of vehicle can move. But the way to move a **bicycle** is totally different with how to move a **plane.**

Every vehicle have their own way to moving, and some of them have a complex logic to move.&#x20;

To make development easier, we can generalized the car, motorcycle, plane, and ship as **vehicle** -> so it means :&#x20;

* Vehicle is abstraction class
* Car, motorcycle, bicycle, and plane become the concrete class





Abstraction concept help us to simplify code detail complexity, so it can be increase readability of our code.

Abstraction objective are :&#x20;

* Hide the detail of internal functionality
* Only expose the relevant functionality or feature

## Why is it Important?

* Hide unnecessary complexity -> It's allow the object user using the function of the object without know about how this object is implemented
* Easy to maintain -> by using abstraction, changes of logic implementation can be done without affected of usage of the object
* Increase readability

## How to Implement Abstraction Concept?

To implement abstraction concept into our code, we can using `abstract` or `interface` class

### Abstract Class

* Is used to create partial abstraction
* In abstract class, it's possible to create :&#x20;
  * Abstract method -> method without code logic implementation
  * Concrete method -> method with code logic implementation

```
abstract class 
```
