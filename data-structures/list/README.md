---
description: Let's learn about concepts of dynamic array
---

# List

List is a `interface` class in Java that provide a concepts to store data like an array, but in dynamic way.

From the statement above, maybe some questions will appear : &#x20;

1. What is interface?
2. How can List store 1 or more data with dynamic size?

Okay let's answer that question

1. Interface -> It's simply a class that contain 1 or more functions without its code logic implementation. So how we can put an algorithm in each function? -> by create a class that implement its interface class. If little bit hard to understand, don't worry, we can talk more about interface later in Object Oriented section.
2. List can store 1 or more data with dynamic size in several way, each way represents by implementation class of List. 2 the most common implementation class is `ArrayList`, and `LinkedList`

The common functions that used to manipulated data using List is `add()` to add element, `get()` to get element by index, `set()` to update the element using index, `remove()` to remove element using index.

**Please take a note that we cannot use List directly because List is interface class, so we should use an implement class when create list variable (e.g ArrayList or LinkedList)**

### Add

Add function have a parameter which represent the element to add to the list. Let's check this example.

```
list.add("value");
```

### Get

Get function have a parameter which represent an index of element. Let's check this example

```
list.get(0);
```

### Set

Set function have 2 parameter which is&#x20;

* First parameter -> index of element that need to update
* Second parameter -> updated element

Let's check this example

```
list.set(1, "Updated Value");
```

### Remove

Remove function only have one parameter which is index of element that need to removed. Let's check this example

```
list.remove(3);
```
