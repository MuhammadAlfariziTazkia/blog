---
description: Abstraction Concept in Object Oriented Programming
---

# Abstraction

The point of abstraction is **simplify the code by hiding unnecessary detail logic implementation**

{% hint style="info" %}
3 Terms that we will frequently used in this discussion :

* **Abstract** -> only provide the definition
* **Concrete** -> provide the definition including the detail logic implementation
* **Override / Overriding** -> it can be implement **abstract** method or re-implement **concrete** method from **abstraction class**
{% endhint %}

## Implement the Abstraction

To implement the abstraction concept in java, we can using `abstract` and `interface` class

### Abstract Class

* Provide **partial abstraction** -> can have **abstract** method and **concrete** method
* To create **abstract** class, we can use this syntax -> `abstract class <ClassName>`
* To define **abstract** **method** in **abstract class** we need to provide `abstract` keyword explicitly in method definition

Example :&#x20;

```
abstract class PropertyCleaningService {
    
    // abstract method
    void request () {
        System.out.println("You can request our service by call +62123123123 ...");
    }
    
    int getCleaningServiceFee (int durationInHour) {
        return durationInHour * 10;
    }
    
    // concrete method
    abstract void clean ();
}
```

* To implement the **abstract** **method** in **abstract class**, we need implementation class that extend to the **abstract class**&#x20;
* The implementation class is must implement all of **abstract method** from **abstract class**
* When we want to implement or re-implement the logic in implementation class, it's recommended to use @Override annotation.

Example :&#x20;

```
class ApartmentCleaningService extends PropertyCleaningService {

    // request method already have implementation in abstract class
    // and we don't want to change default logic of request method
    // so we don't need to implement the logic of request method in this class
    
    // getCleaningServiceFee already have implementation in abstract class
    // but, I want to create different calculation for apartment property
    // so just re-implement the logic in this class
    
    @Override
    public int getCleaningServiceFee (int durationInHour) {
        return durationInHour * 50;
    }
    
    @Override
    public void clean () {
        System.out.println("To clean apartment, we should ask receptionist about location of our customer"); 
    }
}
```

### Interface Class

* Provide **full abstraction** -> only have **abstract** method
* We can create `interface` class by use this syntax -> `interface <ClassName>`
* Don't use `abstract` keyword specifically in method definition, just use this syntax instead -> `<returnDataType> <methodName> (<parameter>);`, e.g -> `void request ();`

Example :&#x20;

```
interface PropertyCleaningService {
    void request ();
    void clean ();
    int getCleaningServiceFee (int durationInHour);
}   
```

* Same as `abstract` class, we need to create implementation class to implement the logic of all of `abstract` method in `interface` class
* We can create implementation class by use this syntax -> `class <ClassName> implements <InterfaceClass>`
* Implementation class must implement all of methods in `interface` class
* It's recommended to use `@Override` annotation in implementation method

Example :&#x20;

```
class HouseCleaningService {

    @Override
    public void request () {
        System.out.println("Requesting cleaning service for house type");
    }
    
    @Override
    public void clean () {
        System.out.println("Cleaning cleaning");
    }
    
    @Override
    public int getCleaningServiceFee (int durationInHour) {
        return durationInHour * 15;
    }
}    
```

## Why is it Important?

* **Hide unnecessary code complexity**
  * It makes easier for developer to check "what does this function can do?" because developer just need to check `abstract` / `interface` to check this. If we don't use abstraction concept, developer need to deep dive into a class that contain full of implementation logic&#x20;
* **Easy to maintain**&#x20;
  * When we want to create feature / logic, modify existing code can be risky because we change something that is already stable. So, instead of modifying existing code, we just need to create another implementation class to implement new feature logic
* **Increase readability**
  * Because we splitting class for definition and class for implementation
* **Support polymorphism**
