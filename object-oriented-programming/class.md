---
description: Understanding class concept in OOP
---

# Class

Class is fundamental concept in object oriented programming.&#x20;

Class have a role as a blueprint of the object that we want to create and use

As we mention in previous article, a class have :&#x20;

* **Attribute** -> represent the data that attached with object which will be created
* **Method** -> represent the behavior / activity that object can perform

## Create a Class

To create  a class, basically these are step that we need to do :&#x20;

Firstly create a file along with class name. E.g -> we want to create `Vehicle` class, so filename should be `Vehicle.java` (should match with classname)

After file is created, this is basic syntax to create a class

```
<access_modifier> class <class_name> {
}
```

* `access_modifier` -> used to define access right of the class, it can be `public`, `private`, `protected`. We will discuss further about this in articles of **Encapsulation**. For now, we use `public` instead
* `class_name` -> the name of the class, match with filename

Example

```
public class Vehicle {
}
```

## Attribute

The data that will be attached with the object which will be created

Actually, how to create attribute in the class is similar with how to create variable, and this is basic syntax to create an attribute of the class :&#x20;

```
<access_modifier> <datatype> <varname/attributename>
```

For the example, we can put the `attribute` in the `class` like this :&#x20;

```
public class Vehicle {
    public String color;
    public String material;
    public int topSpeed;
    public int fuelCapacity;
}
```

## Method

behavior / activity that object can perform. For the example we want to add moving and braking behavior of the vehicle :&#x20;

```
public class Vehicle {
    String color;
    String material;
    int topSpeed;
    int fuelCapacity;
    
    public void moving () {
        System.out.println("The vehicle is moving right now");
    }
    
    public void braking () {
        System.out.println("Vehicle is braking...");
    }
}
```
