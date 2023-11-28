---
description: Understanding polymorphism concept in Object Oriented Programming
---

# Polymorphism

* Simple definition -> A concept that allows an object to have more than one morph and behavior
* How an object can have more than one morph? what does it means? -> this can be happened by creating different implementations of a method or function in related classes

## Method Polymorphism

### Overloading

* Different in method definition level, it can be different at :&#x20;
  * Return type
  * Parameters
* **Compile-Time Polymorphism** -> Occur during compiling

Example overloading on method parameters

```
class PersonHelper {
    public void printDetail (String name, String gender, int age) {
        System.out.println("Name : " + name);
        System.out.println("Gender : " + gender);
        System.out.println("Age : " + age);
    }
    
    public void printDetail (String fullName, String nickName) {
        System.out.println("Name : " + fullName + " (" + nickName + ")");
    }
}

class Main {
    public static void main (String [] args) {
        PersonHelper personHelper = new PersonHelper();
        
        personHelper.printDetail("Fajar", "Male", 23);
        // Will print
        // Name : Fajar
        // Gender : Male
        // Age : 23
        
        personHelper.printDetail("Fajar Nugraha", "Fajar");
        // Will print : 
        // Name : Fajar Nugraha (Fajar) 
    }
}
```

Example overloading on method return type

```
class Calculator {
    public int add (int a, int b) {
        return a + b;
    }
    
    public float add (float a, float b) {
        return a + b;
    }
}
```

### Overriding

* Different in method logic implementation
* **Run-Time Polymorphism ->** Occur when application is running
* Use `@Override` annotation

Example

```
class Animal {
    public void moving () {
        System.out.println("I am start moving");
    }
}

class FlyingAnimal extends Animal {
    @Override
    public void moving () {
        super.moving(); 
        // super.moving() will call moving function in parent class
        // this is optional, only if you want to use existing logic in parent function
         
        System.out.println("Woooz, flying flying!");
    }
}
```

## Advantages

* **Flexibility and Modularity**&#x20;
  * We can have more than one class which every class have a same behavior context but different in behavior implementation based on class / module usages (E.g Flying Animal and Swimming Animal have some behavior context -> both of them can moving, but their have different moving way)
* **Code reusability**
  * Function in subclass, can reuse the logic in superclass/parent class function, and adding some specific logic, for the example we can refer on `Animal` and `FlyingAnimal`, which `Animal` class basically have `moving()` function, and `FlyingAnimal` want to have `moving()` function too but with additional logic
* **Easy to extension**
  * When you want to have a new function logic but we already have existing function with the some context, we don't need to change the logic of existing function -> we just need to extends the class and override instead ! **Because changing existing logic which have stable functionality is too risky**
