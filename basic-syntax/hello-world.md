---
description: Simple "Hello World" in Java
---

# Hello World

I think "Hello World" program is the most common way to try new programming language, so let's check this out.&#x20;

This is minimal code to output "Hello World" to the console in Java :

```
public class Main {
    public static void main (String[] args) {
        System.out.println("Hello World");
    }
}
```

These are simple explanation for code that attached above :&#x20;

* `public class Main` -> Java is one of Object Oriented Programming language, so in Java every code should be wrapped into a `class`. Class name must be same with file name, in this case we using `Main` as class and file name. `public` means this class can be access by another file or resources in this project scope (we will explain deeper for `public` later).
* `public static void main (String[] args)` -> for general explanation, I can say this is a function that will be executed first by the default when we running a Java Class, or we can simply defined as `main method` of the program. Maybe some of you will ask about `static` keyword, but I think we can ignore it for now because I will explain it deeper on `Object Oriented Programming` section.
* `System.out.println("Hello World")` -> `System.out.println` is A function in Java that we can use to display a line of text based on argument that passed into this function. In this case `"Hello World"` is the argument that passed into this function, so program will display `"Hello World"` to the console.
