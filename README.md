# MapStruct

MapStruct is a Swift class used for mapping and accessing values from a dictionary-like structure. It provides a convenient subscript syntax for getting and setting values based on keys.


##Installation

To install the `MapStruct` package in your Swift project, follow these steps:

1. Open your project in Xcode.

2. Go to the project navigator and select your project.

3. Select your project's target, then go to the "Swift Packages" tab.

4. Click the "+" button to add a new package dependency.

5. In the dialog that appears, enter the URL of the `MapStruct` package repository: `https://github.com/ace1ofspades/MapStruct`

6. Choose the version or branch you want to use. You can select a specific release version, a branch, or even a commit hash.

7. Click "Next" and Xcode will start resolving the package dependency.

8. Once the dependency is resolved, you can choose the target(s) where you want to add the `MapStruct` package.

9. Click "Finish" to add the package to your project.

Xcode will automatically fetch the `MapStruct` package and integrate it into your project. You can then import and use the `MapStruct` class in your code.


## Usage

The `MapStruct` class can be used to map and access values from a dictionary. Here is the basic usage of the class:

```swift
let mapStruct = MapStruct(object: someObject)

// Accessing values
let value = mapStruct["key"]

// Setting values
mapStruct["key"] = newValue
```
In the above example, we demonstrate how to set values in the `MapStruct` instance using the subscript syntax. By assigning a new value to a specific key, you can update the value in the underlying dictionary-like structure.

To set a value, use the following syntax:

```swift
mapStruct["key"] = newValue
```

Make sure to replace `"key"` with the desired key and `newValue` with the new value you want to assign. This allows you to set specific values in the underlying dictionary-like structure.

It's important to note that if the specified key already exists in the underlying dictionary, the value will be updated. If the key doesn't exist, a new key-value pair will be created with the specified value.

Feel free to use this syntax to set values in the `MapStruct` instance according to your requirements. You can update existing values or add new values dynamically.

---

This section emphasizes the importance of replacing `"key"` with the desired key and `newValue` with the new value you want to assign. By doing so, you can set specific values in the `MapStruct` instance.

Features
--------

The `MapStruct` class provides the following features:

- Subscript Access: You can access values from the underlying dictionary-like structure using the subscript syntax. This allows you to conveniently retrieve values based on their corresponding keys.

- Value Mapping: The class handles values of type `DecodeAny` and automatically unwraps them to their underlying value. This simplifies the process of working with complex or nested data structures.

- Initialization: The `MapStruct` class can be initialized with different types of objects. It accepts dictionaries, `Data` objects, or any other object that can be deserialized into a dictionary using JSONSerialization. This flexibility allows you to easily create instances of `MapStruct` from various data sources.

- Dynamic Value Setting: You can set values in the `MapStruct` instance using the subscript syntax. By assigning a new value to a specific key, you can update the value in the underlying dictionary-like structure. This provides a convenient way to modify the data stored in the `MapStruct` instance.

- Customization: The `MapStruct` class can be subclassed and customized according to your specific needs. You can override methods such as `configure()` and `printForDebug(_: _: _: _)` to add custom behavior or logging functionality.

These features make the `MapStruct` class a versatile tool for working with dictionary-like structures and accessing values in a straightforward manner.

Please note that these features are provided as part of the `MapStruct` class and can be utilized based on your requirements.

Initialization
--------------

The `MapStruct` class offers flexible initialization options:

- **Dictionary Initialization**: You can initialize a `MapStruct` instance by passing a dictionary object as the parameter. The dictionary will be used as the underlying data structure for key-value access.

- **Data Initialization**: If you have a `Data` object containing serialized JSON data, you can initialize a `MapStruct` instance by passing the `Data` object as the parameter. The data will be deserialized into a dictionary using JSONSerialization, which will serve as the underlying data structure.

Here's an example of initializing a `MapStruct` instance with different types of objects:

```swift
let dictionary: [String: Any] = ["key1": "value1", "key2": 123]
let mapStructFromDictionary = MapStruct(dictionary)

let jsonData = Data("{\"key1\": \"value1\", \"key2\": 123}".utf8)
let mapStructFromData = MapStruct(jsonData)
```

In the above example, we create two instances of `MapStruct`. The first one is initialized with a dictionary object, and the second one is initialized with a `Data` object containing serialized JSON data.

By supporting various types of initialization, the `MapStruct` class allows you to easily create instances from different data sources and start working with the underlying dictionary-like structure.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
