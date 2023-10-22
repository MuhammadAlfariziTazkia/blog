---
description: One of reference data types, let's deep dive!
---

# String

Basically, String is data type that used to represent text in programming languages. This text can be alphabetical, numerical, alphabetical, and another characters that we can see, how cool is that!

### Declaration and Initialization

It's simply like this

```
// only declaration
String variableName; // String variable contained 'null' as default value
System.out.println(variableName); // will print 'null'

variableName = "Test variable name";
System.out.println(variableName); // will print 'Test variable name'

// declaration and initialization
String myName = "John Doe";

// empty string
String emptyStr = "";
```

### Length

To get the num of characters in String, we can use `length()` method. Let's check this example

```
String name = "John";
System.out.println(name.length()); // will print 4
```

### Get Character By Index

Please take a note that index start from 0, and to get specific character by index, we can using function `charAt(index)` . So let's check this example

```
String word = "Hello";
System.out.println(word.charAt(0)); // will print 'H'
System.out.println(word.charAt(1)); // will print 'E'
```

### Change to UPPERCASE and lowercase

We can simply use `toLowerCase()` to change String into lower case, and use `toUpperCase()` to change String into upper case

```
String name = "John";
System.out.println(name.toUpperCase()); // will print 'JOHN'
System.out.println(name.toLowerCase()); // will print 'john'
```

### Get a Substring

We can use `substring()` method to do this, and let's check basic code format to use `substring()`

```
stringVariable.substring(startIndex, endIndex);
```

if we set `startIndex` -> 0, and `endIndex` -> 4, the substring will return character of index 0, 1, 2, and 3.

Let's check this example

```
String word = "012345";
System.out.println(word.substring(0, 3); // will print '012'
```

### Comparation

To compare 2 String values, better to use `equals()` method instead of using `==` . Look for this simple example

```
String str1 = "Halo";
String str2 = "Helo";
System.out.println(str1.equals(str2)); // will return false
System.out.println("Halo".equals(str1)); // will return true
System.out.println("ABC".equals("abc".toUpperCase())); // will return true
System.out.println("ABC".equals("abc")); // will return false
```
