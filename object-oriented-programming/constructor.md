---
description: Constructor in Object Oriented Programming
---

# Constructor

Constructor is a special function in a class that can be used to initiate / create object, we talk about creating object later, in this section we only prepare a method to construct the object

## Construct and set all of parameter

Imagine that is a class of `Monster` which have attribute of `name`, `HP`, `damage`, and `speed`, then we want to create the "Hydra" as an object of the `Monster`

Of course "Hydra" need creation statistic like `HP` to represent maximum of health point, `damage`, and `speed` that "Hydra" have

So in `Monster` class, we should create a special method which allow us to construct a monster along with their statistic -> this special method called **Constructor**

```
class Monster {
    string name;
    int hp;
    int damage;
    int speed;
    
    // constructor
    Monster (string name, int hp, int damage, int speed) {
        this.name = name;
        this.hp = hp;
        this.damage = damage;
        this.speed = speed;
    }
}
```

* Constructor method that we talk about -> `Monster (string name, ...`&#x20;
* Maybe you noticed that `this.name = name`. What does it means?
  * `this.name` and `name` is refer to different sources
  * `this.name` -> refer to `name` attribute of `this` class -> `Monster` class
  * `name` -> refer of the passed argument when this constructor is called

Code snippets above is the common way to create constructor. But, if you still confuse about `this.name` or `name`, we can change the example&#x20;

```
class Monster {
    string name;
    int hp;
    int damage;
    int speed;
    
    // constructor
    Monster (string paramName, int paramHp, int paramDamage, int paramSpeed) {
        this.name = paramName;
        this.hp = paramHp;
        this.damage = paramDamage;
        this.speed = paramSpeed;
    }
}
```

Is the code above more make sense to you? but don't forget the **most common way to create constructor is the first code example**

## Each class can have more than one constructor

how can? -> imagine that we want to have 2 way to construct the monster

* First way -> set all of attribute
* Second way -> I already have default value for `hp` as 1000, and `speed` as 500 if we not set it explicitly

Yap we can create 2 constructor to provide 2 these ways

```
class Monster {
    string name;
    int hp;
    int damage;
    int speed;
    
    // first way constructor -> set all of 
    Monster (string name, int hp, int damage, int speed) {
        this.name = name;
        this.hp = hp;
        this.damage = damage;
        this.speed = speed;
    }
    
    // second way -> we want to set default value for hp and speed
    Monster (string name, string damage) {
        this.name = name;
        this.damage = damage;
        
        // set for default value
        this.hp = 1000;
        this.speed = 500;
    }
}
```
