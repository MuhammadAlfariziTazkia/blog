---
description: Static? what is it?
---

# Static

`static` -> is a keyword in Java programming language that can be applied in variable and function.

{% hint style="info" %}
IMO, I will say that the variables and functions which marked with `static` keyword is owned by `class` level, not only `object`, so -> every variables and functions with this keyword will affect to every objects that instance of that class.
{% endhint %}

## Variable or Function without Static Keyword

Variable and function that we discuss in previous articles has a dynamic behavior, it means -> the value the variable has, or what a function does is depend based constructed object.

Let's say we have this code snippet

```
class Person {
    String name;
    int age;
    String gender;
    
    Person (String name, int age, String gender) {
        this.name = name;
        this.age = age;
        this.gender = gender;
    }
    
    String getName () {
        return this.name;
    }
}

public class Main {
    public static void main (String [] args) {
        Person andi = new Person ("Andi", 23, "Male");
        Person nita = new Person ("Nita", 15, "Female");
    }
}
```

This is an explaination of the code above :&#x20;

* When we construct the object of `andi` with `new Person ("Andi", 23, "Male")`&#x20;
  * Variable `name` will assigned with `Andi`, `age` will assigned with `23`, and `gender` will assigned with `Male`
  * Function `getName()` will return `Andi`
* But when we construct the object of `nita` with `new Person ("Nita", 15, "Female")`
  * Variable `name` will assigned with `Nita`, `age` will assigned with `15`, and `gender` will assigned with `Female`
  * Function `getName()` will return `Nita`

{% hint style="info" %}
Variables and function behavior between object `andi` and `nita` is **different**, so I say it as **dynamic**
{% endhint %}

## Static Variable or Function

Imagine that we want to restricts the creation of `Person` objects to a maximum of `3`, so we can do this with our code

```
class Person {
    String name;
    int age;
    String gender;
    
    static int createdObjects = 0;
    
    Person (String name, int age, String gender) {
        if (isCanCreateObject ()) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            
            createdObjects ++;
        } else {
            System.out.println("Maximum created objects is only 3");
        }
    }
    
    String getName () {
        return this.name;
    }
    
    static getCreatedObjects () {
        return createdObjects;
    }
    
    static boolean isCanCreateObject () {
        // return true if created object still less than 3
        return createdObjects < 3;
    }
}

public class Main {
    public static void main (String [] args) {
        Person andi = new Person ("Andi", 23, "Male");
        Person nita = new Person ("Nita", 15, "Female");
        System.out.println(Person.getCreatedObjects());
    }
}
```

Explaination :&#x20;

* `createdObjects`&#x20;
  * Used to count the created objects of the `Person` class
  * Will incremented after successfully constructed new object
* `getCreatedObjects()`&#x20;
  * Is a function to get information about total created objects
  * Static function can be used in another class with this syntax -> `Classname.staticFunctionName()`
  * So the way to use `getCreatedObjects()` -> `Person.getCreatedObjects()`
* `isCanCreateObject()`
  * Function to check is we can still create object?
  * Called in constructor of `Person`

{% hint style="warning" %}
**Variables** and **functions** which marked by `static` keyword only can used in `static` function, or **constructor** of that class
{% endhint %}

## Usages

From the example above, I hope we can understand the one of usages of `static` keyword.

The other usages sample -> in design pattern theory, we have a `singleton` concept -> we only create object only once. Similar with the example right? but the simple different is from the example, maximum `createdObjects` is `3`, but `singleton` concept only allow `1`
