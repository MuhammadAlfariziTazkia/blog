---
description: Object? what is it?
---

# Object

Object is the instance of the class

In the class, we already define a blueprint to create an object right? So object is the instance of that

For the example we already have `Monster.java` that contain a code of Monster class

{% code title="Monster.java" %}
```
class Monster {
    String name;
    int hp;
    int damage;
    int speed;
    
    // first way constructor -> set all of 
    Monster (String name, int hp, int damage, int speed) {
        this.name = name;
        this.hp = hp;
        this.damage = damage;
        this.speed = speed;
    }
    
    // second way -> we want to set default value for hp and speed
    Monster (String name, int damage) {
        this.name = name;
        this.damage = damage;
        
        // set for default value
        this.hp = 1000;
        this.speed = 500;
    }

    void attack () {
        System.out.println(this.name + " attack with damage of " + this.damage);
    }
    
    void printHp () {
        System.out.println("HP: " + this.hp);
    }
}
```
{% endcode %}

This is the basic syntax to create an object :&#x20;

```
<class_name> <var/object_name> = new <class_name><constructor>;
```

For the example we want to create an object in `Main.java` file

{% code title="Main.java" %}
```
public class Main {
    public static void main (String[] args) {
    
        Monster hydra = new Monster("hydra", 2000, 200, 15);
        // this will call for first way constructor
        
        Monster monster = new Monster("basic", 150);
        // this will call for second way constructor -> only set the name and damage
        
        hydra.attack(); // will print "hydra attack with damage of 200
        hydra.printHp(); // will print "HP: 2000"
        
        monster.attack(); // will print "monster attack with damage of 150
        monster.printHp(); // will print "HP: 1000"
        
        // we can override the hp of "monster"
        monster.hp = 1250;
        monster.printHp(); // will print "HP: 1250"
    }
}
```
{% endcode %}



**By the way, when you not create any constructor in the class, by default class will have 1 constructor empty parameter, so you can use it by**

```
MyClass c = new MyClass(); // call empty constructor
```
