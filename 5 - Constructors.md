# Constructors ❤🍕

## **Constructors in c#:**

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

### Default Constructor:

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

### Parameterized Constructor:

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

### Copy Constructor:

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

### Private Constructor:

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

### Static Constructor:

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

## **Default Constructor:**

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

## **Copy Constructor:**

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

## **Private Constructor:**

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

## **Parameterized Constructor:**

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

## **Static Constructor:**

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

## **Static Constructor Vs Non-Static Constructor:**

Sure, let's compare static constructors and non-static constructors in C# in tabular form with detailed explanations and use cases:

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

## 