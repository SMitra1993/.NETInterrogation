# OOPs Concept ❤🍕

**Links:**

- [Class & Object](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
    - [Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class-)
    - [Object](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#object-)
- [Different ways to create Object](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#different-ways-to-create-objects-)
- [Class Vs Structs](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class-vs-structs-)
- [Early and late binding in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#early-and-late-binding-in-c-)
    - [Early Binding](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#early-binding-)
    - [Late Binding](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#late-binding-)
- [Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#inheritance-)
- [Types on Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#types-on-inheritance-)
    - [Single Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#1-single-inheritance-)
    - [Multilevel Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#2-multilevel-inheritance-)
    - [Hierarchical Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#3-hierarchical-inheritance-)
    - [Multiple Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#4-multiple-inheritance-c-doesnt-support-multiple-inheritance-directly-)
    - [Hybrid Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#5-hybrid-inheritance-)
- [Multiple Inheritance](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#multiple-inheritance-)
- [Encapsulation](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#encapsulation-)
- [Abstraction](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#abstraction-)
- [Encapsulation Vs Abstraction](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#encapsulation-vs-abstraction-)
- [Polymorphism](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#polymorphism-)
- [Inheritance Vs Polymorphism](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#inheritance-vs-polymorphism-)
- [`this` Keyword](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#this-keyword-)
- [Static Class vs Non-static Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#static-class-vs-non-static-class-)
- [Partial Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#partial-class-)
- [Shallow Copy and Deep Copy](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#shallow-copy-and-deep-copy-)
- [Inheritance in Interface](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#inheritance-in-interface-)
- [Inheritance in Constructors](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#inheritance-in-interface-)
- [Abstract Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#abstract-class-)
- [Interface in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#interface-in-c-)
- [Why do we use interface in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#why-do-we-use-interface-in-c-)
- [Abstract Class Vs Interface](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#abstract-class-vs-interface-)
- [Sealed Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#sealed-class-)
- [Delegates vs Interfaces in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#delegates-vs-interfaces-in-c-)
- [Explicit Interface](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#explicit-interface-)

## **Class & Object:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

### Class: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

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

### Object: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept--)

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

## **Different ways to create Object:**

In C#, there are several ways to create objects, each with its own syntax and use cases. Let's explore each method with examples and output:

### 1. Using the `new` Keyword:

The most common way to create objects in C# is by using the `new` keyword followed by the class name and optional constructor arguments.

#### Example:

```csharp
public class Person
{
    public string Name { get; set; }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class
        Person person = new Person();
        person.Name = "Alice";

        Console.WriteLine("Person's name: " + person.Name);
    }
}
```

#### Output:

```
Person's name: Alice
```

### 2. Using Object Initializer:

C# allows you to initialize an object's properties at the time of creation using object initializer syntax.

#### Example:

```csharp
public class Person
{
    public string Name { get; set; }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class with object initializer
        Person person = new Person { Name = "Bob" };

        Console.WriteLine("Person's name: " + person.Name);
    }
}
```

#### Output:

```
Person's name: Bob
```

### 3. Using Constructor Overloading:

If a class has multiple constructors, you can choose which constructor to invoke based on the provided arguments.

#### Example:

```csharp
public class Person
{
    public string Name { get; set; }

    public Person(string name)
    {
        Name = name;
    }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class using a specific constructor
        Person person = new Person("Charlie");

        Console.WriteLine("Person's name: " + person.Name);
    }
}
```

#### Output:

```
Person's name: Charlie
```

### 4. Using Factory Method:

A factory method is a static method that creates and returns instances of a class.

#### Example:

```csharp
public class Person
{
    public string Name { get; set; }

    private Person(string name)
    {
        Name = name;
    }

    // Factory method to create Person objects
    public static Person Create(string name)
    {
        return new Person(name);
    }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class using a factory method
        Person person = Person.Create("David");

        Console.WriteLine("Person's name: " + person.Name);
    }
}
```

#### Output:

```
Person's name: David
```

### 5. Using Reflection:

Reflection allows you to create objects dynamically at runtime using the `Activator.CreateInstance` method.

#### Example:

```csharp
using System;

public class Person
{
    public string Name { get; set; }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class using reflection
        Type type = typeof(Person);
        var person = Activator.CreateInstance(type);

        // Setting property value using reflection
        type.GetProperty("Name").SetValue(person, "Emily");

        Console.WriteLine("Person's name: " + type.GetProperty("Name").GetValue(person));
    }
}
```

#### Output:

```
Person's name: Emily
```
### 6. Creating an Array of Objects:

You can create an array of objects by specifying the array type followed by square brackets `[]` and using the `new` keyword to allocate memory for the array.

#### Example:

```csharp
using System;

public class Person
{
    public string Name { get; set; }
}

class Program
{
    static void Main()
    {
        // Creating an array of Person objects
        Person[] people = new Person[2];

        // Initializing individual objects in the array
        people[0] = new Person { Name = "Alice" };
        people[1] = new Person { Name = "Bob" };

        // Accessing objects in the array
        foreach (var person in people)
        {
            Console.WriteLine("Person's name: " + person.Name);
        }
    }
}
```

#### Output:

```
Person's name: Alice
Person's name: Bob
```

### 7. Creating a Reference to an Existing Object:

You can create a reference to an existing object by assigning the object to a new variable. Both the original object and the reference point to the same memory location.

#### Example:

```csharp
using System;

public class Person
{
    public string Name { get; set; }
}

class Program
{
    static void Main()
    {
        // Creating an object of the Person class
        Person originalPerson = new Person { Name = "Charlie" };

        // Creating a reference to the original object
        Person referencePerson = originalPerson;

        // Modifying the original object
        originalPerson.Name = "David";

        // Accessing the object through the reference
        Console.WriteLine("Reference Person's name: " + referencePerson.Name);
    }
}
```

#### Output:

```
Reference Person's name: David
```

### Description:

- **Using the `new` Keyword**: This is the standard way to create objects in C#. It calls the class's constructor to initialize the object.
- **Using Object Initializer**: Allows you to initialize object properties directly after creation, improving readability.
- **Using Constructor Overloading**: Enables you to create objects using different sets of parameters, providing flexibility.
- **Using Factory Method**: A design pattern that encapsulates object creation logic, allowing for more complex object creation scenarios.
- **Using Reflection**: Allows for dynamic object creation at runtime, useful for scenarios where object types are determined at runtime or when creating objects from dynamically loaded assemblies.
- **Creating an Array of Objects**: Allows you to store multiple objects of the same type in an array structure, providing convenient access and iteration over the objects.
- **Creating a Reference to an Existing Object**: Creates a new variable that refers to the same object in memory as the original variable. Modifications made to the original object are reflected in the reference object, as they point to the same memory location.

## **Class Vs Structs:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

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

## **Early and late binding in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Early and late binding refer to the timing at which method calls are resolved to their corresponding implementations in object-oriented programming languages like C#.

### Early Binding: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Early binding, also known as static binding or compile-time binding, occurs when the method calls are resolved at compile time. In early binding, the compiler knows exactly which method implementation will be invoked based on the declared type of the object or variable.

**Example:**

```csharp
using System;

class Program
{
    static void Main()
    {
        // Early Binding
        Shape shape = new Circle(); // Declared type: Shape, Actual type: Circle
        shape.Draw(); // Resolved at compile time to Shape.Draw()
    }
}

class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape");
    }
}

class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle");
    }
}
```

In this example, the method call `shape.Draw()` is resolved to `Shape.Draw()` at compile time because the declared type of `shape` is `Shape`. This is early binding because the compiler knows the type of the object at compile time and can determine the method to call without needing to look at the runtime type.

### Late Binding: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Late binding, also known as dynamic binding or runtime binding, occurs when the method calls are resolved at runtime. In late binding, the actual method implementation to be invoked is determined dynamically based on the runtime type of the object.

**Example:**

```csharp
using System;

class Program
{
    static void Main()
    {
        // Late Binding
        dynamic shape = new Circle(); // Actual type: Circle
        shape.Draw(); // Resolved at runtime to Circle.Draw()
    }
}

class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape");
    }
}

class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle");
    }
}
```

In this example, the method call `shape.Draw()` is resolved to `Circle.Draw()` at runtime because the actual type of `shape` is `Circle`. This is late binding because the method to call is determined dynamically based on the runtime type of the object.

### Summary:

- Early binding occurs at compile time and provides better performance because the method calls are resolved statically.
- Late binding occurs at runtime and provides more flexibility because the method calls are resolved dynamically based on the actual type of the object.
- Early binding is typically used with static types (e.g., classes), while late binding is often used with dynamic types (e.g., `dynamic` keyword) or scenarios where the type of the object is not known until runtime.

Understanding the concepts of early and late binding is important for designing flexible and efficient object-oriented systems in C# and other programming languages.

## **Inheritance:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Inheritance is a fundamental concept in object-oriented programming (OOP) where a new class (called a derived class or subclass) is created from an existing class (called a base class or superclass). The derived class inherits properties and behaviors (methods) from the base class, allowing code reuse and promoting a hierarchical structure in software design.

### Scenario:

Consider a scenario where you are developing a software system for managing different types of vehicles. You have various types of vehicles such as cars, trucks, and motorcycles. These vehicles share common properties and behaviors, such as a manufacturer, model, and fuel type, but they also have distinct characteristics. Inheritance can be used to model this relationship efficiently.

### Example:

```csharp
using System;

// Base class representing a shape
class Shape
{
    public string Color { get; set; }
    public int X { get; set; }
    public int Y { get; set; }

    // Constructor
    public Shape(string color, int x, int y)
    {
        Color = color;
        X = x;
        Y = y;
    }

    // Method to display shape information
    public virtual void DisplayInfo()
    {
        Console.WriteLine($"Color: {Color}, Position: ({X}, {Y})");
    }
}

// Derived class representing a circle
class Circle : Shape
{
    public double Radius { get; set; }

    // Constructor
    public Circle(string color, int x, int y, double radius) : base(color, x, y)
    {
        Radius = radius;
    }

    // Method to display circle information
    public override void DisplayInfo()
    {
        base.DisplayInfo();
        Console.WriteLine($"Radius: {Radius}");
    }
}

// Derived class representing a rectangle
class Rectangle : Shape
{
    public double Width { get; set; }
    public double Height { get; set; }

    // Constructor
    public Rectangle(string color, int x, int y, double width, double height) : base(color, x, y)
    {
        Width = width;
        Height = height;
    }

    // Method to display rectangle information
    public override void DisplayInfo()
    {
        base.DisplayInfo();
        Console.WriteLine($"Width: {Width}, Height: {Height}");
    }
}

class Program
{
    static void Main()
    {
        // Creating objects of derived classes
        Circle circle = new Circle("Red", 10, 20, 5);
        Rectangle rectangle = new Rectangle("Blue", 30, 40, 10, 15);

        // Displaying information of shapes
        Console.WriteLine("Circle:");
        circle.DisplayInfo();

        Console.WriteLine("\nRectangle:");
        rectangle.DisplayInfo();
    }
}
```

**Output:** 

```csharp
Circle:
Color: Red, Position: (10, 20)
Radius: 5

Rectangle:
Color: Blue, Position: (30, 40)
Width: 10, Height: 15
```

### Explanation:

- The `Shape` class serves as the base class representing common properties and behavior shared by all shapes.
- The `Circle` and `Rectangle` classes are derived from the Shape class, inheriting its properties and behavior.
- Each derived class has its own specific properties (`Radius` for `Circle` and `Width` and `Height` for `Rectangle`) and overrides the `DisplayInfo` method to display shape-specific information along with the base information.
- In the `Main` method, objects of the derived classes are created and their information is displayed, demonstrating how inheritance allows for code reuse and polymorphic behavior.

### Benefits of Inheritance:

1. **Code Reusability**: Inheritance allows you to reuse code defined in the base class in the derived class, reducing redundancy and promoting efficient code organization.
  
2. **Hierarchical Structure**: Inheritance facilitates the creation of a hierarchical structure, where classes can be organized into parent-child relationships based on commonality and specialization.
  
3. **Polymorphism**: Inheritance enables polymorphic behavior, where objects of the derived class can be treated as objects of the base class, allowing for flexibility and extensibility in software design.

Inheritance is a powerful mechanism in OOP that promotes code reuse, enhances maintainability, and facilitates a clear and structured design of software systems.

## **Types on Inheritance:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Inheritance in object-oriented programming (OOP) allows a class (called a derived class or subclass) to inherit properties and behaviors from another class (called a base class or superclass). There are various types of inheritance, each serving different purposes and providing different levels of flexibility in software design. Let's explore some common types of inheritance with examples, scenarios, and outputs:

### 1. Single Inheritance: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Single inheritance occurs when a class inherits properties and behaviors from only one superclass.

**Example:**
```csharp
using System;

// Base class
class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}

// Derived class inheriting from Animal
class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog is barking.");
    }
}

class Program
{
    static void Main()
    {
        Dog myDog = new Dog();
        myDog.Eat();  // Inherited method from Animal class
        myDog.Bark(); // Method defined in Dog class
    }
}
```

**Output:**
```
Animal is eating.
Dog is barking.
```

### 2. Multilevel Inheritance: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Multilevel inheritance occurs when a derived class inherits from another derived class, creating a chain of inheritance.

**Example:**
```csharp
using System;

// Base class
class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}

// Derived class inheriting from Animal
class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog is barking.");
    }
}

// Derived class inheriting from Dog
class Puppy : Dog
{
    public void Play()
    {
        Console.WriteLine("Puppy is playing.");
    }
}

class Program
{
    static void Main()
    {
        Puppy myPuppy = new Puppy();
        myPuppy.Eat();  // Inherited method from Animal class
        myPuppy.Bark(); // Inherited method from Dog class
        myPuppy.Play(); // Method defined in Puppy class
    }
}
```

**Output:**
```
Animal is eating.
Dog is barking.
Puppy is playing.
```

### 3. Hierarchical Inheritance: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Hierarchical inheritance occurs when multiple derived classes inherit from the same base class.

**Example:**
```csharp
using System;

// Base class
class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}

// Derived class inheriting from Animal
class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog is barking.");
    }
}

// Another derived class inheriting from Animal
class Cat : Animal
{
    public void Meow()
    {
        Console.WriteLine("Cat is meowing.");
    }
}

class Program
{
    static void Main()
    {
        Dog myDog = new Dog();
        myDog.Eat();  // Inherited method from Animal class
        myDog.Bark(); // Method defined in Dog class

        Cat myCat = new Cat();
        myCat.Eat();  // Inherited method from Animal class
        myCat.Meow(); // Method defined in Cat class
    }
}
```

**Output:**
```
Animal is eating.
Dog is barking.
Animal is eating.
Cat is meowing.
```

### 4. Multiple Inheritance (C# doesn't support multiple inheritance directly): [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Multiple inheritance occurs when a class inherits from more than one superclass. Although C# doesn't support multiple inheritance directly, you can achieve similar behavior using interfaces.

**Example:**
```csharp
using System;

// Interface 1
interface IWalkable
{
    void Walk();
}

// Interface 2
interface ISwimmable
{
    void Swim();
}

// Derived class implementing interfaces
class Human : IWalkable, ISwimmable
{
    public void Walk()
    {
        Console.WriteLine("Human is walking.");
    }

    public void Swim()
    {
        Console.WriteLine("Human is swimming.");
    }
}

class Program
{
    static void Main()
    {
        Human person = new Human();
        person.Walk(); // Method defined in IWalkable interface
        person.Swim(); // Method defined in ISwimmable interface
    }
}
```

**Output:**
```
Human is walking.
Human is swimming.
```

### 5. Hybrid Inheritance: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Hybrid inheritance is a combination of two or more types of inheritance, such as single, multilevel, or hierarchical inheritance. It involves multiple inheritance paths and can lead to complex class hierarchies.

**Example:**

```csharp
using System;

// Base class
class Animal
{
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}

// Derived class inheriting from Animal
class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog is barking.");
    }
}

// Another derived class inheriting from Animal
class Cat : Animal
{
    public void Meow()
    {
        Console.WriteLine("Cat is meowing.");
    }
}

// Derived class inheriting from both Dog and Cat
class CatDog : Dog
{
    public void Sleep()
    {
        Console.WriteLine("CatDog is sleeping.");
    }
}

class Program
{
    static void Main()
    {
        CatDog myCatDog = new CatDog();
        myCatDog.Eat();  // Inherited method from Animal class
        myCatDog.Bark(); // Method defined in Dog class
        myCatDog.Meow(); // Method inherited from Cat class (due to hierarchy)
        myCatDog.Sleep(); // Method defined in CatDog class
    }
}
```

**Output:**

```
Animal is eating.
Dog is barking.
Cat is meowing.
CatDog is sleeping.
```

### Conclusion:

Different types of inheritance provide varying levels of flexibility and hierarchy in software design. Single inheritance, multilevel inheritance, hierarchical inheritance, and interface-based multiple inheritance (achieved using interfaces) are commonly used in object-oriented programming to model relationships between classes and promote code reuse. Understanding these types of inheritance helps in designing well-structured and maintainable software systems.

## **Multiple Inheritance:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

### Problem:

In C#, multiple inheritance, where a class inherits from more than one class, is not directly supported. This limitation is primarily due to the potential issues that arise from the diamond problem or ambiguity problem.

### Example:

Consider the following scenario:

```csharp
using System;

// Base class A
class A
{
    public void MethodA()
    {
        Console.WriteLine("MethodA from class A");
    }
}

// Base class B
class B
{
    public void MethodA()
    {
        Console.WriteLine("MethodA from class B");
    }

    public void MethodB()
    {
        Console.WriteLine("MethodB from class B");
    }
}

// Derived class C inheriting from classes A and B
class C : A, B
{
    // Class C attempts to inherit from both A and B
    // However, C# does not support multiple inheritance for classes
}

class Program
{
    static void Main()
    {
        // Attempt to create an instance of class C
        C objC = new C();
    }
}
```

In this example, we have two base classes `A` and `B`, each with their own methods. Class `C` attempts to inherit from both `A` and `B`, but this is not allowed in C#. When you try to compile the code, you'll encounter a compilation error stating that "Class 'C' cannot have multiple base classes".

### Explanation:

1. **Ambiguity**: If both base classes `A` and `B` have methods with the same name, such as `MethodA()` and `MethodB()`, the derived class `C` would inherit both of these methods. If you call `MethodA()` on an instance of `C`, it's unclear whether you meant to call `MethodA()` from class `A` or `B`.

2. **Diamond Problem**: If class `C` indirectly inherits from two base classes `A` and `B` (e.g., if class `D` inherits from `A` and `B`, and class `C` inherits from `D`), and both `A` and `B` have a common base class (e.g., class `Object`), there can be ambiguity in resolving method calls and memory allocation, leading to the diamond problem.

### Solution:

You can achieve multiple inheritance behavior using interfaces. Interfaces define contracts that classes can implement, allowing them to provide implementations for multiple behaviors. Let's explore how to achieve multiple inheritance using interfaces with scenarios, examples, and outputs:

### Scenario:

Consider a scenario where you have various types of vehicles, and you want to model their capabilities such as driving on land and floating on water. You need a way to represent both land and water functionalities in your vehicle classes.

### Example:

```csharp
using System;

// Interface representing land-based functionality
interface ILandVehicle
{
    void Drive();
}

// Interface representing water-based functionality
interface IWaterVehicle
{
    void Float();
}

// Car class implementing ILandVehicle
class Car : ILandVehicle
{
    public void Drive()
    {
        Console.WriteLine("Car is driving on land.");
    }
}

// Boat class implementing IWaterVehicle
class Boat : IWaterVehicle
{
    public void Float()
    {
        Console.WriteLine("Boat is floating on water.");
    }
}

// AmphibiousVehicle class implementing both ILandVehicle and IWaterVehicle
class AmphibiousVehicle : ILandVehicle, IWaterVehicle
{
    public void Drive()
    {
        Console.WriteLine("Amphibious vehicle is driving on land.");
    }

    public void Float()
    {
        Console.WriteLine("Amphibious vehicle is floating on water.");
    }
}

class Program
{
    static void Main()
    {
        // Creating instances of different vehicle types
        Car myCar = new Car();
        Boat myBoat = new Boat();
        AmphibiousVehicle myAmphibiousVehicle = new AmphibiousVehicle();

        // Using land-based functionality
        myCar.Drive(); // Output: Car is driving on land.
        myAmphibiousVehicle.Drive(); // Output: Amphibious vehicle is driving on land.

        // Using water-based functionality
        myBoat.Float(); // Output: Boat is floating on water.
        myAmphibiousVehicle.Float(); // Output: Amphibious vehicle is floating on water.
    }
}
```

### Output:

```
Car is driving on land.
Amphibious vehicle is driving on land.
Boat is floating on water.
Amphibious vehicle is floating on water.
```

### Explanation:

In this example:
- We define two interfaces `ILandVehicle` and `IWaterVehicle`, representing land-based and water-based functionality, respectively.
- Classes `Car` and `Boat` implement `ILandVehicle` and `IWaterVehicle`, respectively, providing implementations for the `Drive()` and `Float()` methods.
- The class `AmphibiousVehicle` implements both `ILandVehicle` and `IWaterVehicle`, combining land and water functionality into a single class.
- In the `Main` method, we create instances of `Car`, `Boat`, and `AmphibiousVehicle`, and demonstrate the use of both land-based and water-based functionality through method invocations.

### Conclusion:

By using interfaces, you can achieve multiple inheritance-like behavior in C#, allowing classes to implement multiple contracts and providing flexibility in defining class hierarchies and behaviors. This approach promotes code reuse, maintainability, and extensibility in software development.

## **Encapsulation:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Encapsulation is one of the fundamental principles of object-oriented programming (OOP) and refers to the bundling of data (attributes) and methods (behaviors) that operate on the data within a single unit, typically a class. It helps in hiding the internal state of an object and only exposing the necessary functionalities to interact with it. Encapsulation ensures data integrity, enhances security, and facilitates code maintenance and reuse. Let's explore encapsulation with scenarios, an example, and output:

### Scenario 1:

### Example:

```csharp
using System;

class BankAccount
{
    // Private fields
    private string accountNumber;
    private double balance;

    // Constructor
    public BankAccount(string accNumber, double initialBalance)
    {
        accountNumber = accNumber;
        balance = initialBalance;
    }

    // Public method to deposit money
    public void Deposit(double amount)
    {
        if (amount > 0)
        {
            balance += amount;
            Console.WriteLine($"{amount} deposited successfully.");
        }
        else
        {
            Console.WriteLine("Invalid deposit amount.");
        }
    }

    // Public method to withdraw money
    public void Withdraw(double amount)
    {
        if (amount > 0 && amount <= balance)
        {
            balance -= amount;
            Console.WriteLine($"{amount} withdrawn successfully.");
        }
        else
        {
            Console.WriteLine("Insufficient balance or invalid withdrawal amount.");
        }
    }

    // Public method to check balance
    public double CheckBalance()
    {
        return balance;
    }
}

class Program
{
    static void Main()
    {
        // Creating a bank account
        BankAccount myAccount = new BankAccount("123456789", 1000);

        // Performing operations
        myAccount.Deposit(500); // Output: 500 deposited successfully.
        myAccount.Withdraw(200); // Output: 200 withdrawn successfully.
        
        // Checking balance
        double currentBalance = myAccount.CheckBalance();
        Console.WriteLine($"Current balance: {currentBalance}"); // Output: Current balance: 1300
    }
}
```

### Output:

```
500 deposited successfully.
200 withdrawn successfully.
Current balance: 1300
```

### Explanation:

In this example:
- We have a `BankAccount` class encapsulating private fields `accountNumber` and `balance`, and methods `Deposit`, `Withdraw`, and `CheckBalance`.
- The private fields ensure that the internal state of the bank account is hidden from external access, preventing unauthorized modification.
- The public methods `Deposit`, `Withdraw`, and `CheckBalance` provide controlled access to the account functionalities, enforcing business logic and maintaining data integrity.
- When creating an instance of `BankAccount` and performing operations, the internal state is manipulated through the public methods, maintaining encapsulation and ensuring proper data handling.

### Scenario 2:

### Example:

```csharp
using System;

class Person
{
    // Private fields
    private string name;
    private int age;

    // Property for Name with encapsulation
    public string Name
    {
        get { return name; }
        set
        {
            if (!string.IsNullOrEmpty(value))
                name = value;
            else
                Console.WriteLine("Name cannot be empty.");
        }
    }

    // Property for Age with encapsulation
    public int Age
    {
        get { return age; }
        set
        {
            if (value >= 0 && value <= 120)
                age = value;
            else
                Console.WriteLine("Invalid age.");
        }
    }

    // Constructor
    public Person(string name, int age)
    {
        Name = name; // Using property to set name
        Age = age;   // Using property to set age
    }

    // Public method to display person's information
    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}

class Program
{
    static void Main()
    {
        // Creating a person object
        Person person1 = new Person("John", 30);

        // Accessing properties
        person1.Name = "Alice"; // Output: Name cannot be empty. (since setting an empty name)
        person1.Age = 150;      // Output: Invalid age. (since age is out of range)
        person1.Age = 35;       // Output: (no output since age is valid)

        // Displaying person's information
        person1.DisplayInfo();  // Output: Name: John, Age: 35
    }
}
```

### Output:

```
Name cannot be empty.
Invalid age.
Name: John, Age: 35
```

### Explanation:

In this example:
- We have a `Person` class encapsulating private fields `name` and `age`, and properties `Name` and `Age`.
- The properties `Name` and `Age` use encapsulation to enforce validation logic (non-empty name, valid age range) before setting the values of the private fields.
- When creating an instance of `Person` and setting the properties, encapsulation ensures that only valid data is accepted and stored internally.
- The public method `DisplayInfo` allows external code to access the person's information in a controlled manner, maintaining encapsulation and data integrity.

### Benefits of Encapsulation:

1. **Data Hiding**: Encapsulation hides the internal state of an object, preventing direct access and modification, thus enhancing data security and integrity.
2. **Abstraction**: Encapsulation abstracts the implementation details, allowing users to interact with objects through well-defined interfaces without needing to understand the underlying complexities.
3. **Modularity**: Encapsulation promotes modularity by grouping related data and functionalities within a single unit (class), facilitating code organization, maintenance, and reuse.

Encapsulation is a powerful concept in OOP that promotes code reliability, security, and maintainability, and it is a key principle in designing robust and scalable software systems.

## **Abstraction:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Abstraction is a fundamental concept in object-oriented programming (OOP) that involves hiding complex implementation details while exposing only the essential features of an object. It allows us to focus on what an object does rather than how it does it. Abstraction helps in managing complexity, promoting code reuse, and enhancing maintainability. Let's explore abstraction with a scenario, example, output, and detailed description:

### Example:

```csharp
using System;

// Abstract class representing a shape
abstract class Shape
{
    // Abstract methods to be implemented by derived classes
    public abstract double CalculateArea();
    public abstract double CalculatePerimeter();
}

// Concrete class representing a circle
class Circle : Shape
{
    private double radius;

    public Circle(double radius)
    {
        this.radius = radius;
    }

    public override double CalculateArea()
    {
        return Math.PI * radius * radius;
    }

    public override double CalculatePerimeter()
    {
        return 2 * Math.PI * radius;
    }
}

// Concrete class representing a rectangle
class Rectangle : Shape
{
    private double length;
    private double width;

    public Rectangle(double length, double width)
    {
        this.length = length;
        this.width = width;
    }

    public override double CalculateArea()
    {
        return length * width;
    }

    public override double CalculatePerimeter()
    {
        return 2 * (length + width);
    }
}

class Program
{
    static void Main()
    {
        // Creating shapes
        Shape circle = new Circle(5);
        Shape rectangle = new Rectangle(4, 6);

        // Calculating area and perimeter
        Console.WriteLine("Circle - Area: " + circle.CalculateArea() + ", Perimeter: " + circle.CalculatePerimeter());
        Console.WriteLine("Rectangle - Area: " + rectangle.CalculateArea() + ", Perimeter: " + rectangle.CalculatePerimeter());
    }
}
```

### Output:

```
Circle - Area: 78.53981633974483, Perimeter: 31.41592653589793
Rectangle - Area: 24, Perimeter: 20
```

This example uses an abstract class `Shape` to represent a shape, with abstract methods `CalculateArea()` and `CalculatePerimeter()`. Concrete classes `Circle` and `Rectangle` inherit from `Shape` and provide specific implementations for these methods. The `Main` method demonstrates polymorphic behavior by treating instances of `Circle` and `Rectangle` as `Shape`. This design adheres to the principles of abstraction, as it hides the implementation details of each shape while providing a common interface for interacting with them.

### Benefits of Abstraction:

1. **Focus on Essentials**: Abstraction allows developers to focus on the essential characteristics and behaviors of objects, abstracting away unnecessary details.
2. **Flexibility and Extensibility**: By defining interfaces and abstract classes, abstraction enables flexible and extensible designs, facilitating changes and enhancements.
3. **Code Reusability**: Abstraction promotes code reusability by allowing classes to implement common interfaces and inherit from abstract classes, reducing redundancy and promoting modularity.

Abstraction is a powerful concept in OOP that enables modular, maintainable, and scalable software design. By hiding implementation details behind well-defined interfaces and abstract classes, abstraction helps in managing complexity and promoting code quality.

## **Encapsulation Vs Abstraction:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Aspect          | Encapsulation                                      | Abstraction                                        |
|-----------------|----------------------------------------------------|----------------------------------------------------|
| Definition      | Bundling of data and methods that operate on data, and restricting access to the internal state of an object. | Hiding complex implementation details and exposing only essential features of an object. |
| Purpose         | Enhances data security and integrity by hiding internal state and providing controlled access through methods. | Manages complexity by focusing on what an object does rather than how it does it, promoting code reuse and maintainability. |
| Implementation  | Achieved through access modifiers (e.g., private, protected) and properties/methods to control access to fields and methods. | Implemented using abstract classes, interfaces, and polymorphism to define common interfaces and hide implementation details. |
| Example         | Private fields and public properties/methods in a class to control access to data and behavior. | Abstract classes defining common behavior (e.g., `Shape` with `CalculateArea()` and `CalculatePerimeter()` methods) and concrete classes implementing specific behavior. |
| Key Principle   | Data Hiding                                        | Focus on Essentials                                |

**Difference:**
- **Encapsulation** focuses on bundling data and methods together and controlling access to them, while **abstraction** focuses on hiding implementation details and providing a simplified view of an object's functionality.
- Encapsulation primarily involves access control mechanisms such as access modifiers and properties/methods, while abstraction involves defining common interfaces and hiding implementation details using abstract classes and interfaces.
- Encapsulation enhances data security and integrity by restricting access to the internal state of an object, while abstraction promotes code reuse and maintainability by hiding unnecessary details and exposing only essential features.

## **Polymorphism:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Polymorphism is a fundamental concept in object-oriented programming (OOP) that allows objects of different types to be treated as objects of a common base type. It enables flexibility, extensibility, and code reusability by allowing methods to behave differently based on the object they are invoked upon. Let's explore polymorphism with a scenario, example, and output in detailed description:

### Scenario:

Consider a scenario where you are developing a software system to manage various types of animals in a zoo. Each animal makes a distinct sound, and you want to create a generic way to interact with different types of animals without knowing their specific implementations.

### Example:

```csharp
using System;

// Base class representing an animal
class Animal
{
    public virtual void MakeSound()
    {
        Console.WriteLine("The animal makes a sound.");
    }
}

// Derived class representing a dog
class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The dog barks.");
    }
}

// Derived class representing a cat
class Cat : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The cat meows.");
    }
}

// Derived class representing a bird
class Bird : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The bird chirps.");
    }
}

class Program
{
    static void Main()
    {
        // Create instances of different animals
        Animal dog = new Dog();
        Animal cat = new Cat();
        Animal bird = new Bird();

        // Invoke the MakeSound method on each animal
        dog.MakeSound();  // Output: The dog barks.
        cat.MakeSound();  // Output: The cat meows.
        bird.MakeSound(); // Output: The bird chirps.
    }
}
```

### Output:

```
The dog barks.
The cat meows.
The bird chirps.
```

### Explanation:

In this example:
- We define a base class `Animal` with a virtual method `MakeSound()` representing the common behavior of animals making sounds.
- Derived classes `Dog`, `Cat`, and `Bird` inherit from `Animal` and provide specific implementations for the `MakeSound()` method, representing the sounds made by each type of animal.
- In the `Main` method, we create instances of `Dog`, `Cat`, and `Bird`, treating them polymorphically as `Animal`.
- When invoking the `MakeSound()` method on each animal, the method behaves differently based on the actual type of the object, demonstrating polymorphic behavior.

### Benefits of Polymorphism:

1. **Flexibility**: Polymorphism allows for the development of flexible and extensible code by enabling methods to behave differently based on the object they are invoked upon.
2. **Code Reusability**: Polymorphism promotes code reusability by allowing common interfaces to be defined and implemented by multiple classes, reducing redundancy and promoting modularity.
3. **Ease of Maintenance**: Polymorphism simplifies maintenance and updates by allowing changes to be made in one place (e.g., base class or interface) and automatically reflected in all derived classes.

Polymorphism is a powerful concept in OOP that enables dynamic behavior and enhances the flexibility and maintainability of software systems. By treating objects polymorphically, developers can write code that is more expressive, adaptable, and scalable.

## **Inheritance Vs Polymorphism:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Aspect           | Inheritance                                      | Polymorphism                                      |
|------------------|--------------------------------------------------|---------------------------------------------------|
| Definition       | Mechanism where a new class inherits properties and behaviors from an existing class (base class). | Mechanism where a method can behave differently based on the object it operates on. |
| Purpose          | Promotes code reuse and establishes an "is-a" relationship between classes. | Enables dynamic behavior and flexibility by allowing methods to be invoked on objects of different types. |
| Implementation   | Achieved through class hierarchies and the use of keywords like `extends` (Java) or `:` (C#) to denote inheritance. | Implemented through method overriding and method overloading, often utilizing inheritance to establish a common base type. |
| Example          | `class Dog : Animal`                            | `virtual/abstract void MakeSound()` in base class `Animal` overridden by `void MakeSound()` in derived class `Dog`. |
| Key Principle    | "Is-a" Relationship                             | Dynamic Behavior                                  |

**Difference:**
- **Inheritance** establishes a relationship between classes where one class (derived or child class) inherits properties and behaviors from another class (base or parent class), promoting code reuse and establishing an "is-a" relationship. On the other hand, **polymorphism** allows methods to behave differently based on the object they operate on, enabling dynamic behavior and flexibility without necessarily relying on class hierarchies.

## **`this` Keyword:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, the `this` keyword is a reference to the current instance of a class, allowing you to access members of the current object within its own methods or constructors. It is primarily used to disambiguate between instance variables and parameters or local variables with the same name, and to explicitly refer to instance members when necessary. Here's a breakdown of its usage:

1. **Accessing Instance Members**: You can use `this` to access instance variables and methods of the current object within its own methods or constructors.

```csharp
class MyClass
{
    private int myNumber;

    public MyClass(int myNumber)
    {
        // Using 'this' to disambiguate between the instance variable and the parameter
        this.myNumber = myNumber;
    }

    public void DisplayNumber()
    {
        // Accessing the instance variable using 'this'
        Console.WriteLine("My number is: " + this.myNumber);
    }
}
```

2. **Chaining Constructors**: In constructors, `this` can be used to call another constructor in the same class, allowing for constructor chaining.

```csharp
class MyClass
{
    private int myNumber;

    public MyClass() : this(0) // Calls the parameterized constructor with default value
    {
        // Additional initialization logic if needed
    }

    public MyClass(int myNumber)
    {
        this.myNumber = myNumber;
    }
}
```

3. **Returning Current Instance**: You can return the current instance of the class from a method, enabling method chaining or fluent interfaces.

```csharp
class MyClass
{
    private int myNumber;

    public MyClass SetNumber(int myNumber)
    {
        this.myNumber = myNumber;
        return this; // Return the current instance for method chaining
    }
}
```

4. **Extension Methods**: In extension methods, `this` is used to indicate that the method operates on instances of the specified type.

```csharp
public static class StringExtensions
{
    public static bool IsNullOrEmpty(this string value)
    {
        return string.IsNullOrEmpty(value);
    }
}
```

5. **Current Class Methods**: This usage of the `this` keyword allows you to invoke another method within the same class. It is useful when you want to call another method of the current class, especially to reuse code or maintain a sequence of operations.

```csharp
class MyClass
{
    public void Method1()
    {
        Console.WriteLine("Method 1");
    }

    public void Method2()
    {
        // Invoking Method1 using 'this'
        this.Method1();
        Console.WriteLine("Method 2");
    }
}
```

6. **Declare an Indexer**: In C#, an indexer allows instances of a class to be accessed like arrays. By using the `this` keyword in the declaration of an indexer, you specify that instances of the class can be indexed using the `this` keyword followed by square brackets `[ ]`. This provides a convenient way to access or modify elements of the class instance, similar to arrays or collections.

```csharp
class MyClass
{
    private string[] values = new string[10];

    // Indexer using 'this' keyword
    public string this[int index]
    {
        get
        {
            return values[index];
        }
        set
        {
            values[index] = value;
        }
    }
}
class Program {
     
    // Main Method
    public static void Main()
    {
        MyClass g = new MyClass();
        g[0] = "Jan";
        g[1] = "Feb";
        g[2] = "Mar";
        g[3] = "Apr";
        g[4] = "May";
        g[5] = "Jun";
        g[6] = "Jul";
        g[7] = "Aug";
        g[8] = "Sep";
        g[9] = "Oct";
        g[10] = "Nov";
        g[11] = "Dev";
        for (int i = 0; i < 12; i++)
            Console.Write(g[i] + " ");
    }
}
```

In summary, the `this` keyword in C# is a reference to the current instance of a class, used primarily to disambiguate between instance members and local variables, enable constructor chaining, return the current instance for method chaining, and indicate extension methods.

## **Static Class vs Non-static Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Aspect              | Static Class                                      | Non-static Class                                  |
|---------------------|---------------------------------------------------|---------------------------------------------------|
| Definition          | A class that cannot be instantiated and can only contain static members (fields, methods, properties). | A class that can be instantiated to create objects, and may contain both static and instance members. |
| Instantiation       | Cannot be instantiated with the `new` keyword.    | Can be instantiated with the `new` keyword to create objects. |
| Usage               | Suitable for grouping related utility methods or constants, without the need for instance-specific data. | Suitable for modeling real-world entities or concepts, encapsulating data and behavior specific to individual instances. |
| Memory Allocation   | Memory is allocated only once for the entire application, as static members are shared across all instances and threads. | Memory is allocated separately for each instance of the class, as each instance has its own set of instance members. |
| Accessing Members   | Static members are accessed using the class name (e.g., `StaticClass.StaticMethod()`). | Instance members are accessed through object references (e.g., `objInstance.Method()`), where `objInstance` is an instance of the class. |
| Example             | `public static class MathUtils { ... }`           | `public class Person { ... }`                      |

**Difference:**
- **Static Class**: Cannot be instantiated and is primarily used to group related utility methods or constants. Memory is allocated only once for the entire application, and static members are shared across all instances and threads. Static members are accessed using the class name.
- **Non-static Class**: Can be instantiated to create objects, and may contain both static and instance members. Memory is allocated separately for each instance of the class, and instance members are accessed through object references. Non-static classes are used to model real-world entities or concepts, encapsulating data and behavior specific to individual instances.

## **Partial Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Partial classes in C# allow a class's members to be split across multiple files while appearing as a single entity to the developer. This feature is useful for organizing large classes, auto-generated code, or separating implementation details. Let's explore partial classes with scenarios, examples, and outputs:

### Scenario:

Imagine you are working on a large project with multiple developers. Each developer is responsible for implementing different aspects of a complex class. To maintain modularity and simplify collaboration, you decide to use partial classes.

### Example:

Consider a `Person` class with properties for `Name`, `Age`, and `Address`. Instead of defining all members in a single file, you can split the class across two partial class files: `Person.cs` and `PersonDetails.cs`.

#### Person.cs:

```csharp
// Person.cs
using System;

public partial class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}
```

#### PersonDetails.cs:

```csharp
// PersonDetails.cs
public partial class Person
{
    public string Address { get; set; }
}
```

#### Program.cs:

```csharp
// Program.cs
class Program
{
    static void Main()
    {
        Person person = new Person
        {
            Name = "Alice",
            Age = 30,
            Address = "123 Main St"
        };

        person.DisplayInfo();
        Console.WriteLine($"Address: {person.Address}");
    }
}
```

### Output:

```
Name: Alice, Age: 30
Address: 123 Main St
```

### Explanation:

- In this example, the `Person` class is defined as a partial class across two files: `Person.cs` and `PersonDetails.cs`.
- The properties `Name` and `Age`, along with the method `DisplayInfo()`, are defined in `Person.cs`.
- The `Address` property is defined in `PersonDetails.cs`.
- Despite being split across multiple files, the `Person` class appears as a single entity to the developer. When compiled, the compiler merges all partial class definitions into a single class definition.
- In the `Main` method of `Program.cs`, we instantiate a `Person` object and set its properties. We then call the `DisplayInfo()` method defined in `Person.cs` and access the `Address` property defined in `PersonDetails.cs`.

### Benefits:

1. **Modularity**: Partial classes allow you to organize and maintain large classes more effectively by splitting them into smaller, more manageable parts.
2. **Separation of Concerns**: You can separate auto-generated code, framework-specific code, or different aspects of functionality into separate files.
3. **Collaboration**: Different developers can work on different parts of the same class without interfering with each other's code.

Partial classes provide a flexible and convenient way to structure your codebase, especially for large projects or classes with complex implementations.

## **Shallow Copy and Deep Copy:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, when you copy an object, you can perform either a shallow copy or a deep copy, depending on your requirements. Let's explore both concepts with scenarios, examples, and outputs:

### Shallow Copy:

A shallow copy of an object creates a new object and then copies the non-static fields of the original object to the new object. If the field is a value type, a bit-by-bit copy is performed. If the field is a reference type, the reference is copied, not the actual object. As a result, both the original object and the shallow copy share references to the same child objects.

#### Scenario:

Consider a scenario where you have a `Person` class with a `Name` property of type `string` and an `Address` property of type `Address`, which is a reference type. You create a shallow copy of a `Person` object and modify the `Address` property in the copy.

#### Example:

```csharp
using System;

class Address
{
    public string Street { get; set; }
    public string City { get; set; }
}

class Person
{
    public string Name { get; set; }
    public Address Address { get; set; }
}

class Program
{
    static void Main()
    {
        Address address = new Address { Street = "123 Main St", City = "City" };
        Person originalPerson = new Person { Name = "Alice", Address = address };

        Person shallowCopyPerson = (Person)originalPerson.MemberwiseClone();
        shallowCopyPerson.Address.City = "New City";

        Console.WriteLine("Original Address: " + originalPerson.Address.City);
        Console.WriteLine("Shallow Copy Address: " + shallowCopyPerson.Address.City);
    }
}
```

#### Output:

```
Original Address: New City
Shallow Copy Address: New City
```

### Explanation:

- In this example, we have a `Person` class with a `Name` property and an `Address` property of type `Address`.
- We create an `Address` object and set its `Street` and `City` properties.
- Then, we create a `Person` object named `originalPerson` with the `Name` property set to "Alice" and the `Address` property set to the `Address` object we created.
- We create a shallow copy of the `originalPerson` object using the `MemberwiseClone()` method. This method creates a shallow copy of the object, copying the values of all non-static fields to the new object.
- We modify the `City` property of the `Address` object in the shallow copy.
- Both the original object and the shallow copy now reference the same `Address` object, so when we modify the `City` property in the shallow copy, it affects the original object as well.

### Deep Copy:

A deep copy of an object creates a new object and then recursively copies all non-static fields of the original object to the new object, including child objects. Each object and its child objects are duplicated in memory, resulting in completely independent copies.

#### Scenario:

Using the same `Person` and `Address` classes, you create a deep copy of a `Person` object and modify the `Address` property in the copy, verifying that the original object remains unchanged.

#### Example:

```csharp
using System;
using System.IO;
using System.Runtime.Serialization;
using System.Runtime.Serialization.Formatters.Binary;

[Serializable]
class Address
{
    public string Street { get; set; }
    public string City { get; set; }
}

[Serializable]
class Person
{
    public string Name { get; set; }
    public Address Address { get; set; }

    public Person DeepClone()
    {
        using (MemoryStream stream = new MemoryStream())
        {
            BinaryFormatter formatter = new BinaryFormatter();
            formatter.Serialize(stream, this);
            stream.Seek(0, SeekOrigin.Begin);
            return (Person)formatter.Deserialize(stream);
        }
    }
}

class Program
{
    static void Main()
    {
        Address address = new Address { Street = "123 Main St", City = "City" };
        Person originalPerson = new Person { Name = "Alice", Address = address };

        Person deepCopyPerson = originalPerson.DeepClone();
        deepCopyPerson.Address.City = "New City";

        Console.WriteLine("Original Address: " + originalPerson.Address.City);
        Console.WriteLine("Deep Copy Address: " + deepCopyPerson.Address.City);
    }
}
```

#### Output:

```
Original Address: City
Deep Copy Address: New City
```

### Explanation:

- In this example, the `Address` and `Person` classes are marked as `[Serializable]` to enable binary serialization.
- The `Person` class includes a `DeepClone()` method, which performs a deep copy of the object using binary serialization. This method serializes the object to a memory stream and then deserializes it, creating a new copy in memory.
- We create an `originalPerson` object and set its `Address` property to an `Address` object.
- We create a deep copy of the `originalPerson` object using the `DeepClone()` method.
- We modify the `City` property of the `Address` object in the deep copy, verifying that the change does not affect the original object.

### Summary:

- Shallow copy creates a new object and copies the values of all non-static fields, including references to child objects. Changes to child objects affect both the original and shallow copy.
- Deep copy creates a new object and recursively copies all non-static fields, including child objects. Each object and its child objects are duplicated in memory, resulting in completely independent copies.

Here's a comparison of shallow and deep copy in tabular format:

| Aspect          | Shallow Copy                                                  | Deep Copy                                                     |
|-----------------|---------------------------------------------------------------|---------------------------------------------------------------|
| Definition      | Copies the object and its non-static fields, including references to child objects. | Recursively copies the object and all its non-static fields, including child objects, creating independent copies. |
| Child Objects  | References to child objects are shared between the original and the copy. | Each object and its child objects are duplicated in memory, resulting in independent copies. |
| Memory Usage    | Consumes less memory since it shares references to child objects. | Consumes more memory since it duplicates each object and its child objects. |
| Modifications   | Changes to child objects affect both the original and the copy. | Changes to child objects do not affect the original object or other copies. |
| Implementation  | Usually performed using `MemberwiseClone()` method or manual copying of fields. | Often implemented using serialization and deserialization to create a completely independent copy. |

## **Inheritance in Interface:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, interfaces can inherit from one or more other interfaces, allowing them to inherit members (methods, properties, events, and indexers) from those interfaces. This concept is known as "inheritance in interfaces" or "interface inheritance."

### Example:

Let's create an example to demonstrate inheritance in interfaces:

```csharp
using System;

// Base interface
public interface IShape
{
    void Draw();
}

// Derived interface inheriting from IShape
public interface ICircle : IShape
{
    double Radius { get; set; }
}

// Concrete class implementing ICircle
public class Circle : ICircle
{
    public double Radius { get; set; }

    public void Draw()
    {
        Console.WriteLine($"Drawing a circle with radius {Radius}");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of Circle
        Circle circle = new Circle { Radius = 5 };

        // Call the Draw method of Circle
        circle.Draw();
    }
}
```

### Output:

```
Drawing a circle with radius 5
```

### Explanation:

- We define a base interface `IShape` with a single method `Draw`.
- We define a derived interface `ICircle` that inherits from `IShape` and adds a property `Radius`.
- We create a concrete class `Circle` that implements the `ICircle` interface. It provides implementations for both `Draw` and `Radius`.
- In the `Main` method, we create an instance of `Circle` and set its radius to 5.
- We call the `Draw` method on the `Circle` instance, which prints a message indicating that a circle with a radius of 5 is being drawn.

### Summary:

- Inheritance in interfaces allows one interface to inherit members from another interface.
- A derived interface inherits all the members (methods, properties, events, and indexers) from its base interfaces.
- Classes implementing the derived interface must provide implementations for all inherited members from both the derived interface and its base interfaces.
- Inheritance in interfaces promotes code reusability and supports the design of modular and extensible systems. It enables the creation of hierarchies of related interfaces with shared functionality.

## **Inheritance in Constructors:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Inheritance in constructors refers to how constructors are inherited and invoked in a class hierarchy. When you create a subclass (derived class) that inherits from a base class, the constructors of the base class are also inherited. The derived class can choose to use one of the available constructors from the base class or define its own constructors.

### Example:

Let's create an example to demonstrate inheritance in constructors:

```csharp
using System;

// Base class
public class Animal
{
    public string Name { get; set; }

    // Base class constructor
    public Animal(string name)
    {
        Name = name;
        Console.WriteLine("Animal constructor invoked.");
    }

    // Method to display information about the animal
    public void Display()
    {
        Console.WriteLine($"Name: {Name}");
    }
}

// Derived class inheriting from Animal
public class Dog : Animal
{
    public Dog(string name) : base(name)
    {
        Console.WriteLine("Dog constructor invoked.");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of Dog
        Dog dog = new Dog("Buddy");

        // Call the Display method of Dog
        dog.Display();
    }
}
```

### Output:

```
Animal constructor invoked.
Dog constructor invoked.
Name: Buddy
```

### Explanation:

- We define a base class `Animal` with a constructor that takes a `name` parameter and sets the `Name` property.
- The derived class `Dog` inherits from `Animal` and defines its own constructor that calls the base class constructor using the `base` keyword.
- In the `Main` method, we create an instance of `Dog` with the name "Buddy."
- When the `Dog` constructor is invoked, it first invokes the `Animal` constructor to initialize the `Name` property. Then, it executes its own constructor code.
- Finally, we call the `Display` method of `Dog` to display information about the created dog.

### Summary:

- Inheritance in constructors allows derived classes to inherit and use constructors from their base classes.
- Derived class constructors can choose to invoke one of the available constructors from the base class using the `base` keyword.
- When a derived class constructor is invoked, it first invokes the constructor of its base class to initialize inherited members before executing its own constructor code.
- Constructors in the base class can be parameterized or default constructors, and the derived class can choose which one to use or override.

## **Abstract Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

An abstract class in C# is a class that cannot be instantiated directly and may contain one or more abstract members, such as methods, properties, or events. It serves as a blueprint for derived classes, providing common functionality and defining the structure of the class hierarchy. Abstract classes are typically used when you want to define a common interface or behavior that must be implemented by subclasses.

### Example:

Let's create an example to demonstrate an abstract class:

```csharp
using System;

// Abstract class
public abstract class Shape
{
    // Abstract method
    public abstract double Area();

    // Concrete method
    public void DisplayArea()
    {
        Console.WriteLine($"Area: {Area()}");
    }
}

// Concrete class inheriting from Shape
public class Rectangle : Shape
{
    public double Width { get; set; }
    public double Height { get; set; }

    // Implementing the abstract method
    public override double Area()
    {
        return Width * Height;
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of Rectangle
        Rectangle rectangle = new Rectangle { Width = 5, Height = 4 };

        // Call the DisplayArea method
        rectangle.DisplayArea();
    }
}
```

### Output:

```
Area: 20
```

### Explanation:

- We define an abstract class `Shape` with an abstract method `Area()` and a concrete method `DisplayArea()`.
- The `Shape` class cannot be instantiated directly because it contains an abstract method.
- We define a concrete class `Rectangle` that inherits from `Shape` and implements the `Area()` method by providing its own implementation.
- In the `Main` method, we create an instance of `Rectangle` and set its width and height.
- We call the `DisplayArea` method on the `Rectangle` instance, which internally calls the overridden `Area()` method to calculate the area of the rectangle and display it.

### Features of Abstract Classes:

1. **Abstract Methods**: Abstract classes can contain one or more abstract methods, which are declared without an implementation and must be implemented by derived classes.

2. **Concrete Methods**: Abstract classes can also contain concrete (non-abstract) methods with an implementation, which are inherited by derived classes.

3. **Cannot Be Instantiated**: Abstract classes cannot be instantiated directly. They serve as a template for derived classes and must be subclassed to be used.

4. **May Contain Fields and Properties**: Abstract classes can contain fields, properties, constructors, and other members just like regular classes.

5. **Can Have Constructors**: Abstract classes can have constructors, which are used to initialize fields and perform common initialization tasks.

6. **Can Have Access Modifiers**: Abstract classes can have access modifiers like `public`, `protected`, `internal`, etc., controlling their accessibility to other classes.

7. **Supports Inheritance**: Abstract classes support inheritance, allowing derived classes to extend their functionality and provide implementations for abstract members.

Abstract classes provide a powerful mechanism for defining common behavior and structure in a class hierarchy, promoting code reuse and maintainability in object-oriented programming.

## **Interface in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

An interface in C# defines a contract that classes must adhere to, specifying a set of methods, properties, events, or indexers that implementing classes must provide. Interfaces enable polymorphism by allowing different classes to share common behavior without requiring a common base class. Classes implement interfaces by providing concrete implementations for all members defined in the interface.

### Example:

Let's create an example to demonstrate interfaces in C#:

```csharp
using System;

// Interface definition
public interface IShape
{
    // Method declaration
    double Area();
}

// Class implementing the interface
public class Circle : IShape
{
    public double Radius { get; set; }

    // Implementing the Area method defined in the interface
    public double Area()
    {
        return Math.PI * Radius * Radius;
    }
}

// Class implementing the interface
public class Rectangle : IShape
{
    public double Width { get; set; }
    public double Height { get; set; }

    // Implementing the Area method defined in the interface
    public double Area()
    {
        return Width * Height;
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create instances of classes implementing the interface
        Circle circle = new Circle { Radius = 5 };
        Rectangle rectangle = new Rectangle { Width = 4, Height = 6 };

        // Call the Area method of each object
        Console.WriteLine($"Area of Circle: {circle.Area()}");
        Console.WriteLine($"Area of Rectangle: {rectangle.Area()}");
    }
}
```

### Output:

```
Area of Circle: 78.53981633974483
Area of Rectangle: 24
```

### Explanation:

- We define an interface `IShape` with a method `Area()` that calculates the area of a shape.
- We define two classes `Circle` and `Rectangle` that implement the `IShape` interface by providing concrete implementations for the `Area()` method.
- In the `Main` method, we create instances of the `Circle` and `Rectangle` classes and call the `Area()` method on each object.
- Each class calculates the area based on its specific properties (`Radius` for `Circle` and `Width` and `Height` for `Rectangle`).

### Summary:

- Interfaces in C# define a contract that classes must adhere to by providing concrete implementations for all members defined in the interface.
- Interfaces enable polymorphism by allowing different classes to share common behavior without requiring a common base class.
- Classes implement interfaces by providing concrete implementations for all members defined in the interface, enabling code reuse and promoting a loosely coupled design.

## **Why do we use interface in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Interfaces in C# are used to define contracts that classes must adhere to, enabling polymorphism and promoting a loosely coupled design. They provide a way to share common behavior among different classes without requiring a common base class. Let's explore a problem scenario and its solution using interfaces:

### Problem Scenario:

Suppose we have a program that needs to calculate the total area of various shapes, such as circles, rectangles, and triangles. Each shape has a different formula for calculating its area, and we want to design our program to be flexible and extensible, allowing us to easily add new shapes in the future.

### Solution using Interfaces:

We can use interfaces to define a common contract for all shapes, specifying a method for calculating the area. Each shape class will then implement this interface by providing its own implementation of the area calculation method.

### Example:

Let's create an example to demonstrate how interfaces can solve this problem:

```csharp
using System;

// Interface definition
public interface IShape
{
    double Area();
}

// Circle class implementing the IShape interface
public class Circle : IShape
{
    public double Radius { get; set; }

    public Circle(double radius)
    {
        Radius = radius;
    }

    // Implementing the Area method defined in the interface
    public double Area()
    {
        return Math.PI * Radius * Radius;
    }
}

// Rectangle class implementing the IShape interface
public class Rectangle : IShape
{
    public double Width { get; set; }
    public double Height { get; set; }

    public Rectangle(double width, double height)
    {
        Width = width;
        Height = height;
    }

    // Implementing the Area method defined in the interface
    public double Area()
    {
        return Width * Height;
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create instances of different shapes
        Circle circle = new Circle(5);
        Rectangle rectangle = new Rectangle(4, 6);

        // Calculate and display the total area
        double totalArea = CalculateTotalArea(circle, rectangle);
        Console.WriteLine($"Total Area: {totalArea}");
    }

    // Method to calculate total area of shapes using interface
    static double CalculateTotalArea(params IShape[] shapes)
    {
        double totalArea = 0;
        foreach (var shape in shapes)
        {
            totalArea += shape.Area();
        }
        return totalArea;
    }
}
```

### Explanation:

- We define an interface `IShape` with a method `Area()` to calculate the area of a shape.
- The `Circle` and `Rectangle` classes implement the `IShape` interface by providing their own implementations of the `Area()` method.
- In the `Main` method, we create instances of `Circle` and `Rectangle` and calculate their individual areas.
- We then call the `CalculateTotalArea` method, passing the instances of shapes as arguments. This method calculates the total area of all shapes by invoking the `Area()` method for each shape.

### Benefits:

1. **Flexibility**: Interfaces allow us to define a common contract for different classes, enabling flexibility in the design and promoting code reuse.

2. **Polymorphism**: Interface implementations enable polymorphic behavior, allowing objects of different classes to be treated interchangeably based on the common interface they implement.

3. **Extensibility**: Interfaces facilitate easy addition of new shapes or classes without modifying existing code, making the system more extensible and maintainable.

By using interfaces, we can solve the problem of calculating the total area of different shapes in a flexible, polymorphic, and extensible manner, enabling better code organization and maintainability.


## **Abstract Class Vs Interface:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Below is a detailed comparison of abstract classes and interfaces in C# presented in a tabular form:

| Feature                      | Abstract Class                                     | Interface                                          |
|------------------------------|----------------------------------------------------|----------------------------------------------------|
| Definition                   | Can have both abstract and concrete members.       | Can only have abstract members (methods, properties, events, indexers). |
| Multiple Inheritance         | Cannot inherit from multiple abstract classes.     | Can inherit from multiple interfaces.               |
| Constructor                  | Can have constructors.                             | Cannot have constructors.                           |
| Accessibility                | Can have access modifiers like `public`, `protected`, `internal`, etc. | By default, all members are `public`.             |
| Default Implementation       | Can provide default implementations for some methods. | Cannot provide default implementations.            |
| Fields and Properties        | Can have fields, properties, and other members.    | Cannot have fields, properties, or other members.  |
| Extensibility                | Supports extension methods and properties.         | Cannot add additional functionality beyond what's defined in the interface. |
| Code Reuse                   | Promotes code reuse through inheritance.           | Promotes code reuse through interface implementation. |
| Flexibility                  | Provides more flexibility in terms of implementation details and structure. | Provides more flexibility in terms of multiple interface implementation. |
| Use Case                     | Used when you want to define a common base for a group of related classes with shared functionality. | Used when you want to define a contract that classes must adhere to, regardless of their inheritance hierarchy. |

### Summary:

- **Abstract Class**: Used when you want to define a common base for a group of related classes with shared functionality. It can have both abstract and concrete members, constructors, access modifiers, and can provide default implementations for some methods. Supports inheritance but not multiple inheritance.
  
- **Interface**: Used when you want to define a contract that classes must adhere to, regardless of their inheritance hierarchy. It can only have abstract members, cannot contain implementation details, constructors, or fields. Supports multiple inheritance by allowing a class to implement multiple interfaces.


## **Sealed Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

A sealed class in C# is a class that cannot be inherited by other classes. It prevents other classes from deriving from it, effectively sealing its functionality and preventing extension. Sealing a class can be useful when you want to restrict inheritance and ensure that the class behavior remains unchanged.

### Example:

Let's create an example to demonstrate a sealed class in C#:

```csharp
using System;

// Sealed class definition
public sealed class SealedClass
{
    public void Display()
    {
        Console.WriteLine("This is a sealed class.");
    }
}

// This class cannot inherit from SealedClass because it is sealed
// public class DerivedClass : SealedClass {}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of SealedClass
        SealedClass sealedObj = new SealedClass();

        // Call the Display method
        sealedObj.Display();
    }
}
```

### Output:

```
This is a sealed class.
```

### Explanation:

- We define a `SealedClass` as `sealed`, which means it cannot be inherited by other classes.
- The `Display` method is defined within the sealed class to demonstrate its functionality.
- Attempting to derive a class from `SealedClass`, as shown in the commented code, will result in a compilation error because the class is sealed.
- In the `Main` method, we create an instance of `SealedClass` and call its `Display` method to demonstrate its behavior.

### Benefits of Sealed Classes:

1. **Prevent Modification**: Sealing a class prevents other classes from modifying or extending its behavior, ensuring that the class remains unchanged and stable.

2. **Security**: Sealing a class can enhance security by preventing unauthorized modifications to its behavior, reducing the risk of introducing bugs or vulnerabilities.

3. **Performance**: Sealed classes can potentially improve performance by allowing the compiler to optimize method calls and object creation.

### Rules:

1. **Sealed Class Declaration**: A class is marked as sealed by using the `sealed` keyword in its declaration. It prevents other classes from inheriting from it.

   ```csharp
   public sealed class SealedClass
   {
       // Class members...
   }
   ```

2. **No Inheritance**: A sealed class cannot be used as a base class for other classes. Any attempt to derive a class from a sealed class will result in a compilation error.

   ```csharp
   // Error: 'DerivedClass' cannot derive from sealed type 'SealedClass'
   public class DerivedClass : SealedClass {}
   ```

3. **Cannot Be Abstract**: A sealed class cannot be abstract because it cannot be inherited. It must provide concrete implementations for all its members.

   ```csharp
   // Error: Sealed class 'SealedClass' cannot have abstract members
   public sealed class SealedClass
   {
       public abstract void Method(); // Compilation error
   }
   ```

4. **Complete Implementation**: A sealed class must provide implementations for all its members, including methods, properties, events, and indexers.

   ```csharp
   public sealed class SealedClass
   {
       public void Method() { /* Implementation */ }
       public int Property { get; set; }
       // Other members...
   }
   ```

5. **No Derivation Chains**: Even if a class derives from a non-sealed class that eventually derives from a sealed class, it cannot inherit from the sealed class directly.

   ```csharp
   // Error: 'DerivedClass' cannot derive from sealed type 'IntermediateClass'
   public class IntermediateClass : SealedClass {}
   public class DerivedClass : IntermediateClass {}
   ```

6. **Can Implement Interfaces**: Sealed classes can implement interfaces as usual. They can provide their own implementations for the interface members.

   ```csharp
   public sealed class SealedClass : IInterface
   {
       public void Method() { /* Implementation */ }
       // Other interface members...
   }
   ```

Remember, sealing a class should be done when you are sure that no other class should derive from it. It promotes code stability, security, and maintainability by preventing unwanted inheritance and extension.

### Summary:

- Sealed classes in C# are classes that cannot be inherited by other classes.
- They are marked with the `sealed` keyword in their class definition.
- Sealing a class prevents modification and extension of its behavior, promoting stability and security.
- Sealed classes are useful when you want to restrict inheritance and ensure that a class's behavior remains unchanged.


## **Delegates vs Interfaces in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Feature           | Delegates                                 | Interfaces                                   |
|-------------------|-------------------------------------------|----------------------------------------------|
| Definition        | A delegate is a type that represents references to methods with a specific signature. | An interface is a reference type that defines a contract for the behavior of a class but does not provide any implementation. |
| Usage             | Delegates are used to encapsulate methods and treat them as objects, allowing for method invocation via delegate instances. | Interfaces are used to define a contract that classes must adhere to by implementing the members defined in the interface. |
| Single Implementation | A delegate can reference a single method with a specific signature. | An interface can be implemented by multiple classes, each providing its own implementation for the interface members. |
| Flexibility       | Delegates offer flexibility in method invocation, allowing for dynamic method invocation and callback mechanisms. | Interfaces provide a way to achieve polymorphism, enabling objects of different types to be treated interchangeably if they implement the same interface. |

In this comparison:

- **Delegates** are suitable for scenarios where you need to encapsulate methods and invoke them dynamically, such as event handling or callback mechanisms.
- **Interfaces** are useful when you want to define a contract that multiple classes can implement, enabling polymorphism and interchangeability among objects of different types.

In the provided scenarios, delegates are used to handle events in a UI component, while interfaces are employed to ensure consistent behavior across different classes representing shapes.

**Scenario using Delegates:**

Imagine you're developing a user interface (UI) application, and you need to implement a button component. When the button is clicked, you want to trigger an event to perform some action, such as displaying a message or updating UI elements.

Here's how you can use delegates to handle the button click event:

```csharp
using System;

// Delegate definition for event handler
public delegate void EventHandler();

// Button class with click event
class Button
{
    public event EventHandler Click; // Event declaration

    // Method to simulate button click
    public void SimulateClick()
    {
        // Invoke the click event if it's not null
        Click?.Invoke();
    }
}

class Program
{
    static void Main(string[] args)
    {
        Button button = new Button();

        // Subscribe to the button click event
        button.Click += () => Console.WriteLine("Button clicked!");

        // Simulate button click
        button.SimulateClick();
    }
}
```

**Output:**
```
Button clicked!
```

In this scenario, the `Button` class encapsulates the click event using a delegate (`EventHandler`). When the `SimulateClick` method is called, it triggers the click event, and any subscribed event handlers (in this case, the lambda expression printing "Button clicked!") are invoked.

---
**Scenario using Interfaces:**

Suppose you're working on a graphics application where you need to calculate the area of various shapes (e.g., circles, rectangles, triangles). To ensure consistency and ease of use, you decide to define an interface named `IShape` that all shape classes must implement.

Here's how you can use interfaces to calculate the area of different shapes:

```csharp
using System;

// Interface for shapes
public interface IShape
{
    double CalculateArea();
}

// Circle class implementing IShape
public class Circle : IShape
{
    private double radius;

    public Circle(double radius)
    {
        this.radius = radius;
    }

    // Calculate area of circle
    public double CalculateArea()
    {
        return Math.PI * radius * radius;
    }
}

// Rectangle class implementing IShape
public class Rectangle : IShape
{
    private double width;
    private double height;

    public Rectangle(double width, double height)
    {
        this.width = width;
        this.height = height;
    }

    // Calculate area of rectangle
    public double CalculateArea()
    {
        return width * height;
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create instances of Circle and Rectangle
        IShape circle = new Circle(5);
        IShape rectangle = new Rectangle(4, 6);

        // Calculate and display areas
        Console.WriteLine("Area of circle: " + circle.CalculateArea());
        Console.WriteLine("Area of rectangle: " + rectangle.CalculateArea());
    }
}
```

**Output:**
```
Area of circle: 78.53981633974483
Area of rectangle: 24
```

In this scenario, the `IShape` interface defines a contract with a single method `CalculateArea()`. Both the `Circle` and `Rectangle` classes implement this interface and provide their respective implementations of the method. This allows for consistent usage and calculation of areas for different shapes.

## **Explicit Interface:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Explicit interface implementation in C# allows a class to implement interface members in a way that those members are only accessible through an interface reference, not through the class itself. This technique is useful when a class implements multiple interfaces with members that have the same name but different implementations.

### Example:

Let's consider a scenario where we have two interfaces, `IA` and `IB`, both containing a method named `Method()`. We'll implement these interfaces explicitly in a class `Example`.

```csharp
using System;

interface IA
{
    void Method();
}

interface IB
{
    void Method();
}

class Example : IA, IB
{
    // Explicitly implement IA.Method
    void IA.Method()
    {
        Console.WriteLine("IA.Method() implementation");
    }

    // Explicitly implement IB.Method
    void IB.Method()
    {
        Console.WriteLine("IB.Method() implementation");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Example example = new Example();

        // Access IA.Method through IA interface reference
        IA ia = example;
        ia.Method(); // Output: IA.Method() implementation

        // Access IB.Method through IB interface reference
        IB ib = example;
        ib.Method(); // Output: IB.Method() implementation
    }
}
```

### Output:

```
IA.Method() implementation
IB.Method() implementation
```

In this example:

- The `Example` class implements both `IA` and `IB` interfaces.
- The `Method()` member of both interfaces is implemented explicitly in the `Example` class.
- To access these members, we need to use interface references.
- When `IA` interface reference is used, it invokes the `IA.Method()` implementation.
- When `IB` interface reference is used, it invokes the `IB.Method()` implementation.

### Summary:

Explicit interface implementation is used:
- When a class implements multiple interfaces with members that have the same name but different implementations.
- To disambiguate between interface members and provide specialized implementations for each interface.
- To hide interface members from the class's public API, making them accessible only through interface references.