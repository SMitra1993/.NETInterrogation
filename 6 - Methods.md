# Methods ❤🍕

**Links:**

- [Methods in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-in-c-)
- [Method Overloading](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#method-overloading-)
- [Method Parameter](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#method-parameter-)
- [Method Overriding](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#method-overriding-)
- [Method Hiding](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#method-hiding-)
- [Method Overriding vs Method Hiding](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#method-overriding-vs-method-hiding-)
- [Various ways to make method parameter as optional](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#various-ways-to-make-method-parameter-as-optional-)
- [ref Vs out parameter](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#ref-vs-out-parameter-)
- [Anonymous Method](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#anonnymous-method-)
- [Partial Method](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#partial-method-)
- [Extension Method](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#extension-method-)
- [Local Function](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#local-function-)

## **Methods in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

In C#, methods are blocks of code within a class or struct that perform a specific task. They encapsulate functionality and can be called to execute their code. Let's explore methods in C# in detail, covering function declaration, calling, definition with or without parameters, and with or without return types, along with examples and outputs:

### 1. Function Declaration:

In C#, method declaration includes the method signature, which consists of the method name, parameters (if any), return type, and access modifiers.

#### Example:

```csharp
public class Calculator
{
    // Method declaration without parameters and return type
    public void DisplayMessage()
    {
        Console.WriteLine("Hello, World!");
    }

    // Method declaration with parameters and return type
    public int Add(int a, int b)
    {
        return a + b;
    }
}
```

### 2. Function Calling:

To call a method, you specify the method name followed by parentheses `()`. If the method requires parameters, you provide the values within the parentheses.

#### Example:

```csharp
class Program
{
    static void Main()
    {
        Calculator calculator = new Calculator();

        // Calling method without parameters and return type
        calculator.DisplayMessage();

        // Calling method with parameters and return type
        int result = calculator.Add(5, 3);
        Console.WriteLine("Result: " + result);
    }
}
```

#### Output:

```
Hello, World!
Result: 8
```

### 3. Function Definition:

#### a. With Parameters and Return Type:

```csharp
// Method definition with parameters and return type
public int Add(int a, int b)
{
    return a + b;
}
```

#### b. Without Parameters and Return Type:

```csharp
// Method definition without parameters and return type
public void DisplayMessage()
{
    Console.WriteLine("Hello, World!");
}
```

### 4. Function Parameters:

Methods can have parameters, which are variables that accept values passed into the method when it is called.

#### Example:

```csharp
// Method with parameters
public int Add(int a, int b)
{
    return a + b;
}
```

### 5. Return Type:

Methods can have return types, indicating the type of value they return after execution. If a method does not return anything, its return type is `void`.

#### Example:

```csharp
// Method with return type
public int Add(int a, int b)
{
    return a + b;
}
```

### Summary:

- Methods in C# encapsulate functionality and can be called to execute their code.
- Method declaration includes the method signature, specifying the method name, parameters, return type, and access modifiers.
- Methods can be called by specifying the method name followed by parentheses, with or without parameters.
- Method definition includes the actual implementation of the method's functionality, which may include parameters and a return type.

## **Method Overloading:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Method overloading in C# allows you to define multiple methods in a class with the same name but different parameter lists. This enables you to provide different implementations of a method based on the types and number of parameters passed to it. Let's explore different ways to create method overloading in C# with examples and outputs:

### 1. Overloading by Different Number of Parameters:

You can overload a method by providing different numbers of parameters in each method signature.

#### Example:

```csharp
public class Calculator
{
    // Method to add two integers
    public int Add(int a, int b)
    {
        return a + b;
    }

    // Method to add three integers
    public int Add(int a, int b, int c)
    {
        return a + b + c;
    }
}

class Program
{
    static void Main()
    {
        Calculator calculator = new Calculator();

        // Calling overloaded methods
        int result1 = calculator.Add(5, 3);
        int result2 = calculator.Add(5, 3, 2);

        Console.WriteLine("Result 1: " + result1); // Output: Result 1: 8
        Console.WriteLine("Result 2: " + result2); // Output: Result 2: 10
    }
}
```

### 2. Overloading by Different Data Types of Parameters:

You can also overload a method by providing parameters with different data types.

#### Example:

```csharp
public class Printer
{
    // Method to print an integer
    public void Print(int number)
    {
        Console.WriteLine("Integer: " + number);
    }

    // Method to print a double
    public void Print(double number)
    {
        Console.WriteLine("Double: " + number);
    }
}

class Program
{
    static void Main()
    {
        Printer printer = new Printer();

        // Calling overloaded methods
        printer.Print(5);       // Output: Integer: 5
        printer.Print(3.14);    // Output: Double: 3.14
    }
}
```

### 3. Overloading by Different Sequence of Parameters:

Method overloading can also be achieved by providing parameters in a different sequence.

#### Example:

```csharp
public class ShapeCalculator
{
    // Method to calculate area of rectangle
    public double CalculateArea(double length, double breadth)
    {
        return length * breadth;
    }

    // Method to calculate area of triangle
    public double CalculateArea(double baseLength, double height, string shape)
    {
        if (shape == "triangle")
        {
            return 0.5 * baseLength * height;
        }
        return 0; // Placeholder for other shapes
    }
}

class Program
{
    static void Main()
    {
        ShapeCalculator calculator = new ShapeCalculator();

        // Calling overloaded methods
        double rectangleArea = calculator.CalculateArea(5, 3);
        double triangleArea = calculator.CalculateArea(4, 6, "triangle");

        Console.WriteLine("Rectangle Area: " + rectangleArea); // Output: Rectangle Area: 15
        Console.WriteLine("Triangle Area: " + triangleArea);   // Output: Triangle Area: 12
    }
}
```

### Summary:

- Method overloading in C# allows you to define multiple methods with the same name but different parameter lists.
- Overloading can be achieved by providing different numbers, types, or sequences of parameters in the method signatures.
- Overloaded methods provide flexibility and improve code readability by allowing multiple implementations of a method with similar functionality.

## **Method Parameter:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Method parameters in C# are variables that are defined within the parentheses of a method declaration and are used to pass values to the method when it is called. These parameters allow methods to accept input data and perform operations on that data. Method parameters play a crucial role in defining the behavior and functionality of a method.

Let's explore each of the mentioned method parameter types with examples and outputs:

### 1. Named Parameters:

Named parameters allow you to specify the parameter name along with the value when calling a method, which can improve code readability.

#### Example:

```csharp
public class Person
{
    public void DisplayInfo(string name, int age)
    {
        Console.WriteLine("Name: " + name);
        Console.WriteLine("Age: " + age);
    }
}

class Program
{
    static void Main()
    {
        Person person = new Person();

        // Calling method with named parameters
        person.DisplayInfo(name: "John", age: 30);
        person.DisplayInfo(age: 25, name: "Alice");

        // Output:
        // Name: John
        // Age: 30
        // Name: Alice
        // Age: 25
    }
}
```

### 2. Ref Parameters:

Ref parameters allow a method to modify the value of a parameter directly, which affects the original variable passed as an argument.

#### Example:

```csharp
public class MathOperations
{
    public void Increment(ref int number)
    {
        number++;
    }
}

class Program
{
    static void Main()
    {
        MathOperations math = new MathOperations();
        int value = 5;

        // Calling method with ref parameter
        math.Increment(ref value);

        Console.WriteLine("Value after increment: " + value); // Output: Value after increment: 6
    }
}
```

### 3. Out Parameters:

Out parameters allow a method to return multiple values by modifying the original variable passed as an argument.

#### Example:

```csharp
public class MathOperations
{
    public void Divide(int dividend, int divisor, out int quotient, out int remainder)
    {
        quotient = dividend / divisor;
        remainder = dividend % divisor;
    }
}

class Program
{
    static void Main()
    {
        MathOperations math = new MathOperations();
        int dividend = 10;
        int divisor = 3;
        int quotient, remainder;

        // Calling method with out parameters
        math.Divide(dividend, divisor, out quotient, out remainder);

        Console.WriteLine("Quotient: " + quotient);   // Output: Quotient: 3
        Console.WriteLine("Remainder: " + remainder); // Output: Remainder: 1
    }
}
```

### 4. Default or Optional Parameters:

Default parameters allow you to specify default values for method parameters, making them optional when calling the method.

#### Example:

```csharp
public class Greeting
{
    public void SayHello(string name = "Guest")
    {
        Console.WriteLine("Hello, " + name + "!");
    }
}

class Program
{
    static void Main()
    {
        Greeting greeting = new Greeting();

        // Calling method with default parameter
        greeting.SayHello();          // Output: Hello, Guest!
        greeting.SayHello("John");    // Output: Hello, John!
    }
}
```

### 5. Dynamic Parameters:

Dynamic parameters allow you to pass arguments of any type to a method, and their types are resolved at runtime.

#### Example:

```csharp
public class DataProcessor
{
    public void Process(dynamic data)
    {
        Console.WriteLine("Data Type: " + data.GetType());
    }
}

class Program
{
    static void Main()
    {
        DataProcessor processor = new DataProcessor();

        // Calling method with dynamic parameter
        processor.Process(10);          // Output: Data Type: System.Int32
        processor.Process("Hello");      // Output: Data Type: System.String
        processor.Process(3.14);         // Output: Data Type: System.Double
    }
}
```

### 6. Value Parameters:

Value parameters are the default parameter type in C#. They pass the value of the argument to the method.

#### Example:

```csharp
public class MathOperations
{
    public void Square(int number)
    {
        Console.WriteLine("Square: " + (number * number));
    }
}

class Program
{
    static void Main()
    {
        MathOperations math = new MathOperations();
        int value = 5;

        // Calling method with value parameter
        math.Square(value); // Output: Square: 25
    }
}
```

### 7. Params:

Params parameters allow you to specify a variable number of arguments of the same type for a method.

#### Example:

```csharp
public class MathOperations
{
    public int Sum(params int[] numbers)
    {
        int sum = 0;
        foreach (int num in numbers)
        {
            sum += num;
        }
        return sum;
    }
}

class Program
{
    static void Main()
    {
        MathOperations math = new MathOperations();

        // Calling method with params parameter
        int result = math.Sum(1, 2, 3, 4, 5);
        Console.WriteLine("Sum: " + result); // Output: Sum: 15
    }
}
```

### Summary:

- Named parameters improve code readability by explicitly specifying parameter names.
- Ref parameters allow methods to modify the original variable passed as an argument.
- Out parameters enable methods to return multiple values by modifying the original variables.
- Default parameters provide default values for method parameters, making them optional.
- Dynamic parameters allow passing arguments of any type to a method.
- Value parameters pass the value of the argument to the method.
- Params parameters allow a variable number of arguments of the same type for a method.

## **Method Overriding:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Method overriding in C# is a feature of object-oriented programming that allows a derived class to provide a specific implementation of a method that is already defined in its base class. This enables polymorphism, where the same method name can behave differently based on the object type. Here's a detailed explanation of method overriding with examples and outputs:

### How Method Overriding Works:

When a method is overridden in a derived class, the method signature (name, return type, and parameters) must match the method signature in the base class. The derived class provides its implementation of the method, which overrides the implementation in the base class. When a method is called on an object of the derived class, the runtime determines which version of the method to execute based on the actual type of the object.

### Example:

Let's consider a scenario where we have a base class `Shape` with a method `Draw`, and we want to override this method in derived classes `Circle` and `Rectangle`.

```csharp
using System;

public class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape.");
    }
}

public class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}

public class Rectangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a rectangle.");
    }
}

class Program
{
    static void Main()
    {
        Shape shape1 = new Circle();
        Shape shape2 = new Rectangle();

        shape1.Draw(); // Output: Drawing a circle.
        shape2.Draw(); // Output: Drawing a rectangle.
    }
}
```

### Explanation:

- In the `Shape` class, we define a virtual method `Draw` that prints "Drawing a shape."
- The `Circle` and `Rectangle` classes inherit from `Shape` and override the `Draw` method with their specific implementations.
- In the `Main` method, we create objects of type `Circle` and `Rectangle` and assign them to variables of type `Shape`. This demonstrates polymorphism.
- When we call the `Draw` method on the `shape1` and `shape2` objects, the overridden versions of the method in the `Circle` and `Rectangle` classes are executed, respectively.

### Output:

```
Drawing a circle.
Drawing a rectangle.
```

### Summary:

- Method overriding allows derived classes to provide specific implementations of methods defined in their base classes.
- The `override` keyword is used in the derived class to indicate that a method is overriding a base class method.
- Method overriding enables polymorphism, allowing objects of different types to respond differently to the same method call.
- When a method is called on a base class reference pointing to an object of a derived class, the overridden version of the method in the derived class is invoked, providing dynamic behavior based on the object's actual type.

### **`virtual`,`override`, and `base` keywords:**

Let's break down each of these keywords:

### 1. `virtual` Keyword:

In C#, the `virtual` keyword is used to declare a method, property, or indexer in a base class that can be overridden in derived classes. Here's what it does:

- **Base Class Declaration:** When a method is declared as `virtual` in a base class, it means that the method can be overridden (redefined) in derived classes.
- **Dynamic Binding:** It enables polymorphism, allowing the runtime environment to determine which version of the method to call based on the actual type of the object.
- **Default Implementation:** If a derived class does not override a `virtual` method, it will inherit the base class's implementation.

### 2. `override` Keyword:

The `override` keyword is used in a derived class to override a `virtual` method declared in its base class. Here's what it does:

- **Derived Class Override:** When a method is marked as `override`, it provides a new implementation for a `virtual` method declared in the base class.
- **Method Redefinition:** It replaces the implementation of the base class method with the implementation defined in the derived class.
- **Dynamic Polymorphism:** It enables dynamic binding, allowing the runtime environment to call the appropriate overridden method based on the object's actual type.

### 3. `base` Keyword:

The `base` keyword in C# provides a way to access members (methods, properties, fields) of the base class within a derived class. Here's what it does:

- **Accessing Base Members:** It allows a derived class to invoke methods or access members defined in its base class.
- **Method Invocation:** It can be used to explicitly call a method from the base class that has been overridden in the derived class.
- **Constructor Invocation:** It is used to call the constructor of the base class from within the constructor of the derived class, allowing initialization of base class members.

### Example:

Here's an example demonstrating the use of `virtual`, `override`, and `base`:

```csharp
using System;

public class BaseClass
{
    public virtual void Method1()
    {
        Console.WriteLine("BaseClass.Method1");
    }
}

public class DerivedClass : BaseClass
{
    public override void Method1()
    {
        base.Method1(); // Call base class method
        Console.WriteLine("DerivedClass.Method1");
    }
}

class Program
{
    static void Main()
    {
        DerivedClass obj = new DerivedClass();
        obj.Method1(); // Output: BaseClass.Method1, DerivedClass.Method1
    }
}
```

### Summary:

- `virtual`: Declares a method in a base class that can be overridden in derived classes.
- `override`: Overrides a `virtual` method in a derived class, providing a new implementation.
- `base`: Provides access to members of the base class within a derived class, including method invocation and constructor chaining.

## **Method Hiding:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Method hiding in C# occurs when a method in a derived class has the same name and signature as a method in its base class. Unlike method overriding, where the derived method replaces the base method implementation, method hiding introduces a new method in the derived class that "hides" the base class method. This means that the derived class method is called instead of the base class method when accessed through a reference to the derived class.

### How Method Hiding Works:

1. **New Keyword:** To hide a method from the base class, you use the `new` keyword in the derived class method declaration.
2. **Name and Signature:** The method in the derived class must have the same name and signature as the method in the base class to hide it.
3. **Shadowing:** When a method is hidden, it is said to be shadowed by the method in the derived class. The base class method still exists but is inaccessible through the derived class reference variable.

### Example:

Let's illustrate method hiding with an example:

```csharp
using System;

public class BaseClass
{
    public void Display()
    {
        Console.WriteLine("BaseClass.Display");
    }
}

public class DerivedClass : BaseClass
{
    public new void Display()
    {
        Console.WriteLine("DerivedClass.Display");
    }
}

class Program
{
    static void Main()
    {
        BaseClass obj1 = new DerivedClass();
        obj1.Display(); // Output: BaseClass.Display

        DerivedClass obj2 = new DerivedClass();
        obj2.Display(); // Output: DerivedClass.Display

        BaseClass obj3 = new DerivedClass();
        ((DerivedClass)obj3).Display(); // Output: DerivedClass.Display
    }
}
```

### Explanation:

- The `BaseClass` defines a method named `Display`.
- The `DerivedClass` hides the `Display` method of the base class using the `new` keyword and provides its implementation.
- When `obj1` is of type `BaseClass` but refers to an instance of `DerivedClass`, calling `Display` accesses the base class method because the reference type is `BaseClass`.
- When `obj2` is of type `DerivedClass`, calling `Display` accesses the derived class method directly.
- To call the hidden method in the derived class through a base class reference (`obj3`), you can cast it to `DerivedClass`.

### Output:

```
BaseClass.Display
DerivedClass.Display
DerivedClass.Display
```

### Summary:

- Method hiding occurs when a derived class introduces a new method with the same name and signature as a method in the base class.
- The `new` keyword is used to hide the base class method in the derived class.
- Method hiding is different from method overriding because the base class method is still accessible but shadowed by the derived class method.
- You can access the hidden method through casting or by using a reference variable of the derived class type.

## **Method Overriding vs Method Hiding:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

| Aspect                 | Method Overriding                                    | Method Hiding                                          |
|------------------------|------------------------------------------------------|--------------------------------------------------------|
| Purpose                | Provides a way for a derived class to provide a specific implementation of a method declared in the base class. | Introduces a new method in a derived class with the same name and signature as a method in the base class. |
| Keyword                | `override`                                           | `new`                                                  |
| Base Class Method      | Must be declared as `virtual`                        | Not required to be declared as `virtual`               |
| Derived Class Method   | Must be declared as `override`                       | Must be declared with the `new` keyword                |
| Inheritance            | Follows the principle of inheritance and polymorphism | Follows the principle of hiding or shadowing           |
| Dynamic Binding        | Enables dynamic polymorphism, allowing the runtime environment to determine which version of the method to call based on the object's actual type. | The version of the method called is determined by the compile-time type of the reference variable. If the reference type is of the base class, the base class method is called. |
| Access to Base Method  | Can call the base class method using `base.Method()` | The base class method is shadowed and not directly accessible through a derived class reference variable. |
| Interaction with Base  | Enhances or modifies the behavior of the base class method. | Introduces a new method that may have different behavior from the base class method. |
| Example                | ```csharp public class BaseClass { public virtual void Method() { Console.WriteLine("BaseClass.Method"); } } public class DerivedClass : BaseClass { public override void Method() { Console.WriteLine("DerivedClass.Method"); } } ``` | ```csharp public class BaseClass { public void Method() { Console.WriteLine("BaseClass.Method"); } } public class DerivedClass : BaseClass { public new void Method() { Console.WriteLine("DerivedClass.Method"); } } ``` |

### Summary:

- Method overriding allows derived classes to provide specific implementations of methods declared in the base class, enhancing or modifying their behavior.
- Method hiding introduces new methods in derived classes that shadow methods in the base class, potentially providing different behavior.
- Method overriding enables dynamic polymorphism, allowing the runtime environment to determine the appropriate method to call based on the object's actual type.
- Method hiding is determined by the compile-time type of the reference variable, and the version of the method called is based on the reference type.

## **Various ways to make method parameter as optional:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

### 1. By Using Default Value:

You can specify a default value for a method parameter in its declaration. If no argument is provided for that parameter when calling the method, the default value will be used.

Example:

```csharp
public void PrintMessage(string message = "Hello")
{
    Console.WriteLine(message);
}

// Calling the method without passing any argument
PrintMessage(); // Output: Hello
PrintMessage("Goodbye"); // Output: Goodbye
```

### 2. By Using OptionalAttribute:

The `OptionalAttribute` is used to specify that a parameter is optional. This allows the parameter to be omitted when calling the method.

Example:

```csharp
using System.Runtime.InteropServices;

public void PrintMessage([Optional] string message)
{
    Console.WriteLine(message ?? "Hello");
}

// Calling the method without passing any argument
PrintMessage(); // Output: Hello
PrintMessage("Goodbye"); // Output: Goodbye
```

### 3. By Using Params Keyword:

You can use the `params` keyword to specify a variable number of arguments for a method parameter. This allows you to call the method with zero or more arguments of the specified type.

Example:

```csharp
public void PrintMessages(params string[] messages)
{
    foreach (string message in messages)
    {
        Console.WriteLine(message);
    }
}

// Calling the method with variable number of arguments
PrintMessages(); // Output: (nothing)
PrintMessages("Hello", "Goodbye"); // Output: Hello Goodbye
```

### 4. By Using Method Overloading:

You can create overloaded versions of the method, each with a different number of parameters. This allows callers to choose which version of the method to call based on their needs.

Example:

```csharp
public void PrintMessage(string message)
{
    Console.WriteLine(message);
}

public void PrintMessage()
{
    PrintMessage("Hello");
}

// Calling the overloaded methods
PrintMessage(); // Output: Hello
PrintMessage("Goodbye"); // Output: Goodbye
```

### Summary:

- Making method parameters optional in C# provides flexibility and allows callers to choose whether or not to provide values for those parameters.
- Different approaches, such as default values, `OptionalAttribute`, `params` keyword, and method overloading, can be used to achieve optional parameters, depending on the specific requirements of the method and the calling code.

## **ref Vs out parameter:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Here's a detailed comparison between `ref` and `out` parameters in C#:

| Aspect                 | ref Parameter                                         | out Parameter                                           |
|------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Initialization         | Required to be initialized before being passed        | Not required to be initialized before being passed      |
| Input/Output           | Can act as both input and output parameters           | Primarily used as output parameters                      |
| Initial Value Preserved| The initial value of the parameter is preserved       | The initial value of the parameter is ignored            |
| Method Invocation      | Must be initialized before calling the method         | Can be uninitialized before calling the method           |
| Method Modification    | Can modify the parameter value inside the method      | Must assign a value to the parameter inside the method  |
| Return Value           | Can return multiple values through the parameter      | Typically used to return a single value from a method    |
| Compiler Verification  | Must be initialized before use; compiler error if not | No compiler error if not initialized before use          |
| Examples               |```csharp public void Swap(ref int a, ref int b) { int temp = a; a = b; b = temp; }``` | ```csharp public void Divide(int dividend, int divisor, out int quotient) { quotient = dividend / divisor; }``` |

### Summary:

- `ref` parameters are primarily used for both input and output values, while `out` parameters are mainly used for output values.
- `ref` parameters must be initialized before being passed to a method, whereas `out` parameters do not require initialization.
- Inside a method, `ref` parameters can modify the value of the variable they reference, while `out` parameters must be assigned a value before leaving the method.
- `ref` parameters preserve their initial value, while `out` parameters ignore their initial value.
- `ref` parameters can return multiple values, while `out` parameters are typically used to return a single value from a method.

## **Anonymous Method:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

An anonymous method in C# is a method without a name. It allows you to define a method "on the fly" without explicitly declaring a separate method. Anonymous methods are often used as arguments to other methods, such as event handlers or LINQ queries.

### Example:

Let's consider an example where we use an anonymous method to define a delegate that calculates the square of a given number.

```csharp
using System;

public class Program
{
    public delegate int SquareDelegate(int x);

    public static void Main(string[] args)
    {
        // Define an anonymous method and assign it to a delegate
        SquareDelegate square = delegate (int x)
        {
            return x * x;
        };

        // Call the delegate with an argument
        int result = square(5);

        Console.WriteLine("Square of 5: " + result);
    }
}
```

### Output:

```
Square of 5: 25
```

### Explanation:

- In this example, we define a delegate `SquareDelegate` that represents a method that takes an integer parameter and returns an integer.
- We then create an instance of the delegate `square` and assign it an anonymous method that calculates the square of the input parameter.
- Finally, we call the delegate with an argument (`5`), which invokes the anonymous method and returns the square of `5`.

### Summary:

- Anonymous methods provide a way to define methods inline without explicitly declaring a separate method.
- They are often used for short, one-off operations, such as event handlers or simple calculations.
- Anonymous methods are defined using the `delegate` keyword followed by a parameter list and method body.

## **Partial Method:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Partial methods in C# allow a method declaration to be split into two parts: the declaration and the implementation. One part is defined in a partial class or struct, and the other part is optionally defined in a separate part of the class or struct.

### Example:

Let's consider an example where we define a partial class with a partial method for logging.

```csharp
using System;

// Partial class definition
public partial class Logger
{
    partial void LogMessage(string message); // Declaration of partial method
}

// Another part of the partial class
public partial class Logger
{
    public void PerformLogging(string message)
    {
        // Call the partial method
        LogMessage(message);
    }

    public void LogMessage(string message)
    {
        // Call the partial method
        Console.WriteLine(message);
    }
}

public class Program
{
    static void Main(string[] args)
    {
        Logger logger = new Logger();
        logger.LogMessage("This is a log message."); // Call the PerformLogging method
    }
}
```

### Output:

```
Log message: This is a log message.
```

### Explanation:

- In this example, we define a partial class `Logger` with two parts. The first part contains the declaration of the partial method `LogMessage`, while the second part contains the implementation of the method `PerformLogging`.
- The `PerformLogging` method calls the `LogMessage` method. However, since `LogMessage` is a partial method, its implementation is optional.
- If the partial method is implemented in another part of the class or struct, the call to the partial method is valid and executes the implementation code. Otherwise, the call to the partial method is removed by the compiler, resulting in no code generation for that method.

### Summary:

- Partial methods allow a method declaration to be split into declaration and implementation parts.
- The declaration part is required, but the implementation part is optional.
- Partial methods are typically used for event handling, allowing code generators to insert custom logic without requiring modification of the main codebase.

## **Extension Method:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Extension methods in C# allow you to add new methods to existing types without modifying their source code. These methods are called as if they were instance methods of the extended type.

### Example:

Let's create an extension method for the `string` class that counts the number of words in a string.

```csharp
using System;

public static class StringExtensions
{
    public static int WordCount(this string str)
    {
        return str.Split(new char[] { ' ', '.', '?' }, StringSplitOptions.RemoveEmptyEntries).Length;
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        string sentence = "Extension methods are a powerful feature of C#.";
        int count = sentence.WordCount();
        Console.WriteLine("Word count: " + count);
    }
}
```

### Output:

```
Word count: 7
```

### Explanation:

- In this example, we define an extension method `WordCount` for the `string` class by creating a static class `StringExtensions`.
- The `WordCount` method takes a `string` parameter named `str` and returns an `int` representing the number of words in the string.
- We use the `Split` method to split the string into words using spaces, periods, and question marks as delimiters, and then count the resulting array's length.
- The extension method is invoked on a `string` object `sentence` as if it were an instance method of the `string` class.

### Summary:

- Extension methods allow you to add new methods to existing types without modifying their source code.
- They are defined as static methods in static classes, with the first parameter preceded by the `this` keyword, indicating the type being extended.
- Extension methods are called as if they were instance methods of the extended type, providing a convenient way to add functionality to existing types.

## **Local Function:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/6%20-%20Methods.md#methods-)

Local functions in C# allow you to define methods within another method's scope. These methods are only accessible within the declaring method, making them useful for encapsulating logic that is specific to that method.

### Example:

Let's create a method that calculates the factorial of a number using a local function.

```csharp
using System;

public class Program
{
    public static void Main(string[] args)
    {
        int number = 5;
        int factorial = CalculateFactorial(number);
        Console.WriteLine($"Factorial of {number} is {factorial}");
    }

    public static int CalculateFactorial(int n)
    {
        if (n < 0)
        {
            throw new ArgumentException("Number must be non-negative", nameof(n));
        }

        // Local function to calculate factorial
        int Factorial(int x)
        {
            if (x == 0)
            {
                return 1;
            }
            return x * Factorial(x - 1);
        }

        return Factorial(n);
    }
}
```

### Output:

```
Factorial of 5 is 120
```

### Explanation:

- In this example, we define a method `CalculateFactorial` that takes an integer parameter `n` and calculates its factorial.
- Within the `CalculateFactorial` method, we define a local function `Factorial` to perform the factorial calculation.
- The `Factorial` function is only accessible within the `CalculateFactorial` method and encapsulates the logic for calculating the factorial recursively.
- We call the `Factorial` function to calculate the factorial of the given number `n` and return the result.

### Summary:

- Local functions in C# allow you to define methods within the scope of another method.
- They are only accessible within the declaring method and provide a way to encapsulate logic specific to that method.
- Local functions can access the variables and parameters of the enclosing method, making them useful for implementing helper functions or recursive algorithms.
- `ref`, `out`, and `params` are allowed to use in local functions.