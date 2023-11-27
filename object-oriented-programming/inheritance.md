---
description: Talk about inheritance in Object Oriented Concept
---

# Inheritance

Inheritance in simple definition is a concept that able a class to inherit assets (it can be attribute or method) from another class.

**This is the one of important concepts in Object Oriented Programming !**

This concept will help us to develop and manage hierarchy between each class and another class, and able us to reuse the code in another class.

## Basic Concepts

Basically, inheritance able the new class to get the attributes and methods from another existing class

Usually new created class is known as **sub class**, and another existing class which has attributes and methods that we need to "copy" is known as **super class** or **parent class**

For the example, there is a `Animal` class which contain basic attributes and methods of all animals, which is :&#x20;

* Attributes :&#x20;
  * `speciesName`
* Methods :&#x20;
  * `sounding()`
  * `eating()`

For fulfilled that requirements above, we create `Animal.java`

```
public class Animal {
    private String speciesName;
    
    public void sounding () {
        System.out.println("Hello we sounding!");
    }
    
    public void eating () {
        System.out.println("nyam nyam nyam");
    }
}
```

After we create that class, we realized that we need to create a class that can cover the requirement of flying animals

All of flying animals should have `speciesName`, and their can `sounding()` and `eating()` right?

Besides that flying animal need to have another attribute of `maxFlyHeight`, and behaviour to `flying()`

Should we code class `FlyingAnimal.java` like this?

```
// SAMPLE OF BAD CODE
public class FlyingAnimal {
    
    private String speciesName;
    private float maxFlyHeight;
    
    public void sounding () {
        System.out.println("Hello we sounding!");
    }
    
    public void eating () {
        System.out.println("nyam nyam nyam");
    }
    
    public void flying() {
        System.out.println("Wuzzz I believe I can fly");
    }
} 
```

Please be noticed that we create duplicate code to `speciesName`, `sounding()`, and `eating()`. This is not the best practice in Object Oriented Programming concepts.

Instead of doing that, Object Oriented Programming have another way to solve this in the epic way

```
public class FlyingAnimal extends Animal {
    private float maxFlyHeight;
    
    public void flying() {
        System.out.println("Wuzzz I believe I can fly");
    }
}
```

Please look at the line `public class FlyingAnimal extends Animal`, we have a keyword of `extends`. `extends` means, we "copy" all of **protected**, and **public** attributes of **parent class**.

Why **protected** and **public**? Please check articles of [encapsulation.md](encapsulation.md "mention") , attribute or methods with **private** modifier cannot be accessed on sub class -> So we need to change access modifier of `speciesName` in `Animal.java` into **protected**.

IMO, **protected** is the access modifier which is actually used to implement inheritance concept, because it's only can accessed by that class, and it's subclasses

## Constructor

So currently `FlyingAnimal` have attribute of `speciesName` and methods of `sounding()` and `eating()` from parent class `Animal`, so how we can construct their parent's assets ? -> we can use `super()` method to call parent's constructor. So the code need to be changed like this

`Animal.java` :&#x20;

```
public class Animal {
    protected String speciesName;
    
    // access modifer can be protected / public
    // if we have no need to use Animal class directly from another class
    // (just need to called by FlyingAnimal as a subclass) we can use protected instead
    // but if we have need to use this class directly from another class
    // we can change into public
    protected Animal (String speciesName) {
        this.speciesName = speciesName;
    }
    
    public void sounding () {
        System.out.println("Hello we sounding!");
    }
    
    public void eating () {
        System.out.println("nyam nyam nyam");
    }
}
```

```
public class FlyingAnimal extends Animal {
    private float maxFlyHeight;
    
    public FlyingAnimal (String speciesName, float maxFlyHeight) {
        super (speciesName); // will call constructor of Animal class which need to pass speciesName
        this.maxFlyHeight = maxFlyHeight;
    }
    
    public void flying() {
        System.out.println("Wuzzz I believe I can fly");
    }
}
```

## "Is a" - relationship

When we create an instance of `FlyingAnimal` like this :&#x20;

```
Animal bird = new FlyingAnimal("Eagle", "1000");
```

We can read as `FlyingAnimal` **is a** type of an `Animal`

## Advantages of Inheritance

* Increase reusability aspect
* Code structure have a better structure organization
* Easy to maintain
  * If in the future we need to create **SwimmingAnimal**? -> we just need to create another class that extends to `Animal` class :joy:
