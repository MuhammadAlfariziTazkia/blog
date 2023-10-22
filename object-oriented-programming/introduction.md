---
description: Object Oriented Programming Paradigm
---

# Introduction

Object Oriented Programming (OOP) -> In my personal opinion, I can say that this is programming paradigm that try to solve the problems by represents that problems into an object

OOP have several terminology that you have to know, and we will discuss further about detail of terminology later in the separate sections.

## Terminology

For a better explanation, I try to use "Vehicle Factory" as a study case

* **Class**&#x20;
  * We can say that class is a blueprint that we need to generate or create an object
  * Class should contain information of&#x20;
    * What are the parameters that need to be considered when we making a vehicle? -> this is known as `attribute` of the class
      * Color
      * Speed
      * Material
      * Fuel capacity
      * Etc
    * What are the behaviors that vehicle can do? -> this is represents as `function` / `method` in the class
      * Moving
      * Braking
      * Filling the fuel
      * Etc
  * **Encapsulation**
    * This concept allows us to organize the access rights of the `attribute` or `method`
  * **Inheritance**
    * A concept that a class can inherit `attribute` or `method` "to" or "from" another class
    * When we have `Vehicle` class for vehicle factory, we can inherit the `attribute` and `method` of that class into child class / child factory like `Motorcycle` class for motorcycle factory, or `Car` class for car factory. Because both of `Motorcycle` and `Car` should have `attribute` and `method` of the `Vehicle`
  * **Polymorphism**
    * Ability of object that can have different implementation of behavior
    * For the example, for the `Moving` method :&#x20;
      * In `Car` -> will produce a sound like "brem brem brem"
      * In `Motorcycle` -> will produce a sound like "ngeng ngeng ngeng"
  * **Abstraction**
    * A concept that allows us to give an abstraction to define what can be done by the object, but we don't need to include the details of each implementations
    * Usually we can use `abstract` or `interface` class to create an abstraction of the object, but we will discuss about both of class later in the separate sections

## Advantages

These are advantages when we use object oriented programming paradigm

* **Modularity** -> when we want to create an software, we can split the components of the software into smaller components for specific responsibility
* **Reusability** -> we can reuse the `attribute` or `method` of the object into a different business process
* **Easier to Understand** -> because we represent the problem as an object, so we can be more relate about the problems
