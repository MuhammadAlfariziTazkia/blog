---
description: Key-value data structure
---

# Map

Map is a data structure that we can use in Java to store pair of key-value data. If we using index that start from zero to access data in  a `List`, in a `Map` we can using key to access the data. Key in a map can be int, String, etc.

Same as a `List` class, `Map` class also is an interface class which mean actually there is no function or method implementation in a `Map` class, so it's need an implementation class. `HashMap` is on of implementation class that we need to using `Map`. We talk about `HashMap` in the next section.

Imagine we want to store personal information data in `personalInfo` variable that use `Map` data structure.

Personal information will contain `name`, `age`, and `nationality` of a person, and this is how to manipulate `personalInfo` data using a Map

## Create

This is a basic syntax to create a `Map` using `HashMap` implementation

```
Map<keyDataType, valueDataType> mapVar = new HashMap<>();
```

As we mention before, we want to create `personalInfo` var that contain information of `name`, `age`, `nationality`

| Key         | Key Data Type | Value Example | Value Data Type |
| ----------- | ------------- | ------------- | --------------- |
| name        | String        | "John Doe"    | String          |
| age         | String        | 18            | Integer         |
| nationality | String        | "Indonesia"   | String          |

From the table above, we can see that all of key type is a `String`, but our value will have `String` and `int` data type. So :&#x20;

* `keyDataType` -> `String`
* `valueDataType` -> `String` and `Integer` , because of `String` and `Integer` is a subclass of `Object` , we can use `Object` for data type of value. If now you feel strange with `subclass` or `Object`, is okay because it's part of OOP concepts, and we will talk about this later. For now let's say `Object` is general form of `String` and `Integer` data type

So here is the way to create `personalInfo` variable

```
Map<String, Object> personalInfo = new HashMap<>();
```

## Add key-value Pair

We just need to use `put()` function that need 2 parameters, first parameter is a key and last parameter is a value.

```
personalInfo.put("name", "John Doe");
personalInfo.put("age", 18);
personalInfo.put("nationality", "Indonesia");
```

## Get Value

Unlike list that access value by using index number, to access value in a Map we can use their key instead. This is an example

```
String name = personalInfo.get("name");
System.out.println(name); // this will print "John Doe"
```

## Update Value

To update value in a Map, we can use `put()` function too, but the key in the first parameter it should exist in a Map. If the key is not exist, program will **Add key-value Pair** instead.

The second parameter that need to pass is updated value. So this is an example for update value in a Map

```
personalInfo.put("name", "John Doe Updated Name"); // will update the value
System.out.println(personalInfo.get("name")); // will output "John Doe Updated Name"

personalInfo.put("status", "married"); // this will add new key-value pair in our map
// because currently there is no "status" key in our map
```

## Remove Value

We just need to call `remove()` function along with key of value that need to be removed

```
personalInfo.remove("status");
```

## Is the Key Exist?

To check is the key exist or not in our map, we can using `containsKey()` function like this

```
System.out.println(personalInfo.containsKey("name")); 
// will output true because we have "name" key

System.out.println(personalInfo.containsKey("school")); 
// will return false because we dont have this key
```

## Is the Value Exist?

Similar with the key, we need to call `containsValue()` for check is the value is exist or not

```
System.out.println(personalInfo.containsValue(18));
// will output true because 18 is the value of key "age"
```

## Get Key Set

To get the set of the key in our map, we can use function `keySet()`

```
System.out.println(personalInfo.keySet());
```

## Get Values

To get the list of values that contains in our map, we can use `values()` function

```
System.out.println(personalInfo.values());
```
