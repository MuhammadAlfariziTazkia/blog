---
description: The way to save more than 1 values into a variable
---

# Array

Array is a data structure that able you to store 1 or more values with the same data type into 1 variable. With array, we can access the stored data with an indexes.

### Declaration

Array declaration is an action to tell the compiler about existence of a variable with array data type. This is basic code format to declare a variable with array data type.

```
dataType[] variableName;
```

Example:

```
String[] nameArray;
int[] dayIntArray;
```

### Initialization

Array initialization is an action to give initial elements to a variable. We can initialize array values simultaneously with the declaration, or we can do it separately. This is basic code format to initialize array values

```
// initialization with array size
dataType[] variableName = new dataType[size];

// initialization simultaneously with declaration
dataType[] variableName = {element1, element2, element3};

// separately initialization
dataType[] variableName;
variableName = new dataType[]{element1, element2, element3};
```

Example:

<pre><code>// initialization with array size
int[] dayInts = new int[7]; // size set as 7

// initialization simultaneously with declaration
int[] numberArray= {1, 2, 3};
<strong>String[] nameArray= {"James", "John", "Doe"};
</strong>
// separately initialization
String[] alphabetArray;
alphabetArray= new String[]{"A", "B", "C"};
</code></pre>

### Access Element

We can access element of array using index. Index start from 0.

Example:

```
String[] nameArray= {"James", "John", "Doe"};

System.out.println(nameArray[0]); // will output James
System.out.println(nameArray[2]); // will output Doe
```

### Update Element

We can change element using index to, let's see this simple code

```
String[] nameArray= {"James", "John", "Doe"};

// change element
nameArray[2] = "Dane";

System.out.println(nameArray[2]); // will output Dane -> updated element
```

### Get Length of Array

We can get length of array using `length` property. Let's check this simple code example

```
String[] nameArray= {"James", "John", "Doe"};

System.out.println(nameArray.length); // will output 3
```

### Iterating Elements in Array

We can use loop `for` or `for-each`. to iterate all of array elements. Let's check this out

```
String[] nameArray= {"James", "John", "Doe"};

// USING FOR
for (int i = 0; i < nameArray.length; i++) {
    // i -> index, start with zero
    // i < nameArray.length -> continue_loop_condition

    // access element
    System.out.println(nameArray[i]);
}

// USING FOREACH
for (String name: nameArray) {
    // String name -> selected element in current iteration
    // name have String data type, because nameArray contain String elements
    
    System.out.println(name); // print selected element in current iteration
}
```

### Multidimensions Array

This concepts will able you to have array in 2 dimensions or more.

Let's see this simple example of 2 dimensions array.

```
int[][] matriks = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

System.out.println(matriks[0][0]); // will print 1
System.out.println(matriks[0][2]); // will print 3

System.out.println(matriks[1][2]); // will print 6
```
