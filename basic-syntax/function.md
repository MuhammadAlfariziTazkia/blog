---
description: Can used to implement DRY principle -> Don't Repeat your Code
---

# Function

Function is code block that can called or executed to solve a task

Best practice -> each function should have single functionality

Basic code syntax for function :&#x20;

```
<returnDataType> <functionName> (<paramType1> param1, <paramType2> param2, ...) {
    <statement>
}
```

Description :&#x20;

* `returnDataType` -> usually, the function will return the result value to the code line that called the function, it can be `int`, `float`, `String`, etc. But if we want the function just do the procedure without return anything, we can use `void` as `returnDataType`
* `functionName` -> the name of the function, should be represent the functionality of that function, so then the other programmer can easy to understand the purpose of the function without effort analyzing code statement
* `param` -> parameter of the function. When we called a function to do the task, sometimes we need to passing value to the function. For the example we want to create function to print the name based on user input. So the value need to passed to the function is the name of user input.&#x20;
  * **Argument** -> when we passing the value to the function
  * **Parameter** -> when the value received by the function
* `paramType` -> type of parameter, it can be `int`, `String`, `float`, etc

For the example we want to create a function to calculate the area of rectangle based on passed parameters of `length` and `width`

```
int calculateRectangleArea (int length, int width) {
    int area = length * width;
    return area;
}
```

To call function from the main function, it can be like this :&#x20;

```
public static void main (String [] args) {
    int length = 10;
    int width = 20;
    
    System.out.println(calculateRectangleArea(length, width)); // will print 200
    
    int newArea = calculateRectangleArea(40, 5);
    System.out.println(newArea);  // will print 200
```

## Without VS With Function

### Without

Imagine that we want to print detail information of the person, and we do this if we not use a function (without function) :&#x20;

```
public static void main (String [] args) {
    System.out.println("Name : Dinda");
    System.out.println("Gender : Female");
    System.out.println("Phone : 123123123");
    
    System.out.println("Name : Rudy");
    System.out.println("Gender : Male");
    System.out.println("Phone : 3452345");
    
    System.out.println("Name : Andy");
    System.out.println("Gender : Male");
    System.out.println("Phone : 34564656");
    
    System.out.println("Name : Melisa");
    System.out.println("Gender : Female");
    System.out.println("Phone : 56456");
          
}
```

We just need to do the simple task, just want to print name, gender, and phone of 4 persons but need to write about 12 code line? how about if we want to print detail information of 20 person? how about 100 person? It's scared right?

And imagine if we need to change wording of "Name" with "Fullname", we need to change all of "Name" in every `System.out.println("Name...` besides that it's need a much effort, **there is a risk that one of them can skipped to be changed**.

### With

And let's see how we solve this using a function:

```
void printDetailInformation(String name, String gender, String phone) {
    System.out.println("Name : " + name);
    System.out.println("Gender : " + gender);
    System.out.println("Phone : " + phone);
}

public static void main (String[]args) {
    printDetailInformation("Dinda", "Female", "123123123");
    printDetailInformation("Rudy", "Male", "3452345");
    printDetailInformation("Andy", "Male", "34564656");
    printDetailInformation("Melisa", "Female", "56456");
}
```

This make it easier to write a code, read, and maintain right?

And if someday we need to change wording of "Name" -> "Fullname", all we need just change one time the "Name" wording in the function, and this is will remove **risk that one of them can skipped to be changed.**
