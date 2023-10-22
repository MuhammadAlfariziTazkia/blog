---
description: Object? what is it?
---

# Object

Object is the instance of the class

In the class, we already define a blueprint to create an object right? So object is the instance of that

For the example we already have `Vehicle.java` that contain a code of Vehicle class

{% code title="Vehicle.java" %}
```
public class Vehicle {
    public String color;
    public String material;
    public int topSpeed;
    public int fuelCapacity;
    
    public void moving () {
        System.out.println("The vehicle is moving right now");
    }
    
    pubilc void braking () {
        System.out.println("Vehicle is braking...");
    }
}
```
{% endcode %}

This is the basic syntax to create an object :&#x20;

```
<class_name> <var/object_name> = new <class_name>
```

For the example we want to create an object in `Main.java` file

{% code title="Main.java" %}
```
public class Main {
    public static void main (String[] args) {
        Vehicle myVehicle =  new Vehicle();
        
        myVehicle.moving(); // will print The vehicle is moving right now
        
        myVehicle.material = "Adamantium";
        System.out.println(myVehicle.material); // will print Adamantium
    }
}
```
{% endcode %}
