---
description: One of important concepts in programming languages
---

# Variable and Data Types

### Variable

For simple explanation, we can imagine variable is the container that contain the data. Data in variables can be accessed while the program is executing.

In Java, we can split variable into **local variable, instance variable,** and **static variable.** But for this section I think better to understand about **local variable** first, because we will discuss further about **instance** and **static** variable after know and understand about Object Oriented Programming concepts.

#### **Local Variable**

Local variable declared in a **function** or **method** (we will discuss further about function and method in next few section).&#x20;

Example of variable&#x20;

```
public class VariableExample {
    public static void main (String[] args) {
        String myName = "John Doe";
        System.out.println(myName);
    }
}
```

These are simple explanations about code snippets above :&#x20;

* We already discussed about `main` in `public static void main(String[] args)` is a function name.
* `String myName = "John Doe";` is example of variable declaration. This variable name is `myName` and the data that contained in this variable is `John Doe` which have `String` data type.
* `System.out.println(myName)` will display the value of `myName` which is `John Doe`. So here is output of code snippets above :&#x20;

```
John Doe
```

#### Instance Variable

We will learn more about instance variable and usages in Object Oriented Programming sections, but in this section we can simply say that instance variable is the variable which declared in the class but outside of the function or method. This is an example for a variable declaration named as "text" variable :&#x20;

```
public class Example {
    String text;
    
    public static void main (String[] args) {
        // Main code here
    }
}
```

#### Static Variable

As instance variable, I think better explain deeper about a static variable at Object Oriented Programming sections, but in this section we can simply say that static variable is Instance variable with `static` keyword :smile:

```
public class Example {
    static String myText = "Hello World";
}
```

### Data Types

In Java, we can say that there is 2 kind of data types, which is **Primitive** and **Reference Data Types**.

The main different between these 2 data types is about how to store the data into physical memory block.

#### Primitive Data Type

Store the data into 1 memory block directly.

There is 8 primitive data types in Java :&#x20;

* `byte` -> 8-bit (binary digit) that represents integers (range start from `-128` into `127`)
  * Example `byte num = 42` -> we can say there is a block of memory that contain 8-bit that represents 42 -> `00101010`
* `short` -> 16-bit that represents integers (range start from `-32,768` into `32,767`)
* `int` -> 32-bit that represents integers (range start from `-(2)^31` into (`2^31)-1`)
* `long` -> 64-bit that represents integers (range start from `-(2)^63` into (`2^63)-1`)
* `float` -> 32-bit that represents floating numbers (range start from `-(2)^31` into (`2^31)-1`). Example -> `13.253`
* `double` -> 64-bit that represents floating numbers (range start from `-(2)^63` into (`2^63)-1`)
* `char` -> 16-bit unicode character. Example -> `'c'`
* `boolean` -> only can contain 2 kind of values -> `true` or `false`&#x20;

```
int number = 10;
char myCharacter = 'A';
float floatingNumber = 1.21;
```

#### References Data Type

Store references or address from the **object**.&#x20;

Example of reference data type in Java is `String`, `Array`, `Map`, etc.

For the example, we have `String` value of "John", these are simple explanation / ilustration about how "John" will store in memory.

* `J` will encoded into `byte` -> 0x4A (`01001010`) for the example this `byte` will stored in memory with labeled as `Memory A`
* `o` will encoded into `byte` -> 0x6F which will be stored in memory with labeled as `Memory B`
* `h` will encoded into `byte` -> 0x68 which will be stored in memory with labeled as `Memory C`&#x20;
* `n` will encoded into `byte` -> 0x6E which will be stored in memory with labeled as `Memory D`
* For the example, we can say that variable `name` will store in `Memory ABC` which contain memory address of the first character of "John" -> `Memory A`

```
String myName = "John Doe"
```
