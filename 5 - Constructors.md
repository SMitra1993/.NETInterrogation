# Constructors ❤🍕

**Links:**

- [Constructors in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-in-c-)
    - [Default Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#default-constructor-)
    - [Parameterized Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#parameterized-constructor-)
    - [Copy Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#copy-constructor-)
    - [Private Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#private-constructor-)
    - [Static Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#static-constructor-)
- [Default Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#default-constructor--1)
- [Copy Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#copy-constructor--1)
- [Private Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#private-constructor--1)
- [Parameterized Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#parameterized-constructor--1)
- [Static Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#static-constructor--1)
- [Static Constructor Vs Non-Static Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#static-constructor-vs-non-static-constructor-)
- [Constructor Overloading](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructor-overloading-)
- [Overloaded Constructor using “this” keyword](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#overloaded-constructor-using-this-keyword-)
- [Overloaded Constructor using Copy Constructor](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#overloaded-constructor-using-copy-constructor-)
- [Destructors in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#destructors-in-c-)

## **Constructors in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

In C#, constructors are special member methods used to initialize objects of a class. They are called automatically when an instance of the class is created and are responsible for initializing the object's state.

### Key Characteristics of Constructors:

1. **Same Name as Class**: Constructors have the same name as the class they belong to.

2. **No Return Type**: Constructors do not have a return type, not even `void`.

3. **Automatic Invocation**: Constructors are automatically invoked when an object of the class is created using the `new` keyword.

4. **Initialization**: Constructors are primarily used to initialize the object's state, such as initializing fields, properties, or other resources.

```csharp
using System;

class Car
{
    public string Make;
    public string Model;
    public int Year;

    // Default Constructor
    public Car()
    {
        Make = "Unknown";
        Model = "Unknown";
        Year = 0;
    }

    // Parameterized Constructor
    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }

    // Static Constructor
    static Car()
    {
        Console.WriteLine("Static constructor invoked.");
    }
}

class Program
{
    static void Main()
    {
        // Creating objects using different constructors
        Car car1 = new Car(); // Default Constructor
        Car car2 = new Car("Toyota", "Camry", 2020); // Parameterized Constructor

        // Accessing object properties
        Console.WriteLine($"Car 1: {car1.Year} {car1.Make} {car1.Model}");
        Console.WriteLine($"Car 2: {car2.Year} {car2.Make} {car2.Model}");
    }
}
```

**Output**

```
Static constructor invoked.
Car 1: 0 Unknown Unknown
Car 2: 2020 Toyota Camry
```

Here's the explanation:

1. When the program starts executing, the static constructor of the `Car` class is invoked. This happens before any static member of the class is accessed. Therefore, the message "Static constructor invoked." is printed to the console.

2. Two objects of the `Car` class are created using different constructors:
   - `car1` is created using the default constructor, so its properties (`Make`, `Model`, and `Year`) are initialized to their default values.
   - `car2` is created using the parameterized constructor with specific values for the `make`, `model`, and `year` parameters.

3. Finally, the properties of both `car1` and `car2` objects are accessed and printed to the console, showing their respective values.

So, the output reflects the initialization and usage of objects created with different constructors.

### Default Constructor: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A default constructor is a constructor with no parameters. If no constructor is defined in a class, a default constructor is provided by the compiler. It initializes the object's fields to their default values.

**Example:**

```csharp
using System;

class Car
{
    public string Make;
    public string Model;
    public int Year;

    // Default Constructor
    public Car()
    {
        Make = "Unknown";
        Model = "Unknown";
        Year = 0;
    }
}

class Program
{
    static void Main()
    {
        // Creating an object using the default constructor
        Car car = new Car();

        // Accessing object properties
        Console.WriteLine($"Car: {car.Year} {car.Make} {car.Model}");
    }
}
```

**Output:**
```
Car: 0 Unknown Unknown
```

### Parameterized Constructor: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A parameterized constructor is a constructor with one or more parameters. It allows you to initialize object properties with specific values at the time of object creation.

**Example:**

```csharp
using System;

class Car
{
    public string Make;
    public string Model;
    public int Year;

    // Parameterized Constructor
    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }
}

class Program
{
    static void Main()
    {
        // Creating an object using the parameterized constructor
        Car car = new Car("Toyota", "Camry", 2020);

        // Accessing object properties
        Console.WriteLine($"Car: {car.Year} {car.Make} {car.Model}");
    }
}
```

**Output:**
```
Car: 2020 Toyota Camry
```

### Copy Constructor: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

In C#, there is no direct support for copy constructors like in some other languages. However, you can create a copy constructor by defining a constructor that takes an instance of the same class as a parameter and copies its state.

**Example:**

```csharp
using System;

class Car
{
    public string Make;
    public string Model;
    public int Year;

    // Copy Constructor
    public Car(Car other)
    {
        Make = other.Make;
        Model = other.Model;
        Year = other.Year;
    }
}

class Program
{
    static void Main()
    {
        // Creating an object using the parameterized constructor
        Car originalCar = new Car("Toyota", "Camry", 2020);

        // Creating a copy of the original car
        Car copiedCar = new Car(originalCar);

        // Accessing object properties
        Console.WriteLine($"Original Car: {originalCar.Year} {originalCar.Make} {originalCar.Model}");
        Console.WriteLine($"Copied Car: {copiedCar.Year} {copiedCar.Make} {copiedCar.Model}");
    }
}
```

**Output:**
```
Original Car: 2020 Toyota Camry
Copied Car: 2020 Toyota Camry
```

### Private Constructor: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A private constructor is a constructor with a private access modifier. It is used to prevent the instantiation of a class from outside the class itself. Private constructors are often used in singleton design patterns.

**Example:**

```csharp
using System;

class Singleton
{
    private static Singleton instance;

    // Private Constructor
    private Singleton()
    {
        Console.WriteLine("Singleton instance created.");
    }

    // Static Method to Get Instance
    public static Singleton GetInstance()
    {
        if (instance == null)
        {
            instance = new Singleton();
        }
        return instance;
    }
}

class Program
{
    static void Main()
    {
        // Attempting to create an instance using the new keyword will result in a compile-time error
        // Singleton singleton = new Singleton();

        // Creating an instance using the static method
        Singleton singleton = Singleton.GetInstance();
    }
}
```

**Output:**
```
Singleton instance created.
```

### Static Constructor: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A static constructor is a special type of constructor used to initialize static members of a class. It is called automatically before any static member of the class is accessed for the first time.

**Example:**

```csharp
using System;

class MyClass
{
    public static int Count;

    // Static Constructor
    static MyClass()
    {
        Count = 0;
        Console.WriteLine("Static constructor invoked.");
    }
}

class Program
{
    static void Main()
    {
        // Accessing a static member triggers the static constructor
        Console.WriteLine($"Count: {MyClass.Count}");
    }
}
```

**Output:**
```
Static constructor invoked.
Count: 0
```

In summary, constructors play a vital role in initializing object state in C#. By understanding the different types of constructors and their usage, you can effectively manage object initialization and ensure proper behavior in your applications.

## **Default Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A default constructor is a constructor in a class that takes no parameters. If a class does not have any constructors explicitly defined, the C# compiler automatically provides a default constructor with no parameters. Default constructors are responsible for initializing the object's state to default values.

### Scenario:

Consider a scenario where you have a `Person` class that represents individuals. Each `Person` object should have default values for properties like name, age, and gender when created.

### Example:

```csharp
using System;

class Person
{
    public string Name;
    public int Age;
    public string Gender;

    // Default Constructor
    public Person()
    {
        // Initialize default values
        Name = "Unknown";
        Age = 0;
        Gender = "Unknown";
    }
}

class Program
{
    static void Main()
    {
        // Creating a Person object using the default constructor
        Person person = new Person();

        // Accessing object properties
        Console.WriteLine($"Name: {person.Name}");
        Console.WriteLine($"Age: {person.Age}");
        Console.WriteLine($"Gender: {person.Gender}");
    }
}
```

### Output:

```
Name: Unknown
Age: 0
Gender: Unknown
```

### Explanation:

In this example:
- The `Person` class defines a default constructor with no parameters.
- Inside the default constructor, the properties `Name`, `Age`, and `Gender` are initialized to default values: "Unknown" for `Name` and `Gender`, and 0 for `Age`.
- In the `Main` method, a `Person` object `person` is created using the default constructor.
- The properties of the `person` object are accessed and printed to the console, showing their default values.

This demonstrates how a default constructor is used to initialize object properties to default values when an object is created without specifying any values explicitly. Default constructors are useful for ensuring that objects have valid initial states even when no specific initialization logic is provided.

## **Copy Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A copy constructor is a constructor that creates a new object by copying the state of an existing object of the same class. It allows you to create a new object with the same values as an existing object, providing a convenient way to clone objects.

### Scenario:

Consider a scenario where you have a `Point` class representing a point in a two-dimensional coordinate system. You want to create a copy of an existing `Point` object.

### Example:

```csharp
using System;

class Point
{
    public int X;
    public int Y;

    // Copy Constructor
    public Point(Point other)
    {
        // Copy the state of the other object
        X = other.X;
        Y = other.Y;
    }
}

class Program
{
    static void Main()
    {
        // Creating an original Point object
        Point originalPoint = new Point();
        originalPoint.X = 10;
        originalPoint.Y = 20;

        // Creating a copy of the original Point object using the copy constructor
        Point copiedPoint = new Point(originalPoint);

        // Displaying the properties of both original and copied points
        Console.WriteLine("Original Point:");
        Console.WriteLine($"X: {originalPoint.X}, Y: {originalPoint.Y}");

        Console.WriteLine("\nCopied Point:");
        Console.WriteLine($"X: {copiedPoint.X}, Y: {copiedPoint.Y}");
    }
}
```

### Output:

```
Original Point:
X: 10, Y: 20

Copied Point:
X: 10, Y: 20
```

### Explanation:

In this example:
- The `Point` class defines a copy constructor that takes another `Point` object as its parameter.
- Inside the copy constructor, the properties `X` and `Y` of the current object are assigned the values of the corresponding properties of the other object.
- In the `Main` method, an original `Point` object `originalPoint` is created with coordinates (10, 20).
- Then, a copy of the original `Point` object is created using the copy constructor, passing the `originalPoint` object as a parameter.
- Both the original and copied `Point` objects have the same values for their `X` and `Y` properties, demonstrating that the copy constructor successfully created a new object with the same state as the original object.

This demonstrates how a copy constructor can be used to create a new object by copying the state of an existing object, providing a convenient way to clone objects in C#.

## **Private Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A private constructor is a constructor with a private access modifier, meaning it can only be accessed from within the same class. Private constructors are typically used to prevent the instantiation of a class from outside the class itself. They are commonly used in scenarios such as implementing the singleton pattern, where only one instance of a class should exist.

### Scenario:

Consider a scenario where you have a `Singleton` class that should only have one instance throughout the lifetime of the application. You want to ensure that no other instances of the class can be created from outside the class itself.

### Example:

```csharp
using System;

class Singleton
{
    private static Singleton instance;

    // Private Constructor
    private Singleton()
    {
        Console.WriteLine("Singleton instance created.");
    }

    // Static Method to Get Instance
    public static Singleton GetInstance()
    {
        if (instance == null)
        {
            instance = new Singleton();
        }
        return instance;
    }
}

class Program
{
    static void Main()
    {
        // Attempting to create an instance using the new keyword will result in a compile-time error
        // Singleton singleton = new Singleton();

        // Creating an instance using the static method
        Singleton singleton = Singleton.GetInstance();
    }
}
```

### Output:

```
Singleton instance created.
```

### Explanation:

In this example:
- The `Singleton` class defines a private constructor, which means it cannot be accessed from outside the class itself.
- The `GetInstance` static method provides a way to access the singleton instance. It checks if the instance already exists; if not, it creates a new instance using the private constructor.
- In the `Main` method, an attempt to create an instance of the `Singleton` class using the `new` keyword results in a compile-time error because the constructor is private.
- Instead, the `GetInstance` method is called to obtain the singleton instance, which successfully creates a single instance of the `Singleton` class.

This demonstrates how a private constructor can be used to control the instantiation of a class and enforce certain design patterns such as the singleton pattern in C#. Only the class itself can create instances of itself, ensuring that the desired behavior is maintained throughout the application.

## **Parameterized Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A parameterized constructor in C# is a constructor with one or more parameters. It allows you to initialize object properties with specific values at the time of object creation. Parameterized constructors provide flexibility by allowing you to create objects with different initial states based on the provided parameters.

### Scenario:

Imagine you have a `Car` class that represents vehicles, and you want to create instances of `Car` objects with specific make, model, and year values.

### Example:

```csharp
using System;

class Car
{
    public string Make;
    public string Model;
    public int Year;

    // Parameterized Constructor
    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }
}

class Program
{
    static void Main()
    {
        // Creating a Car object using the parameterized constructor
        Car car = new Car("Toyota", "Camry", 2020);

        // Accessing object properties
        Console.WriteLine($"Car: {car.Year} {car.Make} {car.Model}");
    }
}
```

### Output:

```
Car: 2020 Toyota Camry
```

### Explanation:

In this example:
- The `Car` class defines a parameterized constructor that takes three parameters: `make`, `model`, and `year`.
- Inside the constructor, the properties `Make`, `Model`, and `Year` of the `Car` object are initialized with the values provided as parameters.
- In the `Main` method, a `Car` object `car` is created using the parameterized constructor with the values "Toyota" for make, "Camry" for model, and 2020 for year.
- The properties of the `car` object are accessed and printed to the console, showing the specific make, model, and year values provided during object creation.

This demonstrates how a parameterized constructor allows you to initialize object properties with specific values at the time of object creation. Parameterized constructors are useful for creating objects with different initial states based on the provided parameters, providing flexibility in object instantiation.

## **Static Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

A static constructor in C# is a special type of constructor used to initialize static members of a class. It is called automatically before any static member of the class is accessed for the first time. Static constructors are useful for performing one-time initialization tasks for a class's static members.

### Scenario:

Consider a scenario where you have a `Logger` class that contains static members to log messages. You want to ensure that the logging system is initialized before any other code tries to use it.

### Example:

```csharp
using System;

class Logger
{
    // Static member to count log messages
    public static int LogCount;

    // Static Constructor
    static Logger()
    {
        // Perform one-time initialization tasks
        LogCount = 0;
        Console.WriteLine("Logging system initialized.");
    }

    // Static method to log a message
    public static void Log(string message)
    {
        Console.WriteLine($"Log #{LogCount++}: {message}");
    }
}

class Program
{
    static void Main()
    {
        // Calling a static method triggers the static constructor
        Logger.Log("First log message");

        // Accessing a static member does not trigger the static constructor again
        Console.WriteLine($"Log count: {Logger.LogCount}");
    }
}
```

### Output:

```
Logging system initialized.
Log #0: First log message
Log count: 1
```

### Explanation:

In this example:
- The `Logger` class contains a static member `LogCount` to count the number of log messages and a static method `Log` to log messages.
- The `Logger` class also defines a static constructor that initializes the `LogCount` to 0 and prints a message to indicate that the logging system has been initialized.
- In the `Main` method, the `Log` method is called to log a message. This triggers the static constructor to be invoked, which initializes the logging system.
- After the static constructor is called, the log message is printed, and the `LogCount` is incremented.
- Accessing the `LogCount` static member again does not trigger the static constructor because it has already been initialized.

This demonstrates how a static constructor can be used to perform one-time initialization tasks for static members of a class in C#. Static constructors are invoked automatically before any static member of the class is accessed, ensuring that the initialization tasks are performed when needed.

## **Static Constructor Vs Non-Static Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

Let's compare static constructors and non-static constructors in C# in tabular form with detailed explanations and use cases:

| Feature                | Static Constructors                                      | Non-Static Constructors                                 |
|------------------------|----------------------------------------------------------|----------------------------------------------------------|
| Invocation             | Called automatically before any static member access      | Called explicitly by the `new` keyword                  |
| Access Modifier        | Cannot have access modifiers (always implicit `private`) | Can have various access modifiers (`public`, `private`, etc.) |
| Parameters             | Cannot have parameters                                   | Can have parameters                                      |
| Initialization         | Typically used for one-time initialization of static members | Used for initializing instance members                   |
| Use Cases              | - Initializing static fields or performing one-time initialization tasks for a class; - Initializing static data or resources; - Ensuring that static members are initialized before they are accessed | - Initializing instance fields or performing instance-specific initialization tasks; - Setting up an object's initial state based on provided parameters; - Customizing object behavior during instantiation |

### Detailed Explanation:

- **Invocation**:
  - Static constructors are automatically invoked before any static member of the class is accessed, ensuring that static members are initialized before they are used.
  - Non-static constructors are called explicitly using the `new` keyword when creating an instance of the class.

- **Access Modifier**:
  - Static constructors cannot have access modifiers and are always implicitly `private`.
  - Non-static constructors can have various access modifiers (`public`, `private`, `protected`, etc.), allowing control over their accessibility.

- **Parameters**:
  - Static constructors cannot have parameters, as they are called automatically without any arguments.
  - Non-static constructors can have parameters, allowing initialization of object properties based on provided values.

- **Initialization**:
  - Static constructors are typically used for one-time initialization of static members, such as initializing static fields or performing initialization tasks for a class.
  - Non-static constructors are used for initializing instance members, setting up an object's initial state, and performing instance-specific initialization tasks.

- **Use Cases**:
  - Static constructors are useful for ensuring that static members are initialized before they are accessed, initializing static data or resources, and performing one-time initialization tasks for a class.
  - Non-static constructors are used for setting up an object's initial state based on provided parameters, customizing object behavior during instantiation, and initializing instance fields or resources.

### Use Case Examples:

- **Static Constructors**: 
  - Initializing a static logger instance in a logging utility class.
  - Initializing a static database connection pool in a database access class.

- **Non-Static Constructors**:
  - Initializing instance variables like name, age, and gender in a `Person` class.
  - Customizing the behavior of objects based on constructor parameters, such as initializing the size and color of a `Rectangle` object.

In summary, static constructors and non-static constructors serve different purposes in C#. Static constructors are used for one-time initialization of static members, while non-static constructors are used for initializing instance members and customizing object behavior during instantiation. Understanding when to use each type of constructor is essential for designing well-structured and maintainable C# code.

## **Constructor Overloading:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

Constructor overloading in C# allows you to define multiple constructors with the same name but with different parameter lists. This enables you to create objects using different combinations of parameters, providing flexibility in object initialization.

### Scenario:

Let's consider a scenario where you have a `Rectangle` class representing rectangles. You want to create `Rectangle` objects using different combinations of parameters, such as specifying width and height, specifying only width, or specifying no parameters (default constructor).

### Example:

```csharp
using System;

class Rectangle
{
    public double Width { get; }
    public double Height { get; }

    // Constructor with different types of arguments
    public Rectangle(double width, double height)
    {
        Width = width;
        Height = height;
    }

    // Constructor with different number of arguments
    public Rectangle(double width)
    {
        Width = width;
        Height = width; // Square by default
    }

    // Constructor with different order of arguments
    public Rectangle(double height, double width)
    {
        Width = width;
        Height = height;
    }

    // Default constructor
    public Rectangle()
    {
        Width = 1;  // Default width
        Height = 1; // Default height
    }

    // Method to calculate area
    public double CalculateArea()
    {
        return Width * Height;
    }
}

class Program
{
    static void Main()
    {
        // Creating Rectangle objects using different constructors
        Rectangle rectangle1 = new Rectangle(5, 3);      // By using different type of arguments
        Rectangle rectangle2 = new Rectangle(4);         // By using different number of arguments
        Rectangle rectangle3 = new Rectangle(2, 6);      // By using different order of arguments
        Rectangle rectangle4 = new Rectangle();          // Default constructor

        // Calculating and displaying the area of each rectangle
        Console.WriteLine("Area of Rectangle 1: " + rectangle1.CalculateArea());
        Console.WriteLine("Area of Rectangle 2: " + rectangle2.CalculateArea());
        Console.WriteLine("Area of Rectangle 3: " + rectangle3.CalculateArea());
        Console.WriteLine("Area of Rectangle 4: " + rectangle4.CalculateArea());
    }
}
```

### Output:

```
Area of Rectangle 1: 15
Area of Rectangle 2: 16
Area of Rectangle 3: 12
Area of Rectangle 4: 1
```

### Explanation:

In this example:
- The `Rectangle` class defines multiple constructors to demonstrate constructor overloading.
- Constructor overloading is achieved by defining constructors with different parameter lists:
  - Constructor with different types of arguments: `(double width, double height)`
  - Constructor with different number of arguments: `(double width)` (height is set equal to width)
  - Constructor with different order of arguments: `(double height, double width)`
  - Default constructor: `()`
- Each constructor initializes the `Width` and `Height` properties of the `Rectangle` object based on the provided parameters or default values.
- In the `Main` method, different `Rectangle` objects are created using different constructors, showcasing constructor overloading.
- The area of each rectangle is calculated using the `CalculateArea` method and displayed to the console.

This demonstrates how constructor overloading allows you to create objects using different combinations of parameters, providing flexibility in object initialization based on different scenarios.

## **Overloaded Constructor using “this” keyword:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

In C#, you can use the `this` keyword within a constructor to invoke another constructor within the same class. This is known as constructor chaining or using an overloaded constructor using the `this` keyword. It allows you to avoid duplicating initialization logic by reusing it in multiple constructors within the same class.

### Scenario:

Let's consider a scenario where you have a `Person` class representing individuals. You want to create overloaded constructors to initialize `Person` objects with different combinations of properties. Instead of duplicating initialization logic in each constructor, you'll use the `this` keyword to chain constructors together.

### Example:

```csharp
using System;

class Person
{
    public string Name { get; }
    public int Age { get; }
    public string Gender { get; }

    // Constructor with all properties
    public Person(string name, int age, string gender)
    {
        Name = name;
        Age = age;
        Gender = gender;
    }

    // Constructor with only name and age (gender defaults to "Unknown")
    public Person(string name, int age) : this(name, age, "Unknown")
    {
    }

    // Constructor with only name (age defaults to 0, gender defaults to "Unknown")
    public Person(string name) : this(name, 0)
    {
    }
}

class Program
{
    static void Main()
    {
        // Creating Person objects using different constructors
        Person person1 = new Person("Alice", 30, "Female");
        Person person2 = new Person("Bob", 25);
        Person person3 = new Person("Charlie");

        // Displaying the properties of each person
        Console.WriteLine($"Person 1: {person1.Name}, {person1.Age}, {person1.Gender}");
        Console.WriteLine($"Person 2: {person2.Name}, {person2.Age}, {person2.Gender}");
        Console.WriteLine($"Person 3: {person3.Name}, {person3.Age}, {person3.Gender}");
    }
}
```

### Output:

```
Person 1: Alice, 30, Female
Person 2: Bob, 25, Unknown
Person 3: Charlie, 0, Unknown
```

### Explanation:

In this example:
- The `Person` class defines multiple constructors with different parameter lists to demonstrate constructor overloading.
- Constructor overloading is used to provide flexibility in object initialization.
- The constructor with all properties initializes all properties of the `Person` object.
- The other constructors use the `this` keyword to chain to the primary constructor, passing default values for omitted parameters.
- In the `Main` method, different `Person` objects are created using different constructors, showcasing constructor overloading and constructor chaining.
- The properties of each `Person` object are displayed to the console, showing the result of object initialization.

This demonstrates how you can use the `this` keyword to chain constructors together, avoiding code duplication and providing flexibility in object initialization in C#.

## **Overloaded Constructor using Copy Constructor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

In C#, you can overload the copy constructor of a class to provide different ways of copying objects. Overloading the copy constructor allows you to customize the copying process based on specific requirements or scenarios.

### Scenario:

Consider a scenario where you have a `Rectangle` class representing rectangles, and you want to provide different ways of copying `Rectangle` objects. You may want to copy only the dimensions, or you may want to perform a deep copy including additional properties.

### Example:

```csharp
using System;

class Rectangle
{
    public double Width { get; }
    public double Height { get; }
    public string Color { get; }

    // Constructor with dimensions and color
    public Rectangle(double width, double height, string color)
    {
        Width = width;
        Height = height;
        Color = color;
    }

    // Copy constructor (overloaded)
    public Rectangle(Rectangle other)
    {
        Width = other.Width;
        Height = other.Height;
        Color = other.Color;
    }

    // Method to display rectangle information
    public void DisplayInfo()
    {
        Console.WriteLine($"Width: {Width}, Height: {Height}, Color: {Color}");
    }
}

class Program
{
    static void Main()
    {
        // Creating a rectangle
        Rectangle originalRectangle = new Rectangle(5, 3, "Red");

        // Copying the rectangle using the copy constructor
        Rectangle copiedRectangle = new Rectangle(originalRectangle);

        // Displaying information of both rectangles
        Console.WriteLine("Original Rectangle:");
        originalRectangle.DisplayInfo();

        Console.WriteLine("\nCopied Rectangle:");
        copiedRectangle.DisplayInfo();
    }
}
```

### Output:

```
Original Rectangle:
Width: 5, Height: 3, Color: Red

Copied Rectangle:
Width: 5, Height: 3, Color: Red
```

### Explanation:

In this example:
- The `Rectangle` class defines a copy constructor that takes another `Rectangle` object as its parameter. This constructor is used to create a copy of a `Rectangle` object.
- Inside the copy constructor, the dimensions (`Width` and `Height`) and color properties of the new `Rectangle` object are initialized with the values of the corresponding properties of the `other` `Rectangle` object.
- In the `Main` method, an original `Rectangle` object `originalRectangle` is created with dimensions 5x3 and color "Red".
- Then, a copy of the original `Rectangle` object is created using the copy constructor, resulting in a new `Rectangle` object `copiedRectangle` with the same dimensions and color as the original object.
- The information of both the original and copied rectangles is displayed to the console, showing that the copied rectangle has the same properties as the original rectangle.

This demonstrates how you can overload the copy constructor in C# to customize the copying process of objects, providing flexibility in object duplication based on specific requirements or scenarios.

## **Destructors in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/5%20-%20Constructors.md#constructors-)

In C#, destructors are special methods used to clean up resources and perform finalization tasks before an object is destroyed or garbage collected. Unlike constructors, which are used to initialize objects when they are created, destructors are invoked automatically when an object is about to be removed from memory.

### Example:

```csharp
using System;

class MyClass
{
    // Destructor
    ~MyClass()
    {
        Console.WriteLine("Destructor called.");
    }
}

class Program
{
    static void Main()
    {
        // Creating an object of MyClass
        MyClass myObject = new MyClass();

        // No explicit call to the destructor
        // Destructor will be called when the object is garbage collected
    }
}
```

### Output:

```
Destructor called.
```

### Explanation:

In this example:
- The `MyClass` class defines a destructor using the `~` symbol followed by the class name.
- The destructor is automatically invoked when the `myObject` object of `MyClass` is no longer in use and is eligible for garbage collection.
- In the `Main` method, an object of `MyClass` is created using the `new` keyword.
- When the program terminates or when the object is no longer referenced and is garbage collected, the destructor is automatically called, and "Destructor called." is printed to the console.

### Note:

- Destructors are not explicitly called like constructors. They are automatically invoked by the garbage collector when the object is being collected.
- Destructors cannot be overloaded or inherited. Each class can have only one destructor.
- Destructors cannot have parameters or modifiers.
- It's important to note that destructors are less commonly used in C# compared to constructors, as C# provides other mechanisms such as the `using` statement and IDisposable interface for managing resources more efficiently.