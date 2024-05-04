# OOPs Concept ❤🍕

**Links:**

- [Class & Object](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
    - [Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class-)
    - [Object](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#object-)
- [Class Vs Structs](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class-vs-structs-)

## **Class & Object:** [🏠](hthttps://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Certainly! Let's start with explanations for class and object in C#, along with examples and scenarios:

### **Class:** [🏠](hthttps://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, a class is a blueprint or template for creating objects. It defines the properties, methods, events, and fields that characterize a particular type of object. Classes encapsulate data and behavior into a single unit, promoting code reusability, maintainability, and organization.

**Example: Defining a Class**

```csharp
using System;

class Car
{
    // Fields (member variables)
    public string Make;
    public string Model;
    public int Year;

    // Constructor
    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }

    // Method
    public void StartEngine()
    {
        Console.WriteLine($"Starting the engine of {Year} {Make} {Model}");
    }
}
```

### **Object:** [🏠](hthttps://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

An object is an instance of a class. It represents a specific realization of the class's blueprint, with its unique set of data and behavior. Objects are created using the `new` keyword, which allocates memory and initializes the object based on the class definition.

**Example: Creating and Using Objects**

```csharp
using System;

class Program
{
    static void Main()
    {
        // Creating objects (instances) of the Car class
        Car car1 = new Car("Toyota", "Camry", 2020);
        Car car2 = new Car("Honda", "Accord", 2018);

        // Accessing object properties
        Console.WriteLine($"Car 1: {car1.Year} {car1.Make} {car1.Model}");
        Console.WriteLine($"Car 2: {car2.Year} {car2.Make} {car2.Model}");

        // Invoking object methods
        car1.StartEngine();
        car2.StartEngine();
    }
}
```

**Output:**
```
Car 1: 2020 Toyota Camry
Car 2: 2018 Honda Accord
Starting the engine of 2020 Toyota Camry
Starting the engine of 2018 Honda Accord
```

### Scenarios:

1. **Creating Multiple Objects**: You can create multiple objects of the same class, each representing a different instance with its own unique data and behavior.

2. **Accessing Properties and Methods**: Objects allow you to access and manipulate their properties and invoke their methods to perform specific actions.

3. **Encapsulation and Modularity**: Classes encapsulate related data and behavior, promoting modularity and enabling you to organize your code into reusable components.

4. **Code Reusability**: Once defined, a class can be instantiated multiple times in different parts of your program, promoting code reusability and reducing redundancy.

In summary, classes and objects in C# facilitate the creation of reusable, modular, and organized code by encapsulating data and behavior into cohesive units. By understanding their concepts and usage, you can effectively model real-world entities and implement complex systems in your C# programs.

## **Class Vs Structs:** [🏠](hthttps://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Sure, let's provide a more detailed comparison of classes and structs in C#:

| Feature           | Class                                                | Struct                                                |
|-------------------|------------------------------------------------------|-------------------------------------------------------|
| Purpose           | Classes are primarily used for creating reference types, which are objects that reside on the heap. They allow you to define complex data structures with behavior, encapsulation, and identity. | Structs are primarily used for creating value types, which are lightweight data containers that store their data directly on the stack or inline within other data structures. They are often used for representing simple data types such as numbers, points, or small data structures. |
| Memory Allocation | Objects of classes are allocated on the heap, which is a managed memory pool. This allows for dynamic memory allocation and enables objects to be accessed from anywhere in the program. | Structs are typically allocated on the stack or inline within other data structures. Stack allocation is faster than heap allocation but comes with limitations such as size restrictions and limited scope. |
| Inheritance       | Classes support inheritance, which allows one class to inherit properties and behavior from another class. This enables code reuse, polymorphism, and the creation of class hierarchies. | Structs do not support inheritance. They are sealed by default, meaning they cannot be used as base classes and cannot have derived classes. |
| Default Constructor | Classes have a default constructor provided by the compiler if no constructor is explicitly defined. This default constructor initializes the object's fields to their default values. | Structs also have a default constructor provided by the compiler if no constructor is explicitly defined. However, unlike classes, structs cannot have parameterless constructors if any other constructor is explicitly defined. |
| Constructors      | Classes can have parameterized constructors, allowing you to initialize object instances with specific values during construction. This provides flexibility in object initialization and allows for different object states. | Structs can also have parameterized constructors, allowing you to initialize struct instances with specific values during construction. However, structs cannot have a parameterless constructor if any other constructor is explicitly defined. |
| Destructors       | Classes support destructors, also known as finalizers, which are special methods called when an object is garbage collected. Destructors are used to release unmanaged resources held by the object. | Structs do not support destructors. Since structs are value types and are typically allocated on the stack, they do not require explicit cleanup and are automatically deallocated when they go out of scope. |
| Boxing/Unboxing   | Classes support boxing and unboxing, which is the process of converting a value type to a reference type (boxing) and vice versa (unboxing). Boxing allows value types to be treated as objects, but it comes with performance overhead and potential memory allocation. | Structs do not support boxing and unboxing. Since structs are value types, they are directly stored in memory without the need for additional heap allocation. This results in better performance and reduced memory overhead compared to classes. |
| Performance       | Classes typically have slower performance compared to structs due to heap allocation and the overhead of reference types. Accessing objects on the heap involves indirection and additional memory lookups, which can impact performance, especially in performance-critical applications. | Structs generally have better performance compared to classes due to stack allocation and the efficiency of value types. Structs are stored directly in memory without the overhead of reference types, resulting in faster access and reduced memory overhead. However, structs should be used judiciously, as excessive stack allocation can lead to stack overflow errors and reduced performance in certain scenarios. |
| Usage             | Classes are used for modeling complex objects with behavior, encapsulation, and identity. They are suitable for representing entities with rich functionality, such as objects in object-oriented programming paradigms. | Structs are used for representing lightweight data containers with simple data types. They are suitable for storing small data structures, passing parameters by value, and improving performance in memory-constrained or performance-critical scenarios. |

### When to Use Classes:

- Use classes for complex objects with behavior, state, and identity.
- When you need to support inheritance and polymorphism.
- When you want to model entities with a significant amount of data and behavior.

### When to Use Structs:

- Use structs for lightweight data containers that represent simple values.
- When you need better performance and memory efficiency, especially for small data structures.
- When you want to work with value types directly without the overhead of heap allocation.

In summary, while classes and structs share similarities in their role as data types in C#, they have distinct characteristics and are used for different purposes. Classes are suitable for modeling complex objects with behavior and identity, while structs are more appropriate for representing lightweight data containers with simple data types. Understanding the differences between classes and structs is essential for choosing the appropriate type for your specific requirements and optimizing the performance and memory usage of your applications.

## 