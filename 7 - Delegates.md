# Delegates ❤🍕

**Links:**

- [Delegates](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates--1)
- [Multicasting Delegate](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#multicasting-delegate-)
- [Predicate Delegate](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#multicasting-delegate-)
- [Func Delegate](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#func-delegate-)
- [Action Delegate](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#action-delegate-)
- [Func Vs Action Vs Predicate Delegates](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#func-vs-action-vs-predicate-delegates-)

## **Delegates:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

Delegates in C# are reference types that represent methods with a specific signature. They provide a way to pass methods as parameters, store them in variables, and invoke them dynamically.

### Declaration of Delegates:

Delegates are declared using the `delegate` keyword followed by the signature of the method that the delegate can reference. Here's the general syntax:

```csharp
Modifier delegate ReturnType DelegateName(ParameterList);
```

### Example:

Let's declare a delegate named `MathOperation` that represents methods taking two integers as parameters and returning an integer.

```csharp
public delegate int MathOperation(int a, int b);
```

### Instantiation & Invocation of Delegates:

Once a delegate is declared, you can create instances of it and assign methods to it using the method name or lambda expressions.

#### Example:

Let's create an instance of the `MathOperation` delegate and assign the `Add` and `Subtract` methods to it.

```csharp
public class Program
{
    public static int Add(int a, int b)
    {
        return a + b;
    }

    public static int Subtract(int a, int b)
    {
        return a - b;
    }

    public static void Main(string[] args)
    {
        // Instantiate the delegate and assign methods
        MathOperation addOperation = new MathOperation(Add);
        MathOperation subtractOperation = Subtract;

        // Invoke the delegates
        int result1 = addOperation(5, 3); // Invokes the Add method
        int result2 = subtractOperation(5, 3); // Invokes the Subtract method

        Console.WriteLine($"Addition result: {result1}");
        Console.WriteLine($"Subtraction result: {result2}");
    }
}
```

### Output:

```
Addition result: 8
Subtraction result: 2
```

### Explanation:

- In this example, we declare a `MathOperation` delegate representing methods that take two integers as parameters and return an integer.
- We define two static methods `Add` and `Subtract`, which match the signature of the delegate.
- We create instances of the `MathOperation` delegate (`addOperation` and `subtractOperation`) and assign the `Add` and `Subtract` methods to them, respectively.
- We then invoke the delegates as if they were methods, passing arguments `(5, 3)` to perform addition and subtraction.
- The delegate instances call the assigned methods (`Add` and `Subtract`), and the results are printed to the console.

### Benefits:

1. **Encapsulation**: Delegates allow you to encapsulate methods, enabling you to pass methods as parameters to other methods, store them in variables, or return them from methods. This promotes cleaner and more modular code by separating concerns and improving code organization.

2. **Flexibility**: Delegates provide a flexible way to implement callback mechanisms, event handling, and other scenarios requiring dynamic method invocation. They enable you to dynamically change behavior at runtime by replacing the method a delegate points to.

3. **Reusability**: Delegates promote code reusability by allowing you to pass methods as arguments to multiple methods or classes. This eliminates the need to duplicate code and encourages the creation of generic, reusable components.

4. **Decoupling**: Delegates help decouple components in a system by removing direct dependencies between them. Instead of tightly coupling components by directly calling methods, delegates allow components to interact indirectly through callback mechanisms, promoting better separation of concerns.

5. **Asynchronous Programming**: Delegates are often used in asynchronous programming models, such as the Event-based Asynchronous Pattern (EAP) or the Asynchronous Programming Model (APM), to define callback methods for asynchronous operations. They enable you to execute code asynchronously without blocking the main thread.

6. **Dynamic Invocation**: Delegates enable dynamic method invocation at runtime, allowing you to call methods dynamically based on conditions or user input. This dynamic dispatch mechanism is useful in scenarios where the exact method to be invoked may vary at runtime.

7. **Extension Methods**: Delegates can be used to define extension methods, which allow you to add new functionality to existing types without modifying their source code. This enables you to extend the behavior of classes or interfaces without inheritance or modification.

### Summary:

- Delegates in C# allow you to pass methods as parameters, store them in variables, and invoke them dynamically.
- Delegates are declared using the `delegate` keyword, specifying the method signature they can reference.
- You can create instances of delegates and assign methods to them using the method name or lambda expressions.
- Delegates provide a flexible way to implement callback mechanisms, event handling, and other scenarios requiring dynamic method invocation.

## **Multicasting Delegate:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

Multicasting of delegates in C# refers to the ability to combine multiple methods into a single delegate instance. This allows you to invoke multiple methods sequentially through a single delegate invocation.

### Example:

Let's create a delegate representing a simple operation and then multicast multiple methods to it.

```csharp
using System;

public delegate void SimpleOperation(int value);

public class Program
{
    public static void Main(string[] args)
    {
        // Create instances of the delegate and multicast methods to it
        SimpleOperation operations = null;
        operations += DoubleValue;
        operations += TripleValue;

        // Invoke the delegate, which will invoke both methods sequentially
        operations?.Invoke(5);
    }

    public static void DoubleValue(int value)
    {
        Console.WriteLine($"Double of {value}: {value * 2}");
    }

    public static void TripleValue(int value)
    {
        Console.WriteLine($"Triple of {value}: {value * 3}");
    }
}
```

### Output:

```
Double of 5: 10
Triple of 5: 15
```

### Explanation:

- In this example, we define a delegate `SimpleOperation` representing methods that take an integer parameter and return void.
- We create an instance of the delegate `operations` and multicast two methods to it: `DoubleValue` and `TripleValue`.
- When we invoke the delegate `operations`, it sequentially invokes both methods that were multicast to it.
- The output shows that both methods are invoked in the order they were added to the delegate, doubling and tripling the input value `5` respectively.

### Summary:

- Multicasting of delegates in C# allows you to combine multiple methods into a single delegate instance.
- You can multicast methods to a delegate using the `+=` operator, and they will be invoked sequentially when the delegate is invoked.
- Multicast delegates provide a convenient way to perform multiple operations through a single delegate invocation, useful in scenarios such as event handling and callback mechanisms.

## **Predicate Delegate:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

The `Predicate` delegate in C# is a built-in delegate type defined in the .NET Framework's `System` namespace. It represents a method that takes one input parameter and returns a Boolean value, typically used to determine whether an object meets a specific condition.

### Example:

Let's create a simple example using the `Predicate` delegate to filter even numbers from a list.

```csharp
using System;
using System.Collections.Generic;

public class Program
{
    public static void Main(string[] args)
    {
        List<int> numbers = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

        // Predicate method to check if a number is even
        Predicate<int> isEven = num => num % 2 == 0;

        // Filter even numbers using Predicate delegate
        List<int> evenNumbers = numbers.FindAll(isEven);

        // Print even numbers
        Console.WriteLine("Even numbers:");
        foreach (var num in evenNumbers)
        {
            Console.WriteLine(num);
        }
    }
}
```

### Output:

```
Even numbers:
2
4
6
8
10
```

In this example:

- We declare a `Predicate<int>` delegate named `isEven`, which represents a method that takes an integer parameter and returns a Boolean value indicating whether the number is even.
- We use a lambda expression to define the condition for even numbers (i.e., `num % 2 == 0`).
- We use the `FindAll` method of the `List<T>` class to filter even numbers from the `numbers` list based on the condition specified by the `isEven` predicate.
- Finally, we print the even numbers using a `foreach` loop.

### Benefits of using Predicate Delegate:

1. **Encapsulation**: The use of the `Predicate` delegate allows us to encapsulate the condition for filtering elements, promoting cleaner and more modular code.
2. **Flexibility**: By using a delegate, we can easily change the filtering condition without modifying the calling code.
3. **Reusability**: Since the filtering logic is encapsulated in a separate method, it can be reused in multiple places within the codebase.
4. **Separation of Concerns**: Using a delegate separates the concerns of filtering logic from the code that performs the filtering operation, enhancing maintainability and readability.

### Summary:

The `Predicate` delegate in C# provides a flexible and reusable way to define conditions for filtering elements in collections. It promotes encapsulation, flexibility, reusability, and separation of concerns in codebases, leading to cleaner and more maintainable code.

## **Func Delegate:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

The `Func` delegate in C# is a generic delegate type defined in the `System` namespace. It represents a method that takes zero or more input parameters and returns a value of a specified type. The last type parameter of the `Func` delegate represents the return type, while the preceding type parameters represent the input parameter types.

### Example:

Let's create a simple example using the `Func` delegate to calculate the area of a circle.

```csharp
using System;

public class Program
{
    public static void Main(string[] args)
    {
        // Define a Func delegate to calculate area
        Func<double, double> calculateArea = radius => Math.PI * Math.Pow(radius, 2);

        // Calculate area of a circle with radius 5
        double radius = 5;
        double area = calculateArea(radius);

        Console.WriteLine($"Area of circle with radius {radius} = {area:F2}");
    }
}
```

### Output:

```
Area of circle with radius 5 = 78.54
```

### Explanation:

- In this example, we declare a `Func<double, double>` delegate named `calculateArea`, representing a method that takes a `double` parameter (radius) and returns a `double` value (area).
- We use a lambda expression to define the calculation of the area of a circle (`Math.PI * Math.Pow(radius, 2)`).
- We then invoke the `calculateArea` delegate with a radius value of 5, and it calculates the area of the circle.
- Finally, we print the calculated area with two decimal places using the `Console.WriteLine` method.

### Summary:

- The `Func` delegate in C# allows you to define and use functions with a specified input parameter type(s) and return type.
- It is a generic delegate with one or more type parameters representing the input parameter types and the return type.
- `Func` delegates are commonly used in scenarios where you need to define and pass functions as parameters to other methods, such as LINQ queries, functional programming, and asynchronous programming.
- The `Func` delegate simplifies the syntax for defining and using functions, making it easier to work with higher-order functions and functional programming concepts in C#.

## **Action Delegate:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

The `Action` delegate in C# is a generic delegate type defined in the `System` namespace. It represents a method that takes zero or more input parameters and does not return a value. The `Action` delegate simplifies the syntax for defining and using methods that perform actions or side effects without returning a value.

### Example:

Let's create a simple example using the `Action` delegate to print a message to the console.

```csharp
using System;

public class Program
{
    public static void Main(string[] args)
    {
        // Define an Action delegate to print a message
        Action<string> printMessage = message => Console.WriteLine(message);

        // Invoke the Action delegate to print a message
        printMessage("Hello, world!");
    }
}
```

### Output:

```
Hello, world!
```

### Explanation:

- In this example, we declare an `Action<string>` delegate named `printMessage`, representing a method that takes a `string` parameter (message) and does not return a value.
- We use a lambda expression to define the action of printing the message to the console (`Console.WriteLine(message)`).
- We then invoke the `printMessage` delegate with the message "Hello, world!", and it prints the message to the console.
- Finally, the message "Hello, world!" is displayed in the console output.

### Summary:

- The `Action` delegate in C# is used to represent methods that perform actions or side effects without returning a value.
- It is a generic delegate with one or more type parameters representing the input parameter types (if any).
- `Action` delegates are commonly used in scenarios where you need to define and pass methods as parameters to other methods, such as event handling, asynchronous programming, and functional programming.
- The `Action` delegate simplifies the syntax for defining and using methods that perform actions, making it easier to work with side-effecting functions and procedures in C#.

## **Func Vs Action Vs Predicate Delegates:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/7%20-%20Delegates.md#delegates-)

Below is a detailed comparison of `Func`, `Action`, and `Predicate` delegates in tabular form:

| Feature                      | Func                                              | Action                                          | Predicate                                       |
|------------------------------|---------------------------------------------------|-------------------------------------------------|-------------------------------------------------|
| Delegate Type                | Generic delegate representing a function         | Generic delegate representing an action         | Generic delegate representing a predicate       |
| Number of Type Parameters    | One or more, last one represents return type     | One or more, last one does not represents return type    | One or more, last one represents return type boolean    |
| Return Type                  | Required                                          | Not applicable                                  | Required (Boolean)                              |
| Input Parameters             | Zero or more                                       | Zero or more                                    | Zero or more                                    |
| Purpose                      | Used for methods that return a value             | Used for methods that do not return a value     | Used for methods that return a Boolean result   |
| Common Use Cases             | Function composition, LINQ queries               | Event handling, callback mechanisms            | Filtering collections, LINQ queries             |
| Example                      | `Func<int, int, int>`                             | `Action<string>`                                 | `Predicate<int>`                                |

### Summary:

- **Func Delegate**: Used for methods that return a value. It can have one or more input parameters and a return type. Commonly used for function composition and LINQ queries.
- **Action Delegate**: Used for methods that perform an action or side effect without returning a value. It can have one or more input parameters but no return type. Commonly used for event handling and callback mechanisms.
- **Predicate Delegate**: Used for methods that return a Boolean result, typically used for filtering collections or defining conditions. It can have one or more input parameters and must return a Boolean value. Commonly used in LINQ queries and filtering scenarios.

Each of these delegates serves a specific purpose and provides flexibility in different programming scenarios. Depending on whether you need a method that returns a value, performs an action, or evaluates a condition, you can choose the appropriate delegate type.
