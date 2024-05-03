# Control Statement ❤🍕

**Links:**

- [Decision Making](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#decision-making-)
    - [If Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#scenario-1-simple-if-statement-)
    - [If-Else Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#scenario-2-if-else-statement-)
    - [If-Else If-Else Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#scenario-3-if-else-if-else-statement-)
    - [Switch Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#scenario-4-switch-statement-)
    - [Nested Switch Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#scenario-5-nested-switch-statement-)
- [Loops in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#loops-in-c-)
    - [For Loop](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#1-for-loop-)
    - [While Loop](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#2-while-loop-)
    - [Do-While Loop](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#3-do-while-loop-)
    - [Foreach Loop](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#4-foreach-loop-)
- [for Vs foreach](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#for-vs-foreach-)
- [Jump Statements](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#jump-statements-)
    - [Break Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#1-break-statement-)
    - [Continue Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#2-continue-statement-)
    - [Return Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#3-return-statement-)
    - [Goto Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#4-goto-statement-)
    - [Throw Statement](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#5-throw-statement-)


## **Decision Making:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

Decision making in C# refers to the ability to execute different blocks of code based on certain conditions. This is achieved using conditional statements such as `if`, `else`, `else if`, and `switch`. These statements allow you to control the flow of your program based on the evaluation of expressions or variables. Let's explore some scenarios and examples to understand how decision making works in C#:

### Scenario 1: Simple If Statement [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `if` statement is a fundamental decision-making statement that allows you to execute a block of code if a specified condition evaluates to true. It can also be followed by an optional `else` block to execute code when the condition is false.

```csharp
using System;

class Program
{
    static void Main()
    {
        int number = 10;

        if (number > 0)
        {
            Console.WriteLine("Number is positive.");
        }
    }
}
```

**Output:**  
```
Number is positive.
```

In this example:
- We have a variable `number` with a value of 10.
- The `if` statement checks if the value of `number` is greater than 0.
- Since the condition is true (`10 > 0`), the statement inside the `if` block is executed, printing "Number is positive."

### Scenario 2: If-Else Statement [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `else if` statement is an extension of the `if` statement, allowing you to test multiple conditions sequentially. It is used when you have multiple conditions to evaluate, each with its corresponding block of code to execute.

```csharp
using System;

class Program
{
    static void Main()
    {
        int number = -5;

        if (number > 0)
        {
            Console.WriteLine("Number is positive.");
        }
        else
        {
            Console.WriteLine("Number is not positive.");
        }
    }
}
```

**Output:**  
```
Number is not positive.
```

In this example:
- We have a variable `number` with a value of -5.
- The `if` condition checks if the value of `number` is greater than 0. Since it's not (`-5 > 0` is false), the code inside the `else` block is executed, printing "Number is not positive."

### Scenario 3: If-Else If-Else Statement [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

```csharp
using System;

class Program
{
    static void Main()
    {
        int number = 0;

        if (number > 0)
        {
            Console.WriteLine("Number is positive.");
        }
        else if (number < 0)
        {
            Console.WriteLine("Number is negative.");
        }
        else
        {
            Console.WriteLine("Number is zero.");
        }
    }
}
```

**Output:**  
```
Number is zero.
```

In this example:
- We have a variable `number` with a value of 0.
- The `if` condition checks if the value of `number` is greater than 0. Since it's not (`0 > 0` is false), it moves to the `else if` block and checks if the value is less than 0. Again, it's not (`0 < 0` is false), so it executes the code inside the `else` block, printing "Number is zero."

### Scenario 4: Switch Statement [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `switch` statement provides a convenient way to execute different blocks of code based on the value of an expression or variable. It evaluates the expression once and then matches the value of the expression to one of several possible `case` labels, executing the corresponding block of code.

```csharp
using System;

class Program
{
    static void Main()
    {
        char grade = 'B';

        switch (grade)
        {
            case 'A':
                Console.WriteLine("Excellent!");
                break;
            case 'B':
                Console.WriteLine("Good!");
                break;
            case 'C':
                Console.WriteLine("Fair!");
                break;
            default:
                Console.WriteLine("Needs Improvement!");
                break;
        }
    }
}
```

**Output:**  
```
Good!
```

In this example:
- We have a variable `grade` with a value of 'B'.
- The `switch` statement checks the value of `grade` against different cases. Since it matches the case `'B'`, it executes the code inside that case, printing "Good!".

### Scenario 5: Nested Switch Statement [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

```csharp
using System;

class Program
{
    static void Main()
    {
        char department = 'M';
        char category = 'E';

        switch (department)
        {
            case 'I':
                Console.WriteLine("Inside the IT department:");
                switch (category)
                {
                    case 'S':
                        Console.WriteLine("Software Development");
                        break;
                    case 'N':
                        Console.WriteLine("Networking");
                        break;
                    default:
                        Console.WriteLine("Other IT Services");
                        break;
                }
                break;
            case 'M':
                Console.WriteLine("Inside the Marketing department:");
                switch (category)
                {
                    case 'A':
                        Console.WriteLine("Advertising");
                        break;
                    case 'P':
                        Console.WriteLine("Promotions");
                        break;
                    default:
                        Console.WriteLine("Other Marketing Services");
                        break;
                }
                break;
            default:
                Console.WriteLine("Other Departments");
                break;
        }
    }
}
```

**Output:**  
```
Inside the Marketing department:
Other Marketing Services
```

In this example:
- We have two variables `department` and `category` representing department and category codes.
- The outer `switch` statement checks the value of `department`.
- Depending on the value of `department`, it enters one of the nested `switch` statements.
- The nested `switch` statements check the value of `category` within each department.
- Depending on the value of `category`, it executes the corresponding case block.
- In this case, since the `department` is 'M' (Marketing) and the `category` is 'E', it executes the default case inside the nested switch statement for the Marketing department, printing "Other Marketing Services".

## **Loops in c#** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

In C#, loops are used to execute a block of code repeatedly until a specified condition is met. There are several types of loops available, including `for`, `while`, `do-while`, and `foreach`, each serving different purposes. Let's explore each type with scenarios, examples, and outputs:

### 1. For Loop: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `for` loop is commonly used when you know the number of iterations in advance. It consists of three parts: initialization, condition, and iteration. These parts are specified within the parentheses `()` of the loop declaration. The loop body is executed as long as the condition evaluates to true.

**Example: Printing numbers from 1 to 5**

```csharp
using System;

class Program
{
    static void Main()
    {
        for (int i = 1; i <= 5; i++)
        {
            Console.WriteLine(i);
        }
    }
}
```

**Output:**
```
1
2
3
4
5
```

### 2. While Loop: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `while` loop repeats a block of code as long as a specified condition is true. Unlike the `for` loop, the initialization and iteration steps are performed outside the loop declaration. This loop type is useful when the number of iterations is not known in advance and depends on the evaluation of a condition.

**Example: Summing numbers until the sum exceeds 100**

```csharp
using System;

class Program
{
    static void Main()
    {
        int sum = 0;
        int i = 1;

        while (sum <= 100)
        {
            sum += i;
            i++;
        }

        Console.WriteLine($"Sum: {sum}");
    }
}
```

**Output:**
```
Sum: 105
```

### 3. Do-While Loop: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

Similar to the `while` loop, the `do-while` loop repeats a block of code based on a specified condition. However, it ensures that the loop body is executed at least once, even if the condition is false initially. This can be helpful when you want to execute a block of code before checking the loop condition.

**Example: Taking input until a valid number is entered**

```csharp
using System;

class Program
{
    static void Main()
    {
        int number;

        do
        {
            Console.WriteLine("Enter a positive number:");
        } while (!int.TryParse(Console.ReadLine(), out number) || number <= 0);

        Console.WriteLine($"You entered: {number}");
    }
}
```

### 4. Foreach Loop: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `foreach` loop simplifies iteration over elements in a collection, such as arrays, lists, or other enumerable types. It automatically iterates over each element in the collection, assigning the current element to a loop variable for processing. This loop type is particularly convenient for working with collections without needing to manage loop counters or indices manually.

**Example: Iterating over an array**

```csharp
using System;

class Program
{
    static void Main()
    {
        int[] numbers = { 1, 2, 3, 4, 5 };

        foreach (int number in numbers)
        {
            Console.WriteLine(number);
        }
    }
}
```

**Output:**
```
1
2
3
4
5
```

These examples demonstrate how to use different types of loops in C# to execute code repeatedly under various conditions. Depending on the situation, you can choose the appropriate loop type to achieve the desired behavior in your program.

## **for Vs foreach:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

Here's a comparison of the `for` and `foreach` loops in C# presented in a tabular format, along with considerations regarding their performance:

| Feature                | `for` Loop                                        | `foreach` Loop                                    |
|------------------------|---------------------------------------------------|---------------------------------------------------|
| Purpose                | Used for iterating a fixed number of times.       | Used for iterating over elements in a collection.|
| Syntax                 | `for (initialization; condition; iteration)`       | `foreach (type variable in collection)`          |
| Usage                  | Requires manual management of loop variables.     | Automatically iterates over elements in a collection.|
| Performance            | Generally faster due to direct index access.      | May be slower, especially for large collections or value types.|
| Access to Collection   | Direct access to elements using indexing.         | Iterates over elements without direct index access.|
| Clarity and Readability| More verbose and requires explicit index management.| Concise and clearer, especially for collections.|

### Performance Considerations:

- **`for` Loop Performance**: 
  - Generally, the `for` loop may have better performance when iterating over arrays or collections with known lengths, as it allows direct access to elements using indexing.
  - It is suitable for scenarios where you need precise control over loop iteration or where performance optimization is critical.

- **`foreach` Loop Performance**: 
  - The `foreach` loop may have slightly lower performance compared to the `for` loop, especially for large collections or value types, due to its overhead in handling enumerators and lack of direct index access.
  - It is ideal for iterating over collections where index management is unnecessary or when working with collections that implement `IEnumerable` or `IEnumerable<T>` interfaces.

### Scenario Recommendations:

- **Use `for` Loop When**:
  - You need to iterate over arrays or collections with known lengths.
  - Precise control over loop iteration is required.
  - Performance optimization is a top priority, especially for large datasets.

- **Use `foreach` Loop When**:
  - You need to iterate over elements in a collection without concern for index management.
  - Working with collections that implement `IEnumerable` or `IEnumerable<T>` interfaces.
  - Clarity and readability are essential, especially when dealing with nested data structures or complex collections.

In summary, while both `for` and `foreach` loops have their advantages and performance considerations, the choice between them depends on factors such as the type of collection being iterated, the need for index management, and the importance of performance optimization in your application.

## **Jump Statements:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

Jump statements in C# are used to alter the flow of control in a program. They allow you to transfer the control from one part of the code to another based on certain conditions or requirements. There are three main types of jump statements: `break`, `continue`, and `return`. Let's explore each of them with examples, scenarios, and outputs:

### 1. Break Statement: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `break` statement is primarily used within loops (`for`, `while`, `do-while`) and `switch` statements to exit the loop or switch block prematurely. When encountered, the `break` statement immediately terminates the execution of the loop or switch block, and control transfers to the statement following the loop or switch.

**Example: Finding the first even number in a sequence**

```csharp
using System;

class Program
{
    static void Main()
    {
        int[] numbers = { 1, 3, 5, 6, 7, 9 };

        foreach (int number in numbers)
        {
            if (number % 2 == 0)
            {
                Console.WriteLine($"First even number found: {number}");
                break; // Exit the loop once an even number is found
            }
        }
    }
}
```

**Output:**
```
First even number found: 6
```

In this example, the `break` statement is used to exit the `foreach` loop as soon as the first even number is encountered in the array.

### 2. Continue Statement: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `continue` statement is used within loops (`for`, `while`, `do-while`) to skip the remaining code in the loop's body for the current iteration and proceed to the next iteration. When encountered, the `continue` statement bypasses the remaining code inside the loop and jumps back to the loop's condition check.

**Example: Skipping odd numbers in a sequence**

```csharp
using System;

class Program
{
    static void Main()
    {
        int[] numbers = { 1, 2, 3, 4, 5, 6 };

        foreach (int number in numbers)
        {
            if (number % 2 != 0)
            {
                continue; // Skip odd numbers
            }
            Console.WriteLine($"Even number found: {number}");
        }
    }
}
```

**Output:**
```
Even number found: 2
Even number found: 4
Even number found: 6
```

In this example, the `continue` statement is used to skip printing odd numbers and proceed to the next iteration of the `foreach` loop.

### 3. Return Statement: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `return` statement is used within methods to exit the method prematurely and return a value (if the method has a return type) to the caller. When encountered, the `return` statement immediately exits the method's execution, and control returns to the calling code with the specified return value (if any).

**Example: Checking if a number is prime**

```csharp
using System;

class Program
{
    static bool IsPrime(int number)
    {
        if (number <= 1)
        {
            return false; // Exit early if number is less than or equal to 1
        }

        for (int i = 2; i <= Math.Sqrt(number); i++)
        {
            if (number % i == 0)
            {
                return false; // Exit early if number is divisible by any other number
            }
        }

        return true; // Return true if number is prime
    }

    static void Main()
    {
        int num = 11;
        Console.WriteLine($"Is {num} prime? {IsPrime(num)}");
    }
}
```

**Output:**
```
Is 11 prime? True
```

In this example, the `return` statement is used to exit the `IsPrime` method as soon as it determines whether the number is prime or not, without continuing the loop unnecessarily.

### 4. Goto Statement: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `goto` statement allows transferring the control of the program to a labeled statement within the same method or block. While `goto` provides a way to change the flow of control, its usage is generally discouraged due to its potential to create spaghetti code and decrease code readability and maintainability.

**Example: Using Goto to Handle Errors**

```csharp
using System;

class Program
{
    static void Main()
    {
        int value = 10;

        if (value < 0)
        {
            goto ErrorHandler;
        }

        Console.WriteLine($"Value is: {value}");
        return;

        ErrorHandler:
        Console.WriteLine("Error: Value cannot be negative");
    }
}
```

**Output:**
```
Value is: 10
```

In this example, the `goto` statement is used to transfer the control to the `ErrorHandler` label if the value is negative. The code inside the `ErrorHandler` block is then executed to handle the error condition.

### 5. Throw Statement: [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/3%20-%20ControlStatement.md#control-statement-)

The `throw` statement is used to explicitly raise an exception during the execution of a program. It is typically used to signal exceptional conditions or errors that cannot be handled within the current context and need to be propagated to higher-level error-handling code.

**Example: Throwing an Exception**

```csharp
using System;

class Program
{
    static void ValidateNumber(int number)
    {
        if (number < 0)
        {
            throw new ArgumentException("Number cannot be negative");
        }
    }

    static void Main()
    {
        try
        {
            ValidateNumber(-5);
            Console.WriteLine("Number is valid");
        }
        catch (ArgumentException ex)
        {
            Console.WriteLine($"Error: {ex.Message}");
        }
    }
}
```

**Output:**
```
Error: Number cannot be negative
```

In this example, the `throw` statement is used inside the `ValidateNumber` method to raise an `ArgumentException` if the number is negative. When the exception is thrown, the program flow transfers to the nearest `catch` block where the exception is handled.


Let's provide more detailed explanations for each jump statement:

ions.
- Exiting a method early if a specific condition cannot be met or an error occurs.
