---
description: Manage the access right of our resource
---

# Encapsulation

Encapsulation is the one of four main pillars in Object Oriented Programming

This is crucial concept that allow programmer to manage and organize the access right of the attribute, method, or even the class.

## Access Modifier

These are access modifier that can be used to organize access right of the asset (can be attribute or method) in the class

<table><thead><tr><th width="218"></th><th width="120">Class</th><th width="124">Package</th><th width="128">Subclass</th><th width="330">World</th></tr></thead><tbody><tr><td>no-modifier / default</td><td>Yes</td><td>Yes</td><td>-</td><td>-</td></tr><tr><td>public</td><td>Yes</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>protected</td><td>Yes</td><td>Yes</td><td>Yes</td><td>-</td></tr><tr><td>private</td><td>Yes</td><td>-</td><td>-</td><td>-</td></tr></tbody></table>

## Main Idea

* Restricting direct access to class attribute -> so better to use `private` attribute
* Enforce manipulation of class attribute only can happened in that class only
* E.g:&#x20;
  * Class A cannot access attribute on Class B directly
  * If Class A have to use or modify attribute on Class B, it should be through by public method on Class B -> it's commonly by Setter and Getter method

## Bad Code Example

```
class Monster {
    public String name;
    public int hp;
    public int damage;
    public int speed;
}

class Main {
    public static void main (String [] args) {
        Monster m = new Monster();
        m.name = "hydra";
        m.hp = 1000;
        System.out.println(m.name); // will output "hydra"
    }
}
```

I can say this is the example of bad code because you can see in class `Main`, the attribute of class `Monster` directly.

Please refer the good code below instead

## Good Code Example

```
class Monster {
    private String name;
    private int hp;
    private int damage;
    private int speed;
    
    public void setName (String name) {
        this.name = name;
    }
    
    public void setHp (String hp) {
        this.hp = hp;
    }
    
    public String getName () {
        return this.name;
    }
}

class Main {
    public static void main (String [] args) {
        Monster m = new Monster();
        m.setName("hydra");
        m.setHp(1000);
        System.out.println(m.getName); // will display "hydra"
    }
}

```

You can see that all of attribute in `Monster` class are `private`, and there is some public function in `Monster` class

* `setName()` to change / set the name of the monster
* `setHp()` to change / set the hp of the monster
* `getName()` to get the name of the monster

`set...()` and `get...()` are common functions when you using Object Oriented Programming

## Advantage

This is the advantage to implement encapsulation based on my opinion :&#x20;

* We can restrict which attribute can be modified -> you can see that I only create setter method for `name` and `hp`. In the some case, perhaps I don't want other attribute like `damage` and `speed` can be set directly, instead I want some default calculation to decide the value of `damage` and `speed`. For the example:&#x20;
  * I want the value of `damage` is based on character length of the `name`&#x20;
  * I want the value of `speed` is based on `damage` / `hp`
  * So we can go with this code

<pre><code><strong>// FIRST WAY
</strong>class Monster {
    private String name;
    private int hp;
    private int damage;
    private int speed;
    
    public void setName (String name) {
        this.name = name;
        this.damage = name.length();
    }
    
    public void setHp (String hp) {
        this.hp = hp;
        
        if (damage != null) {
            this.speed = damage / hp;
        }
    }
}

// SECOND WAY
class Monster {
    private String name;
    private int hp;
    private int damage;
    private int speed;
    
    public void setName (String name) {
        this.name = name;
        setDamage(); // change damage every name is updated
    }
    
    private void setDamage () {
        this.damage = this.name.length();
    }
    
    public void setHp (String hp) {
        this.hp = hp;
        setSpeed(); // change speed every hp is updated
    }
    
    private void setSpeed (String hp) {
        if (this.damage != null) {
            this.speed = this.damage / this.hp;
        }
    }
}
</code></pre>

* We can create precondition before we set the value. For the example I only want the `name` of the monster only can change 3 times. Please let's check the code below for the example when implement or not implement the encapsulation. (**Note -> check conclusion at the end of each implementation)**

<pre><code><strong>// WITHOUT ENCAPSULATION
</strong><strong>class Monster {
</strong>    public String name;
    public int hp;
    public int damage;
    public int speed;
}

class Gameplay {
    public static void main (string [] args) {
        Monster m = new Monster();
        int nameChangeCounter = 0;
        
        // several lines of code
    
        if (nameChangeCounter &#x3C; 3) { // we should check is monster already have name
            m.name = "hydra"; 
            nameChangeCounter += 1;
        }
        
        // several rows of code
        
        if (nameChangeCounter &#x3C; 3) { // we should check is monster already have name
            m.name = "updated hydra"; 
            nameChangeCounter += 1;
        }
        
        // WE NEED CHECK NAMECHANGECOUNTER EVERY WE SHOULD SET THE NAME OF MONSTER
        // IMAGINE THERE IS MORE THAN ONE CLASS THAT CREATE MONSTER OBJECT 
            //-> THE CODE WILL REPEATED AGAIN AND AGAIN
        // AND IMAGINE IF THE PRECONDITION NEED TO CHANGE 
            // -> WE SHOULD CHANGE SO MANY LINE OF CODE
            // -> SOME OF PRECONDITION HAVE A POTENTIAL TO BE SKIPPED BECAUSE WE ARE ONLY HUMAN
}

// ------------------------------------------


// WITH ENCAPSULATION
class Monster {
    private String name;
    private int hp;
    private int damage;
    private int speed;
    private int nameChangeCounter = 0;
    
    public void setName (String name) {
        this.isCanChangeName () {
            this.name = name;
            this.nameChangeCounter += 1;
        }
    }
    
    // if precondition need to be change, we can only adjust this function
    public boolean isCanChangeName () {
        return this.nameChangeCounter &#x3C; 3;
    }
}

class Gameplay {
    public static void main (string [] args) {
        Monster m = new Monster();
        m.setName("hydra");
        
        // several lines of code
        
        m.setName("updated hydra");
        
        // ANOTHER CLASS NO NEED TO KNOW LOGIC OR PRECONDITION WHEN WE SET THE NAME
        // BECAUSE LOGIC AND PRECONDITION IS HANDLED IN MONSTER CLASS
}
</code></pre>

