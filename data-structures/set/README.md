---
description: Set Data Structure in Java
---

# Set

I can say that `Set` data structure is similar with `List` -> is used to store more than one value which have same data type.

The main different between `Set` and `List` -> `List` can contain duplicate value, but `Set` cannot contain duplicate value.

The other similarities between `Set` and `List` is both of them is `interface` class, so to manipulate data with the `Set`, we need using implementation class of `Set`. I thought that `HashSet` is most common implementation class while using `Set`.&#x20;

It's interesting to explore how logic that implemented in `HashSet`, but we will talk about that later. For now, we focus to discuss about the simple way to operate the `Set`.

## Create

This is basic simple example to create `Set` using implementation of `HashSet`, and this variable will contain value with `String` data types.

```
Set<String> nameSet = new HashSet<>();
```

## Add Element

We need to call function `add()` to do this. `add()` function have single parameter which is the value that we want to add.

```
nameSet.add("John Doe");
nameSet.add("Jane Doe");
```

## Is Element Exist?

We need to call function `contains()` along with the parameter of value that we want to know the existence.

```
System.out.println(nameSet.contains("John Doe"); // will display true
System.out.println(nameSet.contains("Bejo"); // will display false
```

## Remove Element

It's simply to use `remove()` function along with element that we need to removed.

```
nameSet.remove("John Doe");
```

## Count Elements

We can use `size()` function to know how many elements that our set have.

```
nameSet.size();
```

## Iterate the Set

Maybe so far you notice that there is no way to access set using an index. To get `Set` element, we need to use iterate them. For the example we can use these 2 way to iterate the `Set`

### Using For-each

```
for (String name : nameSet) {
    System.out.println(name);
}
```

### Using Iterator

Firstly I think we better create variable with `Iterator` type

```
Iterator<String> iterator = nameSet.iterator();
```

We type `<String>` is because the element in the `Set` have `String` data type

Iterate using `while` loop, with condition of `iterator.hasNext()` -> it means this loop still working while our `Set` still have element which has not been iterated&#x20;

To display the accessed value, we can use `next()` function

```
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}
```
