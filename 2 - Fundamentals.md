# Fundamentals ❤🍕

**Links:**

- [C# Identifier](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#c-identifier-)
- [Data Types](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#data-types-)
- [Data Variables](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#data-variables-)
- [Types of Variables](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#types-of-variables-)
- [Instance variable Vs Static variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#instance-variable-vs-static-variable-)
- [Constants variable Vs Read-Only variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#constants-variable-vs-read-only-variable-)
- [Var - Implicitely typed variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#var---implicitely-typed-variable-)
- [Dynamic Type](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#dynamic-type-)
- [Var Vs Dynamic Type](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#var-vs-dynamic-type-)
- [Scope of Variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#scope-of-variable-)
- [Access Modifiers](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#access-modifiers-)
- [Literals in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#literals-in-c-)
- [Opertors in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#opertors-in-c-)
- [Assignment Operators in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#assignment-operators-in-c-)
- [Boxing Vs Unboxing](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#boxing-vs-unboxing-)
- [Params in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#params-in-c-)
- [Type Casting in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#type-casting-in-c-)
- [Enumeration in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#enumeration-in-c-)
- [Properties in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#properties-in-c-)
- [Get Accessor & Set Accessor](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#get-accessor--set-accessor-)
- [Nullable types](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#nullable-types-)
- [Structures in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#structures-in-c-)
- [Static Keyword in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#static-keyword-in-c-)
- [Is vs As operator keyword in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#is-vs-as-operator-keyword-in-c-)
- [typeof vs GetType Operator](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#typeof-vs-gettype-operator-)
- [ref in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#ref-in-c-)

## **C# Identifier:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, identifiers are names used to identify variables, methods, classes, namespaces, and other programming elements within a C# program. Identifiers play a crucial role in coding because they provide a way to refer to different elements and make the code readable and understandable. Here are the main rules and characteristics of C# identifiers:

1. **Rules for Naming Identifiers**:
   - Identifiers in C# must adhere to the following rules:
     - Can consist of letters, digits, and underscores (`_`).
     - Must begin with a letter or an underscore (`_`).
     - Cannot contain whitespace characters or special symbols (such as `$`, `#`, `%`, etc.), except for underscores (`_`).
     - Cannot be a reserved keyword or type name in C#.
     - Can have any length, but only the first 512 characters are significant.
     - Are case-sensitive, meaning uppercase and lowercase letters are considered distinct.

2. **Conventions for Naming Identifiers**:
   - While C# allows a wide range of characters and naming conventions for identifiers, it's a common practice to follow certain conventions for readability and maintainability:
     - Use descriptive and meaningful names that reflect the purpose or functionality of the identifier.
     - Use camelCase for local variables, method parameters, and private fields (`myVariable`, `myParameter`, `myPrivateField`).
     - Use PascalCase for class names, method names, properties, namespaces, and public fields or properties (`MyClass`, `MyMethod`, `MyProperty`, `MyNamespace`, `MyPublicField`).
     - Avoid using underscores (`_`) as prefixes or suffixes, except for private fields (`_myPrivateField`).
     - Use abbreviations sparingly and consistently.
     - Choose concise but descriptive names to enhance code readability.

3. **Examples**:
   - Valid identifiers:
     ```csharp
     int myVariable;
     string MyMethod(int myParameter)
     {
         MyClass myObject = new MyClass();
         return myObject.MyProperty;
     }
     ```

   - Invalid identifiers (due to violating naming rules or conventions):
     ```csharp
     int 123myVariable; // Identifier cannot begin with a digit
     string My Method(int myParameter) // Identifier cannot contain whitespace
     string $myVariable; // Identifier cannot contain special symbols other than underscores
     string MY_VARIABLE; // Identifier conventions typically use camelCase or PascalCase
     ```

In summary, identifiers in C# are names used to refer to various programming elements within a C# program, such as variables, methods, classes, and namespaces. They must adhere to certain rules and conventions to ensure readability, maintainability, and compliance with C# language specifications.

## **Data Types:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Sure, here's a detailed explanation of the main data types in C# presented in tabular form:

| Data Type  | Description                                                | Size (bits)  | Range                                                     | Default Value    | .NET Framework Type       |
|------------|------------------------------------------------------------|--------------|-----------------------------------------------------------|------------------|---------------------------|
| `bool`     | Represents a Boolean value (true or false).               | 8 (1 byte)   | `true` or `false`                                         | `false`          | `System.Boolean`          |
| `byte`     | Represents an unsigned 8-bit integer.                      | 8 (1 byte)   | 0 to 255                                                  | 0                | `System.Byte`             |
| `sbyte`    | Represents a signed 8-bit integer.                         | 8 (1 byte)   | -128 to 127                                               | 0                | `System.SByte`            |
| `short`    | Represents a signed 16-bit integer.                        | 16 (2 bytes) | -32,768 to 32,767                                         | 0                | `System.Int16`            |
| `ushort`   | Represents an unsigned 16-bit integer.                     | 16 (2 bytes) | 0 to 65,535                                                | 0                | `System.UInt16`           |
| `int`      | Represents a signed 32-bit integer.                        | 32 (4 bytes) | -2,147,483,648 to 2,147,483,647                           | 0                | `System.Int32`            |
| `uint`     | Represents an unsigned 32-bit integer.                     | 32 (4 bytes) | 0 to 4,294,967,295                                        | 0                | `System.UInt32`           |
| `long`     | Represents a signed 64-bit integer.                        | 64 (8 bytes) | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807   | 0                | `System.Int64`            |
| `ulong`    | Represents an unsigned 64-bit integer.                     | 64 (8 bytes) | 0 to 18,446,744,073,709,551,615                           | 0                | `System.UInt64`           |
| `float`    | Represents a single-precision floating-point number.       | 32 (4 bytes) | -3.402823e38 to 3.402823e38                               | 0.0              | `System.Single`           |
| `double`   | Represents a double-precision floating-point number.       | 64 (8 bytes) | -1.79769313486232e308 to 1.79769313486232e308             | 0.0              | `System.Double`           |
| `decimal`  | Represents a decimal floating-point number.                | 128 (16 bytes)| (-7.9 x 10^28 to 7.9 x 10^28) / (10^(0 to 28))            | 0.0              | `System.Decimal`          |
| `char`     | Represents a single Unicode character.                     | 16 (2 bytes) | U+0000 to U+FFFF                                          | `'\0'` (null)   | `System.Char`             |
| `string`   | Represents a sequence of characters.                       | -            | -                                                         | `null`           | `System.String`           |
| `object`   | Represents any type in C#.                                | -            | -                                                         | `null`           | `System.Object`           |

- **Size (bits)**: Indicates the number of bits used to represent the data type in memory.
- **Range**: Defines the minimum and maximum values that can be stored in the data type.
- **Default Value**: Represents the initial value assigned to a variable of the data type if no explicit value is provided.

These data types cover a wide range of numeric, textual, and general-purpose values used in C# programming. Each data type has its own characteristics and usage scenarios, providing flexibility and precision in representing different kinds of data.

## **Data Variables:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, data variables are used to store and manipulate data values within a program. A variable is a named storage location in memory that holds a value of a specific data type. Here are examples of data variables and their types in C#:

### Examples of Data Variables:

1. **Integer Variable**:
   - Stores whole numbers without decimal points.
   ```csharp
   int age = 25;
   ```

2. **Floating-Point Variable**:
   - Stores numbers with decimal points.
   ```csharp
   double height = 5.8;
   ```

3. **Boolean Variable**:
   - Stores true or false values.
   ```csharp
   bool isStudent = true;
   ```

4. **Character Variable**:
   - Stores single characters.
   ```csharp
   char grade = 'A';
   ```

5. **String Variable**:
   - Stores sequences of characters.
   ```csharp
   string name = "John Doe";
   ```

6. **Array Variable**:
   - Stores multiple values of the same type in a collection.
   ```csharp
   int[] numbers = { 1, 2, 3, 4, 5 };
   ```

7. **Object Variable**:
   - Stores references to objects of any type.
   ```csharp
   object obj = "Hello";
   ```

### Types of Data Variables:

1. **Value Types**:
   - Hold the data value directly within their own memory space.
   - Examples: `int`, `double`, `bool`, `char`, etc.
   - Values of value types are copied when passed to methods or assigned to other variables.

2. **Reference Types**:
   - Hold a reference to the memory location where the data is stored.
   - Examples: `string`, arrays, classes, interfaces, delegates, etc.
   - Values of reference types are passed by reference, meaning the memory location is shared between variables.

### Example Code:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declaring and initializing variables
        int age = 25;
        double height = 5.8;
        bool isStudent = true;
        char grade = 'A';
        string name = "John Doe";
        int[] numbers = { 1, 2, 3, 4, 5 };
        object obj = "Hello";

        // Outputting variable values
        Console.WriteLine("Age: " + age);
        Console.WriteLine("Height: " + height);
        Console.WriteLine("Is Student: " + isStudent);
        Console.WriteLine("Grade: " + grade);
        Console.WriteLine("Name: " + name);
        Console.WriteLine("Numbers: " + string.Join(", ", numbers));
        Console.WriteLine("Object: " + obj);
    }
}
```

In this example, various types of data variables are declared and initialized with values. Then, their values are printed to the console. Each variable holds a specific type of data, such as integers, floating-point numbers, boolean values, characters, strings, arrays, and objects.

## **Types of Variables:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, variables can be categorized into different types based on various factors such as scope, lifetime, and storage. Here are the main types of variables in C#:

### 1. Local Variables:
   - **Definition**: Variables declared within a method or a block of code.
   - **Scope**: Limited to the block or method in which they are declared.
   - **Lifetime**: Exist only as long as the block or method is executing.
   - **Example**:
     ```csharp
     void MyMethod()
     {
         int x = 10; // Local variable
     }
     ```

### 2. Instance Variables (Fields):
   - **Definition**: Variables declared within a class but outside any method.
   - **Scope**: Available to all methods within the class.
   - **Lifetime**: Exist as long as the object (instance of the class) exists.
   - **Example**:
     ```csharp
     class MyClass
     {
         int x; // Instance variable
     }
     ```

### 3. Static Variables (Class Variables):
   - **Definition**: Variables declared with the `static` keyword within a class.
   - **Scope**: Available to all instances of the class.
   - **Lifetime**: Exist as long as the program is running or until explicitly modified.
   - **Example**:
     ```csharp
     class MyClass
     {
         static int count = 0; // Static variable
     }
     ```

### 4. Constant Variables:
   - **Definition**: Variables declared with the `const` keyword.
   - **Scope**: Available in the same scope where they are declared.
   - **Lifetime**: Exist for the entire duration of the program.
   - **Value**: Cannot be changed once initialized.
   - **Example**:
     ```csharp
     const double Pi = 3.14; // Constant variable
     ```

### 5. Readonly Variables:
   - **Definition**: Variables declared with the `readonly` keyword.
   - **Scope**: Available in the same scope where they are declared.
   - **Lifetime**: Exist for the entire duration of the program.
   - **Value**: Can only be assigned a value at the time of declaration or in the constructor.
   - **Example**:
     ```csharp
     readonly int MaxValue = 100; // Readonly variable
     ```

### 6. Parameters (Method Parameters):
   - **Definition**: Variables used to pass data into methods.
   - **Scope**: Limited to the method in which they are declared.
   - **Lifetime**: Exist as long as the method is executing.
   - **Example**:
     ```csharp
     void MyMethod(int x) // Parameter variable
     {
         // Code
     }
     ```

These are the main types of variables in C#, each serving different purposes and having specific characteristics regarding scope, lifetime, and storage. Understanding the types of variables is crucial for effective program design and memory management in C#.

## **Instance variable Vs Static variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

| Aspect                 | Instance Variable                         | Static Variable                                |
|------------------------|-------------------------------------------|------------------------------------------------|
| Declaration            | Declared within a class, but outside any method. | Declared with the `static` keyword within a class. |
| Scope                  | Belongs to an instance of the class.      | Belongs to the class itself rather than to any instance. |
| Accessibility          | Accessed using an instance of the class.   | Accessed using the class name directly or via an instance. |
| Memory Allocation      | Memory allocated separately for each instance of the class. | Memory allocated only once for all instances of the class. |
| Lifetime               | Exist as long as the instance of the class exists. | Exist as long as the program is running or until explicitly modified. |
| Initialization         | Initialized when an instance of the class is created. | Initialized when the class is loaded into memory. |

In summary, instance variables are specific to each instance of a class and are accessed through instances of the class, whereas static variables belong to the class itself and are accessed directly using the class name. Instance variables have separate memory allocations for each instance, while static variables have a single memory allocation shared across all instances of the class.

## **Constants variable Vs Read-Only variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Here's a comparison of constant variables and readonly variables in C# presented in a tabular form:

| Aspect                | Constant Variables                      | Readonly Variables                           |
|-----------------------|-----------------------------------------|----------------------------------------------|
| Declaration           | Declared using the `const` keyword.     | Declared using the `readonly` keyword.       |
| Value Assignment      | Must be assigned a value at declaration. | Can be assigned a value at declaration or in the constructor. |
| Initialization       | Initialized at compile time.             | Initialized at runtime.                      |
| Value Modification   | Cannot be changed after initialization. | Can only be assigned a value at declaration or in the constructor, but its value can be modified by the constructor only. |
| Scope                 | Available in the same scope where they are declared. | Available in the same scope where they are declared. |
| Lifetime              | Exist for the entire duration of the program. | Exist for the entire duration of the program. |

In summary, constant variables are assigned a value at compile time and cannot be changed thereafter, while readonly variables can be assigned a value either at declaration or in the constructor, but their value can be modified only in the constructor. Both constant and readonly variables are available for the entire duration of the program and have the same scope.

## **Var - Implicitely typed variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Implicitly Typed Local Variables, introduced in C# 3.0, allow you to declare variables without explicitly specifying their data types. Instead, the compiler infers the data type based on the value assigned to the variable at the time of initialization. Here's an explanation of var with examples and scenarios:

### Syntax:
```csharp
var variableName = value;
```

### Example 1: Simple Usage
```csharp
var age = 25;
var name = "John";
```
In this example, the compiler infers that `age` is of type `int` and `name` is of type `string` based on the assigned values.

### Example 2: Complex Data Types
```csharp
var numbers = new int[] { 1, 2, 3, 4, 5 };
var person = new { Name = "John", Age = 25 };
```
Here, `numbers` is inferred to be an array of integers, and `person` is inferred to be an anonymous type with `Name` and `Age` properties.

### Example 3: LINQ Queries
```csharp
var result = from num in numbers
             where num % 2 == 0
             select num;
```
In this scenario, `result` will be of type `IEnumerable<int>` based on the LINQ query's result.

### Example 4: Iterating Collections
```csharp
var countries = new List<string> { "USA", "UK", "Canada" };
foreach (var country in countries)
{
    Console.WriteLine(country);
}
```
Here, `country` is inferred as a `string` type based on the elements of the `countries` list.

### Example 5: LINQ to SQL Queries
```csharp
var dbContext = new MyDataContext();
var users = from user in dbContext.Users
            where user.Age > 18
            select user;
```
In this example, `users` will be inferred as an `IQueryable<User>` based on the LINQ to SQL query's result.

### Scenarios:
1. **Simplifying Code**: Var can simplify code, especially when the type is obvious from the right-hand side of the assignment.
2. **Anonymous Types**: Var is commonly used when working with anonymous types, as the type name is unknown.
3. **LINQ Queries**: Var is frequently used with LINQ queries to avoid explicitly specifying the data type of query results.
4. **Complex Initialization**: Var can be useful when initializing complex data types or when the type name is long or cumbersome to write.

### Considerations:
1. **Readability**: While var can improve code readability in certain scenarios, it should not be overused, especially when the type is not clear from the initialization value.
2. **Type Inference**: The compiler infers the type of var variables at compile time, so the actual type is known and enforced by the compiler.
3. **Maintainability**: Using var excessively may make the code harder to maintain, especially for developers who are not familiar with the codebase.

In summary, var provides a convenient way to declare variables without explicitly specifying their types, improving code readability and reducing redundancy in certain scenarios. However, it should be used judiciously to maintain code clarity and understandability.

## **Dynamic Type:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, the `dynamic` type was introduced in C# 4.0 as part of the dynamic language runtime (DLR) feature. It allows you to declare variables whose type is resolved at runtime rather than at compile time. With the `dynamic` type, you can defer type checking and binding until runtime, enabling scenarios such as late binding and interoperability with dynamic languages.

### Syntax:
```csharp
dynamic variableName = value;
```

### Features and Characteristics:

1. **Dynamic Binding**:
   - Unlike other types where binding and type checking occur at compile time, `dynamic` variables postpone these processes until runtime.
   - The type of a `dynamic` variable is determined at runtime based on the operations performed on it.

2. **Late Binding**:
   - `dynamic` enables late binding, allowing you to invoke members (methods, properties, fields, etc.) on objects without specifying their types at compile time.
   - Member resolution occurs at runtime based on the actual type of the object.

3. **Interoperability**:
   - `dynamic` is commonly used for interoperability with dynamic languages such as Python, JavaScript, and Ruby, where types are determined at runtime.

### Example:

```csharp
dynamic obj = GetDynamicObject(); // GetDynamicObject returns an object of unknown type

// Late binding - member resolution occurs at runtime
var result = obj.SomeMethod(); // SomeMethod may or may not exist on obj

// Dynamic typing - type resolution occurs at runtime
dynamic value = "Hello";
value = 10; // value changes its type from string to int
```

### Scenarios:

1. **COM Interop**:
   - When working with COM objects, where types are resolved dynamically, the `dynamic` type can simplify interoperability.

2. **Dynamic Languages Integration**:
   - `dynamic` is useful when interacting with dynamic languages like Python or JavaScript from C# code, where types are not known until runtime.

3. **Reflection and ExpandoObject**:
   - `dynamic` can be used with reflection or `ExpandoObject` to manipulate objects dynamically at runtime, providing flexibility in certain scenarios.

### Considerations:

1. **Performance Overhead**:
   - Using `dynamic` may incur a performance overhead compared to statically typed variables because of the additional runtime type checks and binding.

2. **Type Safety**:
   - Since type checking occurs at runtime, errors related to incorrect member invocations may only be detected during program execution.

3. **Debugging**:
   - Debugging code with `dynamic` variables can be more challenging since the types of these variables are not known at compile time.

In summary, the `dynamic` type in C# provides flexibility and interoperability by deferring type checking and binding until runtime. While it can be useful in certain scenarios, it should be used judiciously to balance flexibility with performance and maintainability considerations.

## **Var Vs Dynamic Type:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

| Aspect             | var                                  | dynamic                                   |
|--------------------|--------------------------------------|-------------------------------------------|
| Intitialization     | If the variable does not initialized it throw an error. | If the variable does not initialized it will not throw an error. |
| Type Inference     | Inferred at compile time based on the initialization value. | Type resolution deferred until runtime based on the operations performed on it. |
| Static/Dynamic Typing | Static typing; type is known at compile time. | Dynamic typing; type is resolved at runtime. |
| Usage              | Mainly used with statically typed language constructs. | Used for dynamic typing, late binding, and interoperability scenarios. |
| Type Safety        | Provides type safety at compile time. | May lead to runtime errors if used improperly, as type checking is deferred until runtime. |
| Performance        | No performance overhead, as it's just a syntactic sugar. | May incur a performance overhead due to runtime type checks and dynamic binding. |
| Debugging          | Easier to debug, as the type is known at compile time. | Can be more challenging to debug, as type resolution occurs at runtime. |

In summary, `var` is used for type inference at compile time, providing static typing and type safety, while `dynamic` allows for dynamic typing and late binding, deferring type resolution until runtime. The choice between `var` and `dynamic` depends on the specific requirements and constraints of the programming scenario.

## **Scope of Variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Certainly! Let's delve into each scope level in C#:

### 1. Class Level Scope:

- **Definition**: Variables declared within a class but outside any method or constructor.
- **Access**: Accessible to all methods and constructors within the class.
- **Lifetime**: Exist as long as the class exists.
- **Example**:
  ```csharp
  class MyClass
  {
      int classVar = 10; // Class level variable

      public void Method1()
      {
          Console.WriteLine(classVar); // Accessible within methods
      }

      public void Method2()
      {
          Console.WriteLine(classVar); // Accessible within methods
      }
  }
  ```

### 2. Method Level Scope:

- **Definition**: Variables declared within a method.
- **Access**: Limited to the method in which they are declared.
- **Lifetime**: Exist only as long as the method is executing.
- **Example**:
  ```csharp
  class MyClass
  {
      public void MyMethod()
      {
          int methodVar = 20; // Method level variable
          Console.WriteLine(methodVar); // Accessible within the method
      }
  }
  ```

### 3. Block Level Scope:

- **Definition**: Variables declared within a block of code, such as within loops, conditionals, or method bodies.
- **Access**: Limited to the block in which they are declared.
- **Lifetime**: Exist only within the block in which they are declared.
- **Example**:
  ```csharp
  class MyClass
  {
      public void MyMethod()
      {
          if (true)
          {
              int blockVar = 30; // Block level variable
              Console.WriteLine(blockVar); // Accessible within the block
          }
      }
  }
  ```

### Comparison:

- **Scope Hierarchy**:
  - Class level scope is the broadest, followed by method level scope, and then block level scope.
- **Visibility**:
  - Class level variables are visible to all methods within the class, method level variables are limited to the method, and block level variables are limited to the block in which they are declared.
- **Lifetime**:
  - Variables at each level have different lifetimes, depending on the duration of their enclosing scope.

### Use Cases:

- **Class Level Scope**: Used for variables that need to maintain state across multiple methods within a class.
- **Method Level Scope**: Used for temporary variables required for computation within a method.
- **Block Level Scope**: Used for variables that are only needed within a specific block of code, such as loop counters or temporary storage.

Understanding and correctly utilizing these scope levels in C# is crucial for writing maintainable and efficient code. Each scope level serves a distinct purpose and offers different levels of visibility and accessibility for variables within a program.

## **Access Modifiers:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Sure, let's delve into each access modifier in detail:

### 1. public:

- **Description**: Public members are accessible from any other class or assembly. They have the widest accessibility.
- **Usage**: Often used for members that need to be accessed from outside the class or assembly.
- **Example**:
  ```csharp
  public class MyClass
  {
      public int PublicVar;
      public void PublicMethod() { }
  }
  ```

### 2. private:

- **Description**: Private members are accessible only within the same class. They have the narrowest accessibility.
- **Usage**: Used to hide implementation details and restrict access to internal workings of a class.
- **Example**:
  ```csharp
  public class MyClass
  {
      private int PrivateVar;
      private void PrivateMethod() { }
  }
  ```

### 3. protected:

- **Description**: Protected members are accessible within the same class and its derived classes.
- **Usage**: Used to allow derived classes to access certain members while still restricting access to other classes.
- **Example**:
  ```csharp
  public class MyBaseClass
  {
      protected int ProtectedVar;
      protected void ProtectedMethod() { }
  }

  public class MyDerivedClass : MyBaseClass
  {
      void AnotherMethod()
      {
          ProtectedVar = 10; // Accessing protected member from derived class
          ProtectedMethod(); // Accessing protected method from derived class
      }
  }
  ```

### 4. internal:

- **Description**: Internal members are accessible within the same assembly.
- **Usage**: Used for members that should only be accessed within the same assembly but not from outside assemblies.
- **Example**:
  ```csharp
  internal class InternalClass
  {
      internal int InternalVar;
      internal void InternalMethod() { }
  }
  ```

### 5. protected internal:

- **Description**: Protected internal members are accessible within the same assembly and by derived classes, regardless of the assembly.
- **Usage**: Used when you want members to be accessible by derived classes and within the same assembly.
- **Example**:
  ```csharp
  public class MyBaseClass
  {
      protected internal int ProtectedInternalVar;
      protected internal void ProtectedInternalMethod() { }
  }

  public class MyDerivedClass : MyBaseClass
  {
      void AnotherMethod()
      {
          ProtectedInternalVar = 10; // Accessing protected internal member from derived class
          ProtectedInternalMethod(); // Accessing protected internal method from derived class
      }
  }
  ```

| Modifier             | Description                                      | Example                                   | Allows Access from Other Classes | Allows Access from Derived Classes | Allows Access from Same Assembly |
|----------------------|--------------------------------------------------|-------------------------------------------|-----------------------------------|------------------------------------|----------------------------------|
| `public`             | Accessible from any other class or assembly.    | `public class MyClass { }`                | Yes                               | Yes                                | Yes                              |
| `private`            | Accessible only within the same class.          | `private int myVar;`                      | No                                | No                                 | No                               |
| `protected`          | Accessible within the same class and its derived classes. | `protected void MyMethod() { }`         | No                                | Yes                                | Yes                              |
| `internal`           | Accessible within the same assembly.            | `internal class MyClass { }`              | Yes                               | No                                 | Yes                              |
| `protected internal` | Accessible within the same assembly and by derived classes, regardless of the assembly. | `protected internal void MyMethod() { }` | Yes                               | Yes                                | Yes                              |

Understanding these access modifiers is crucial for designing classes with proper encapsulation and controlling the visibility of class members in C#. Each modifier offers different levels of access, allowing you to specify the desired level of encapsulation and accessibility for your class members.

## **Literals in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, a literal represents a fixed value in your source code. Here's an explanation of various types of literals in C# along with examples and scenarios:

### 1. Numeric Literals:

- **Integer Literals**: Represent whole numbers without decimal points.
  - Example: `int myInt = 10;`
- **Floating-Point Literals**: Represent numbers with a decimal point.
  - Example: `float myFloat = 3.14f;`
- **Double Literals**: Similar to floating-point literals but with higher precision.
  - Example: `double myDouble = 3.14;`
- **Decimal Literals**: Represent precise decimal values with higher precision compared to floating-point literals.
  - Example: `decimal myDecimal = 3.14159m;`

   - Scenario: Calculations involving numbers.
   - Example: Computing the area of a rectangle using integer literals.
     ```csharp
     int length = 10;
     int width = 5;
     int area = length * width; // area = 50
     ```

### 2. Boolean Literals:

- **Boolean Literals**: Represent the values true or false.
  - Example: `bool myBool = true;`
    
    - Scenario: Conditional statements.
    - Example: Checking if a number is even or odd.
        ```csharp
        int number = 7;
        bool isEven = (number % 2 == 0); // false
        ```

### 3. Character Literals:

- **Character Literals**: Represent single characters enclosed in single quotes.
  - Example: `char myChar = 'A';`

   - Scenario: Processing individual characters.
   - Example: Converting a character to uppercase.
     ```csharp
     char lowercase = 'a';
     char uppercase = char.ToUpper(lowercase); // 'A'
     ```

### 4. String Literals:

- **String Literals**: Represent sequences of characters enclosed in double quotes.
  - Example: `string myString = "Hello, World!";`

   - Scenario: Storing and manipulating text.
   - Example: Concatenating strings.
     ```csharp
     string firstName = "John";
     string lastName = "Doe";
     string fullName = firstName + " " + lastName; // "John Doe"
     ```

### 5. Null Literal:

- **Null Literal**: Represents a null reference.
  - Example: `object myObject = null;`

   - Scenario: Representing absence of a value.
   - Example: Initializing reference types to null.
     ```csharp
     string address = null;
     ```
Literals in C# provide a way to represent fixed values directly within your code. They are fundamental to various programming tasks such as arithmetic calculations, conditional statements, string manipulation, and more. Understanding and correctly using literals is essential for writing clear, concise, and maintainable code in C#.

## **Opertors in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Sure, let's explore the various types of operators in C# along with examples and scenarios:

### 1. Arithmetic Operators:

- **Description**: Perform arithmetic operations such as addition, subtraction, multiplication, division, and modulus.
- **Examples**:
  ```csharp
  int a = 10;
  int b = 5;
  int sum = a + b;        // Addition
  int difference = a - b; // Subtraction
  int product = a * b;    // Multiplication
  int quotient = a / b;   // Division
  int remainder = a % b;  // Modulus
  ```

### 2. Relational Operators:

- **Description**: Compare two values and return a boolean result.
- **Examples**:
  ```csharp
  int x = 10;
  int y = 5;
  bool isEqual = x == y; // Equality
  bool isNotEqual = x != y; // Inequality
  bool isGreater = x > y; // Greater than
  bool isLess = x < y;    // Less than
  bool isGreaterOrEqual = x >= y; // Greater than or equal to
  bool isLessOrEqual = x <= y;    // Less than or equal to
  ```

### 3. Logical Operators:

- **Description**: Perform logical operations on boolean values.
- **Examples**:
  ```csharp
  bool condition1 = true;
  bool condition2 = false;
  bool result1 = condition1 && condition2; // Logical AND
  bool result2 = condition1 || condition2; // Logical OR
  bool result3 = !condition1; // Logical NOT
  ```

### 4. Assignment Operators:

- **Description**: Assign values to variables.
- **Examples**:
  ```csharp
  int x = 10;
  int y = 5;
  x += y; // Equivalent to: x = x + y;
  y -= x; // Equivalent to: y = y - x;
  ```

### 5. Unary Operators:

- **Description**: Operate on a single operand.
- **Examples**:
  ```csharp
  int a = 10;
  int b = -a; // Unary minus
  bool condition = true;
  bool negation = !condition; // Logical NOT
  ```

### 6. Increment and Decrement Operators:

- **Description**: Increase or decrease the value of a variable by one.
- **Examples**:
  ```csharp
  int counter = 0;
  counter++; // Increment by one
  counter--; // Decrement by one
  ```

### 7. Conditional Operator (Ternary Operator):

- **Description**: A ternary operator that evaluates a condition and returns one of two values based on the result.
- **Example**:
  ```csharp
  int x = 10;
  int y = 5;
  int result = (x > y) ? x : y; // If x is greater than y, result = x, otherwise result = y
  ```

### Scenarios:

1. **Arithmetic Operators**:
   - Scenario: Calculating total cost of items in a shopping cart.
   - Example: `totalCost = price * quantity;`

2. **Relational Operators**:
   - Scenario: Checking if a user's age is eligible for a discount.
   - Example: `isEligibleForDiscount = (age >= 60);`

3. **Logical Operators**:
   - Scenario: Implementing access control based on user permissions.
   - Example: `hasPermission = (isAdmin || isModerator);`

4. **Assignment Operators**:
   - Scenario: Updating a counter variable in a loop.
   - Example: `counter += 1;`

5. **Unary Operators**:
   - Scenario: Converting a positive number to negative.
   - Example: `negativeValue = -positiveValue;`

6. **Increment and Decrement Operators**:
   - Scenario: Updating a counter while iterating through a list.
   - Example: `index++;`

7. **Conditional Operator**:
   - Scenario: Determining the maximum value between two numbers.
   - Example: `maxValue = (x > y) ? x : y;`

Operators are essential for performing various operations in C# programming. Understanding and using them effectively is crucial for writing efficient and readable code.

## **Assignment Operators in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

### 1. Simple Assignment Operator `=`:

- **Description**: Assigns the value on the right-hand side to the variable on the left-hand side.
- **Example**:
  ```csharp
  int x = 10; // Assigns the value 10 to the variable x
  ```

### 2. Addition Assignment Operator `+=`:

- **Description**: Adds the value on the right-hand side to the current value of the variable and assigns the result back to the variable.
- **Example**:
  ```csharp
  int x = 5;
  x += 3; // Equivalent to: x = x + 3;
  // After this operation, x will have the value 8
  ```

### 3. Subtraction Assignment Operator `-=`:

- **Description**: Subtracts the value on the right-hand side from the current value of the variable and assigns the result back to the variable.
- **Example**:
  ```csharp
  int x = 10;
  x -= 4; // Equivalent to: x = x - 4;
  // After this operation, x will have the value 6
  ```

### 4. Multiplication Assignment Operator `*=`:

- **Description**: Multiplies the value on the right-hand side by the current value of the variable and assigns the result back to the variable.
- **Example**:
  ```csharp
  int x = 3;
  x *= 2; // Equivalent to: x = x * 2;
  // After this operation, x will have the value 6
  ```

### 5. Division Assignment Operator `/=`:

- **Description**: Divides the current value of the variable by the value on the right-hand side and assigns the result back to the variable.
- **Example**:
  ```csharp
  int x = 10;
  x /= 2; // Equivalent to: x = x / 2;
  // After this operation, x will have the value 5
  ```

### 6. Modulus Assignment Operator `%=`:

- **Description**: Computes the remainder of dividing the current value of the variable by the value on the right-hand side and assigns the result back to the variable.
- **Example**:
  ```csharp
  int x = 10;
  x %= 3; // Equivalent to: x = x % 3;
  // After this operation, x will have the value 1
  ```

### 7. Left Shift Assignment Operator `<<=`:

- **Description**: Shifts the bits of the left-hand operand to the left by a specified number of positions and assigns the result back to the left-hand operand.
- **Syntax**: `x <<= n` is equivalent to `x = x << n`, where `x` is the left-hand operand and `n` is the number of positions to shift.
- **Example**:
  ```csharp
  int x = 5;    // Binary: 0000 0101
  x <<= 2;      // Shift left by 2 positions
  // After this operation, x will have the value 20 (Binary: 0001 0100)
  ```

### 8. Right Shift Assignment Operator `>>=`:

- **Description**: Shifts the bits of the left-hand operand to the right by a specified number of positions and assigns the result back to the left-hand operand.
- **Syntax**: `x >>= n` is equivalent to `x = x >> n`, where `x` is the left-hand operand and `n` is the number of positions to shift.
- **Example**:
  ```csharp
  int x = 20;   // Binary: 0001 0100
  x >>= 2;      // Shift right by 2 positions
  // After this operation, x will have the value 5 (Binary: 0000 0101)
  ```

  #### Scenario:

  - **Scenario**: Converting units of measurement (e.g., from seconds to milliseconds) by shifting the binary representation of the value.
  - **Example**:
    ```csharp
    int seconds = 10;    // Value in seconds
    seconds <<= 10;      // Convert seconds to milliseconds (10 seconds = 10,000 milliseconds)
    ```

### 9. Bitwise AND `&`:

- **Description**: Performs a bitwise AND operation between corresponding bits of two operands.
- **Example**:
  ```csharp
  int a = 5;    // Binary: 0000 0101
  int b = 3;    // Binary: 0000 0011
  int result = a & b;  // Binary: 0000 0001
  // After this operation, result will have the value 1
  ```

### 10. Bitwise AND Assignment `&=`:

- **Description**: Performs a bitwise AND operation between corresponding bits of two operands and assigns the result back to the left-hand operand.
- **Example**:
  ```csharp
  int x = 10;     // Binary: 0000 1010
  int y = 6;      // Binary: 0000 0110
  x &= y;         // Binary: 0000 0010
  // After this operation, x will have the value 2
  ```

### 11. Bitwise Exclusive OR (XOR) `^`:

- **Description**: Performs a bitwise exclusive OR (XOR) operation between corresponding bits of two operands. Returns 1 if the bits are different, and 0 if they are the same.
- **Example**:
  ```csharp
  int a = 5;    // Binary: 0000 0101
  int b = 3;    // Binary: 0000 0011
  int result = a ^ b;  // Binary: 0000 0110
  // After this operation, result will have the value 6
  ```

### 12. Bitwise Inclusive OR `|`:

- **Description**: Performs a bitwise OR operation between corresponding bits of two operands.
- **Example**:
  ```csharp
  int a = 5;    // Binary: 0000 0101
  int b = 3;    // Binary: 0000 0011
  int result = a | b;  // Binary: 0000 0111
  // After this operation, result will have the value 7
  ```

  #### Scenario:

  - **Scenario**: Setting or clearing specific bits in a bit field.
  - **Example**:
    ```csharp
    int flags = 0b0011;     // Initial bit field
    int mask = 0b0100;      // Mask for setting a bit
    flags |= mask;          // Set the third bit
    // After this operation, flags will have the value 0b0111
    ```

Assignment operators are fundamental in C# for modifying the values of variables efficiently. They provide a shorthand way to perform arithmetic operations and assign the result back to the variable. Understanding and using assignment operators correctly is essential for writing concise and readable code.

## **Boxing Vs Unboxing:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Sure! Let's start with the explanations:

### Boxing:

- **Definition**: Boxing is the process of converting a value type (e.g., `int`, `float`, `struct`) to an object type (e.g., `object`, `interface`).
- **Scenario**: When you need to store value types in collections or pass them as arguments to methods that accept object types.
- **Example**:
  ```csharp
  int intValue = 10;         // Value type
  Object boxedValue = intValue;  // Boxing: converting int to object
  ```

### Unboxing:

- **Definition**: Unboxing is the process of converting an object type (e.g., `object`, `interface`) to a value type (e.g., `int`, `float`, `struct`).
- **Scenario**: When you retrieve value types from collections or cast them from object types back to their original value types.
- **Example**:
  ```csharp
  Object boxedValue = 10;    // Object type
  int intValue = (int)boxedValue;  // Unboxing: converting object to int
  ```

Now, let's present the differences between boxing and unboxing in tabular form:

| Feature                | Boxing                                    | Unboxing                                      |
|------------------------|-------------------------------------------|-----------------------------------------------|
| Definition             | Converts Value types to Reference types.     | Converts Reference types to Value types.         |
| Direction              | Converts from value type to object type.  | Converts from object type to value type.      |
| Memory              | Value Type variables are always stored in Stack memory.  | Reference Type variables are stored in Heap memory.      |
| Process                | Allocates memory and copies value.        | Retrieves the value from memory.              |
| Performance Impact     | May incur performance overhead due to memory allocation and copying. | Generally faster as it's a direct type cast. |
| Example Scenario       | Storing value types in collections such as ArrayList or List<object>. | Retrieving value types from collections.      |

Understanding the differences between boxing and unboxing is important for optimizing performance and avoiding unintended side effects in C# applications, especially when dealing with large datasets or performance-critical code sections.

## **Params in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

The `params` keyword in C# allows you to specify a method parameter that takes a variable number of arguments. This means that the number of arguments passed to the parameter can vary, and the compiler creates an array to contain them. Let's explore this with scenarios:

### Scenario 1: Calculating the Sum of Numbers

Suppose you want to create a method that calculates the sum of a variable number of integers.

```csharp
public class MathUtils
{
    public static int Sum(params int[] numbers)
    {
        int sum = 0;
        foreach (int num in numbers)
        {
            sum += num;
        }
        return sum;
    }
}
```

**Usage:**

```csharp
int result = MathUtils.Sum(1, 2, 3, 4, 5); // result will be 15
```

In this scenario, the `Sum` method can accept any number of integer arguments, and the `params` keyword simplifies the method signature, allowing the caller to pass a variable number of arguments.

### Scenario 2: Logging Messages

Suppose you want to create a logging method that accepts a variable number of strings to log.

```csharp
public class Logger
{
    public static void Log(params string[] messages)
    {
        foreach (string message in messages)
        {
            Console.WriteLine(message);
        }
    }
}
```

**Usage:**

```csharp
Logger.Log("Error: File not found.", "Warning: Memory usage high.", "Info: Task completed successfully.");
```

In this scenario, the `Log` method can accept any number of string messages to log, and the `params` keyword simplifies the method signature, allowing the caller to pass a variable number of arguments.

### Scenario 3: Formatting Strings

Suppose you want to create a method that formats a string with a variable number of placeholders and values.

```csharp
public class StringFormatter
{
    public static string Format(string format, params object[] args)
    {
        return string.Format(format, args);
    }
}
```

**Usage:**

```csharp
string result = StringFormatter.Format("Hello, {0}! Today's date is {1}.", "John", DateTime.Now);
Console.WriteLine(result);
```

In this scenario, the `Format` method can accept a format string with placeholders and a variable number of arguments to replace the placeholders, and the `params` keyword simplifies the method signature.

Using the `params` keyword allows you to create methods that are more flexible and easier to use, especially when the number of arguments passed to the method may vary. It simplifies the syntax for callers and provides more convenience when working with variable-length argument lists.

## **Type Casting in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Type casting in C# is the process of converting a value from one data type to another. There are two types of casting: implicit casting (also known as widening conversion) and explicit casting (also known as narrowing conversion). Let's explore both types with examples:

### 1. Implicit Casting (Widening Conversion):

Implicit casting occurs when the target data type can accommodate all possible values of the source data type without loss of precision. This type of casting is performed automatically by the compiler.

**Example:**

```csharp
int intValue = 10;
double doubleValue = intValue; // Implicit casting from int to double
```

In this example, the `int` value `10` is implicitly cast to a `double` value without the need for an explicit cast. Since `double` can accommodate all possible values of `int`, the conversion is performed automatically.

### 2. Explicit Casting (Narrowing Conversion):

Explicit casting occurs when the target data type may not be able to accommodate all possible values of the source data type without loss of precision. This type of casting requires an explicit cast operator.

**Example:**

```csharp
double doubleValue = 10.5;
int intValue = (int)doubleValue; // Explicit casting from double to int
```

In this example, the `double` value `10.5` is explicitly cast to an `int` value using the cast operator `(int)`. Since `int` cannot accommodate fractional values, the fractional part of `10.5` is truncated, and the resulting `intValue` will be `10`.

### Scenario:

Consider a scenario where you have a `double` variable representing a temperature in Celsius, and you need to convert it to an `int` variable representing the temperature in Fahrenheit.

```csharp
double celsiusTemp = 25.5;
int fahrenheitTemp = (int)(celsiusTemp * 9 / 5 + 32); // Explicit casting from double to int
```

In this scenario, the `double` value representing the temperature in Celsius is explicitly cast to an `int` value representing the temperature in Fahrenheit using the formula `(celsiusTemp * 9 / 5 + 32)`. Since `int` cannot accommodate fractional values, the result is explicitly cast to an `int` using the cast operator `(int)`.

Type casting is a powerful feature in C# that allows you to convert data between different data types, enabling interoperability and flexibility in your code. However, you should be cautious when performing explicit casting, as it may result in loss of precision or data truncation.

## **Enumeration in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Enums in C# provide a way to define a group of related named constants that represent integral values. They are often used to improve code readability and maintainability by giving meaningful names to numeric values. Let's explore enums with examples and outputs:

### Example 1: Days of the Week

```csharp
using System;

public enum DayOfWeek
{
    Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday
}

class Program
{
    static void Main()
    {
        DayOfWeek today = DayOfWeek.Monday;
        Console.WriteLine($"Today is {today}");
        Console.WriteLine($"Enum Value for {today} is {(int)today}");
    }
}
```

**Output:**
```
Today is Monday
Enum Value for Monday is 1
```

### Example 2: Traffic Light Colors

```csharp
using System;

public enum TrafficLightColor
{
    Red, Yellow, Green
}

class Program
{
    static void Main()
    {
        TrafficLightColor currentColor = TrafficLightColor.Red;
        Console.WriteLine($"The current color is {currentColor}");
    }
}
```

**Output:**
```
The current color is Red
```

### Example 3: Custom Integral Values

```csharp
using System;

public enum HttpStatusCode
{
    OK = 200,
    BadRequest = 400,
    NotFound = 404,
    InternalServerError = 500
}

class Program
{
    static void Main()
    {
        HttpStatusCode responseCode = HttpStatusCode.OK;
        Console.WriteLine($"Response code: {responseCode}");
    }
}
```

**Output:**
```
Response code: OK
```

### Example 4: Flags Enum

```csharp
using System;

[Flags]
public enum FileAccess
{
    None = 0,
    Read = 1 << 0,
    Write = 1 << 1,
    ReadWrite = Read | Write
}

class Program
{
    static void Main()
    {
        FileAccess myAccess = FileAccess.Read | FileAccess.Write;
        if ((myAccess & FileAccess.Read) != 0)
        {
            Console.WriteLine("Read access granted.");
        }
        if ((myAccess & FileAccess.Write) != 0)
        {
            Console.WriteLine("Write access granted.");
        }
    }
}
```

**Output:**
```
Read access granted.
Write access granted.
```

Enums in C# are versatile and widely used for defining sets of named constants. They improve code readability, make it easier to understand and maintain, and provide compile-time type safety.

## **Properties in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Properties in C# provide a way to encapsulate data within objects and control access to that data. They allow you to define methods to get (getters) and set (setters) the value of private fields while hiding the implementation details. Properties came into existence to provide a more object-oriented approach to access and modify class members, compared to using public fields directly. Let's see an example and discuss why properties are used:

### Example: Student Class with Properties

```csharp
using System;

public class Student
{
    private string name;
    private int age;

    // Property to get and set the name
    public string Name
    {
        get { return name; }
        set { name = value; }
    }

    // Property to get and set the age
    public int Age
    {
        get { return age; }
        set
        {
            if (value >= 0 && value <= 120)
            {
                age = value;
            }
            else
            {
                throw new ArgumentException("Age must be between 0 and 120.");
            }
        }
    }
}

class Program
{
    static void Main()
    {
        // Create a new student object
        Student student = new Student();

        // Set the properties
        student.Name = "John Doe";
        student.Age = 25;

        // Retrieve and display the properties
        Console.WriteLine($"Name: {student.Name}");
        Console.WriteLine($"Age: {student.Age}");
    }
}
```

In this example, we have a `Student` class with private fields `name` and `age`, and properties `Name` and `Age` to get and set their values, respectively. 


### Why Properties Are Used:

1. **Encapsulation**: Properties encapsulate the internal state of an object by providing controlled access to its data. They allow you to hide the implementation details of how the data is stored or computed.

2. **Data Validation**: Properties enable you to validate the values being assigned to them before updating the underlying fields. This ensures data integrity and consistency.

3. **Abstraction**: Properties provide an abstraction layer over fields, allowing you to modify the internal representation of data without affecting the external interface.

4. **Code Maintainability**: By encapsulating data access within properties, you can modify the internal implementation of a class without impacting the code that uses it.

5. **Readability and Expressiveness**: Properties make the code more readable and expressive by providing a clear and concise syntax for accessing and modifying object data.

Overall, properties in C# enhance the encapsulation, data validation, abstraction, and maintainability of object-oriented code, leading to more robust and flexible software designs.

## **Get Accessor & Set Accessor:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, properties are composed of a getter and/or a setter, which are referred to as accessors. These accessors define how the value of the property can be retrieved and modified. Let's explain each accessor:

### Get Accessor (Getter):

The get accessor is used to retrieve the value of the property. It is responsible for returning the current value of the property when the property is accessed.

**Syntax:**
```csharp
public int MyProperty
{
    get
    {
        // Return the value of the property
        return someValue;
    }
}
```

In this example, `MyProperty` is a property with a get accessor that returns the value of `someValue`.

### Set Accessor (Setter):

The set accessor is used to modify the value of the property. It allows you to assign a new value to the property.

**Syntax:**
```csharp
public int MyProperty
{
    set
    {
        // Assign the value to the property
        someValue = value;
    }
}
```

In this example, `MyProperty` is a property with a set accessor that assigns the value of `value` to `someValue`.

### Example: Property with Both Get and Set Accessors

```csharp
private int myProperty;

public int MyProperty
{
    get
    {
        // Return the value of the property
        return myProperty;
    }
    set
    {
        // Assign the value to the property
        myProperty = value;
    }
}
```

In this example, `MyProperty` is a property with both a get accessor to retrieve the value and a set accessor to modify the value.

### Usage:

Properties with both get and set accessors provide a way to encapsulate data within an object while controlling access to it. They allow you to define read-only, write-only, or read-write properties based on your requirements. 

**Read-Only Property:**
```csharp
public int ReadOnlyProperty
{
    get
    {
        // Return the value (no setter)
        return someValue;
    }
}
```

**Write-Only Property:**
```csharp
public int WriteOnlyProperty
{
    set
    {
        // Assign the value (no getter)
        someValue = value;
    }
}
```

Properties with accessors provide a clean and intuitive way to work with object data, enhancing encapsulation, data validation, and code readability in C#.

## **Nullable types:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, a nullable type allows you to represent both normal range of values for its underlying value type and a null value. This is particularly useful when you need to represent the absence of a value in scenarios where a value type is required. Nullable types are represented by appending a `?` to the underlying value type. Let's explore nullable types with an example and output:

### Example: Nullable Integers

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declare a nullable integer
        int? nullableInt = null;

        // Assign a value to the nullable integer
        nullableInt = 10;

        // Output the value of the nullable integer
        if (nullableInt.HasValue)
        {
            Console.WriteLine($"Value of nullableInt: {nullableInt.Value}");
        }
        else
        {
            Console.WriteLine("nullableInt is null");
        }
    }
}
```

**Output:**
```
Value of nullableInt: 10
```

### Explanation:

- In this example, we declare a nullable integer `nullableInt` using the `int?` syntax. By default, `nullableInt` is assigned a value of `null`.
- We then assign a value of `10` to `nullableInt`.
- We use the `HasValue` property to check if `nullableInt` has a value. If it does, we output the value using the `Value` property. If it doesn't, we output that `nullableInt` is null.
- Since `nullableInt` has a value of `10`, the output will be "Value of nullableInt: 10".

### Example: Nullable Booleans

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declare a nullable boolean
        bool? nullableBool = null;

        // Assign a value to the nullable boolean
        nullableBool = true;

        // Output the value of the nullable boolean
        if (nullableBool.HasValue)
        {
            Console.WriteLine($"Value of nullableBool: {nullableBool.Value}");
        }
        else
        {
            Console.WriteLine("nullableBool is null");
        }
    }
}
```

**Output:**
```
Value of nullableBool: True
```

### Explanation:

- In this example, we declare a nullable boolean `nullableBool` using the `bool?` syntax. By default, `nullableBool` is assigned a value of `null`.
- We then assign a value of `true` to `nullableBool`.
- We use the `HasValue` property to check if `nullableBool` has a value. If it does, we output the value using the `Value` property. If it doesn't, we output that `nullableBool` is null.
- Since `nullableBool` has a value of `true`, the output will be "Value of nullableBool: True".

Nullable types in C# are useful when you need to represent a value type that can also be null, providing flexibility in handling missing or optional values.

## **Structures in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

Structures (structs) in C# are user-defined value types that can contain data members and member functions. They are similar to classes but have some key differences, such as being value types (allocated on the stack) rather than reference types (allocated on the heap). Structs are commonly used for small, lightweight objects that represent simple data types. Let's explore structs with a detailed example and output.

### Example: Creating a Struct for a Point in 2D Space

Let's create a struct called `Point` to represent a point in 2D space with x and y coordinates. We'll define properties to access and modify the coordinates, and a method to calculate the distance from another point.

```csharp
using System;

public struct Point
{
    // Data members
    public int X;
    public int Y;

    // Constructor
    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }

    // Method to calculate distance from another point
    public double DistanceTo(Point other)
    {
        int deltaX = X - other.X;
        int deltaY = Y - other.Y;
        return Math.Sqrt(deltaX * deltaX + deltaY * deltaY);
    }
}

class Program
{
    static void Main()
    {
        // Create two points
        // no need to create an
        // instance using 'new' keyword
        Point point1;
        point1.X = 3;
        point1.Y = 4;
        Point point2;
        point2.X = 6;
        point2.Y = 8;

        // Display the coordinates of the points
        Console.WriteLine($"Point 1: ({point1.X}, {point1.Y})");
        Console.WriteLine($"Point 2: ({point2.X}, {point2.Y})");

        // Calculate and display the distance between the points
        double distance = point1.DistanceTo(point2);
        Console.WriteLine($"Distance between the points: {distance}");
    }
}
```

**Output:**
```
Point 1: (3, 4)
Point 2: (6, 8)
Distance between the points: 5
```

### Explanation:

- We define a struct called `Point` with two data members `X` and `Y` representing the x and y coordinates of the point.
- We define a constructor to initialize the coordinates of the point when it is created.
- We define a method `DistanceTo` to calculate the distance between the current point and another point passed as an argument.
- In the `Main` method, we create two instances of the `Point` struct, `point1` and `point2`, with different coordinates.
- We display the coordinates of the points and calculate the distance between them using the `DistanceTo` method.

### Key Points about Structs:

1. **Value Types**: Structs are value types, which means they are stored on the stack and copied by value when passed as arguments or assigned to other variables.

2. **Lightweight**: Structs are lightweight compared to classes, making them suitable for representing small, simple data structures.

3. **Immutability**: By default, structs are immutable, meaning their data members cannot be modified after creation. However, you can define mutable structs by using mutable data members or methods that modify the state of the struct.

4. **Performance**: Structs can offer better performance than classes in certain scenarios, especially when dealing with small, frequently used objects.

5. **Use Cases**: Structs are commonly used for representing simple data types, such as coordinates, points, rectangles, and other small, value-based objects.

Structs provide a powerful and efficient way to define and work with small, lightweight data structures in C#, offering performance benefits and flexibility for various programming tasks.

### Can we add methods inside struct in c#? How can we access static and non-static members inside struct?

Yes, we can add methods inside a struct in C#. These methods can be both static and non-static, allowing structs to encapsulate behavior along with data. Let's explore how to add methods to a struct and how to access both static and non-static members inside a struct with examples and outputs.

### Example: Adding Methods to a Struct

```csharp
using System;

public struct Rectangle
{
    public int Length { get; set; }
    public int Width { get; set; }

    // Non-static method to calculate area
    public int CalculateArea()
    {
        return Length * Width;
    }

    // Static method to compare two rectangles
    public static bool AreEqual(Rectangle r1, Rectangle r2)
    {
        return r1.Length == r2.Length && r1.Width == r2.Width;
    }
}

class Program
{
    static void Main()
    {
        Rectangle rect1 = new Rectangle { Length = 5, Width = 4 };
        Rectangle rect2 = new Rectangle { Length = 3, Width = 6 };

        // Access non-static method
        int area1 = rect1.CalculateArea();
        Console.WriteLine($"Area of rect1: {area1}");

        // Access static method
        bool equal = Rectangle.AreEqual(rect1, rect2);
        Console.WriteLine($"Are rect1 and rect2 equal? {equal}");
    }
}
```

**Output:**
```
Area of rect1: 20
Are rect1 and rect2 equal? False
```

### Explanation:

- We define a struct called `Rectangle` with two data members `Length` and `Width`, representing the dimensions of a rectangle.
- We add a non-static method `CalculateArea()` to calculate the area of the rectangle.
- We add a static method `AreEqual()` to compare two rectangles for equality.
- In the `Main` method, we create two instances of the `Rectangle` struct, `rect1` and `rect2`, with different dimensions.
- We call the non-static method `CalculateArea()` on `rect1` to calculate its area and display the result.
- We call the static method `AreEqual()` on the `Rectangle` struct itself to compare `rect1` and `rect2` for equality and display the result.

### Accessing Static and Non-Static Members Inside Struct

- **Accessing Non-Static Members**: Non-static members (properties, methods) inside a struct can be accessed using the instance of the struct (`this` keyword is optional).

- **Accessing Static Members**: Static members (properties, methods) inside a struct can be accessed using the name of the struct itself, followed by the member name.

In the example above:
- We access the non-static method `CalculateArea()` using the instance `rect1`.
- We access the static method `AreEqual()` using the name of the struct `Rectangle`.

Both static and non-static methods can be useful inside a struct, providing behavior and functionality along with data encapsulation. They allow structs to represent more complex entities and perform operations on them.

## **Static Keyword in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

The `static` keyword in C# is used to declare members (methods, properties, fields, and constructors) that belong to the type itself, rather than to instances of the type. This means that a static member is shared among all instances of the type and can be accessed directly through the type name without creating an instance. Let's explore various uses of the `static` keyword with examples and scenarios:

### 1. Static Class:

A static class in C# is a class that can only contain static members (fields, methods, properties, events, or nested types) and cannot be instantiated. Static classes are commonly used to group related utility methods or constants and provide a convenient way to organize and access functionality without the need for object instantiation.

```csharp
public static class MathUtility
{
    public static double Add(double a, double b)
    {
        return a + b;
    }

    public static double Subtract(double a, double b)
    {
        return a - b;
    }
}

class Program
{
    static void Main()
    {
        double sum = MathUtility.Add(5, 3);
        Console.WriteLine($"Sum: {sum}");
    }
}
```

**Output:**
```
Sum: 8
```

In this example, `MathUtility` is a static class containing static methods for performing addition and subtraction.

### Key Points about Static Classes:

1. **No Instance Creation**: Static classes cannot be instantiated using the `new` keyword, and all members of a static class must be static.

2. **Accessing Members**: Static members of a static class can be accessed directly through the class name without creating an instance of the class.

3. **Utility Functions**: Static classes are commonly used to group related utility methods or constants that do not require instance-specific data.

4. **Namespace Organization**: Static classes provide a convenient way to organize functionality within a namespace without the need for object instantiation.

5. **Cannot Inherit or Be Inherited**: Static classes cannot inherit from other classes, and they cannot be inherited by other classes.

### 2. Static Method:

Static methods in C# are methods that belong to the type itself rather than to instances of the type. They are declared using the `static` keyword and can be invoked directly through the type name without the need to create an instance of the class. Static methods are commonly used for utility methods, helper functions, or operations that do not require access to instance-specific data.

```csharp
public class StringUtils
{
    public static int GetStringLength(string input)
    {
        return input.Length;
    }
}

class Program
{
    static void Main()
    {
        int length = StringUtils.GetStringLength("Hello, World!");
        Console.WriteLine($"Length: {length}");
    }
}
```

**Output:**
```
Length: 13
```

In this example, `GetStringLength` is a static method of the `StringUtils` class that returns the length of a string.

#### Key Points about Static Methods:

1. **No Instance Required**: Static methods belong to the type itself and do not require an instance of the class to be invoked. They can be called directly through the class name.

2. **Accessing Static and Non-Static Members**: Static methods can only access other static members of the class. They cannot access instance members (non-static fields, properties, or methods) unless they are provided with an instance of the class as a parameter.

3. **Stateless Operations**: Static methods are stateless and do not have access to instance-specific data. They are commonly used for operations that do not rely on instance state.

4. **Utility Methods**: Static methods are often used for utility methods, helper functions, or operations that are not tied to specific instances of the class.

5. **Performance Benefits**: Since static methods do not require object instantiation, they can offer better performance compared to instance methods, especially for operations that do not require access to instance data.

### 3. Static Variables:

Static variables in C# are variables that belong to the type itself rather than to instances of the type. They are declared using the `static` keyword and maintain their value across all instances of the class. Static variables are shared among all instances of the class and can be accessed directly through the class name without the need to create an instance.

```csharp
public class Counter
{
    public static int Count = 0;

    public Counter()
    {
        Count++;
    }
}

class Program
{
    static void Main()
    {
        Counter c1 = new Counter();
        Counter c2 = new Counter();
        Console.WriteLine($"Number of counters created: {Counter.Count}");
    }
}
```

**Output:**
```
Number of counters created: 2
```

In this example, the `Count` variable is a static variable that keeps track of the number of `Counter` instances created.

#### Key Points about Static Variables:

1. **Shared Among Instances**: Static variables are shared among all instances of the class and maintain their value across all instances.

2. **Accessed Through Class Name**: Static variables can be accessed directly through the class name without the need to create an instance of the class.

3. **Initialization**: Static variables can be initialized inline or in a static constructor. If not initialized explicitly, they are assigned a default value based on their data type (e.g., `0` for numeric types, `null` for reference types).

4. **Global State**: Static variables introduce global state to your application, which can lead to potential issues such as race conditions in multithreaded environments. Care should be taken when using static variables to ensure thread safety.

5. **Performance Benefits**: Since static variables are shared among all instances of the class, they can offer performance benefits in scenarios where data needs to be shared across multiple instances.

### 4. Static Constructor:

A static constructor in C# is a special type of constructor that is used to initialize static data members or to perform any necessary setup tasks that need to be executed only once when the type is first accessed. Static constructors are invoked automatically by the runtime before any static members of the class are accessed or before any instance of the class is created.

```csharp
public class AppConfig
{
    public static string AppName { get; }

    static AppConfig()
    {
        AppName = "MyApp";
    }
}

class Program
{
    static void Main()
    {
        Console.WriteLine($"Application Name: {AppConfig.AppName}");
    }
}
```

**Output:**
```
Application Name: MyApp
```

In this example, the static constructor of `AppConfig` initializes the `AppName` property to a default value.

#### Key Points about Static Constructors:

1. **Execution Timing**: Static constructors are executed automatically by the runtime before any static members of the class are accessed or before any instance of the class is created.
   
2. **Initialization**: Static constructors are typically used to initialize static data members or perform any one-time initialization tasks for the class.
   
3. **Implicit Invocation**: Static constructors are invoked implicitly by the runtime and cannot be called explicitly like instance constructors.
   
4. **No Parameters**: Static constructors cannot have parameters, access modifiers, or be inherited or overloaded.

5. **Single Execution**: Static constructors are guaranteed to run only once per application domain, regardless of the number of instances or static member accesses.

### Limitations of Using Static Keyword:

1. **Global State**: Static members introduce global state, making code less modular and harder to test.

2. **Thread Safety**: Static members can introduce thread safety issues in multithreaded environments if not properly synchronized.

3. **Inheritance**: Static members cannot be overridden or inherited, limiting polymorphism.

4. **Testing**: Code that relies heavily on static members can be difficult to unit test, as static members are tightly coupled and cannot be easily mocked.

5. **Performance**: Excessive use of static members can lead to performance issues, especially in heavily concurrent applications.

While the `static` keyword can be useful for certain scenarios, it should be used judiciously to avoid the aforementioned limitations and maintain code maintainability, testability, and performance.

## **Is vs As operator keyword in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

| Feature            | `is` Operator                                            | `as` Operator                                              |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------|
| Purpose            | Checks if an object is compatible with a given type.     | Attempts to cast an object to a specified type.             |
| Usage              | Used in boolean expressions.                             | Used in assignment or as a cast expression.                 |
| Syntax             | `expression is type`                                     | `expression as type`                                        |
| Result             | Returns `true` or `false` based on type compatibility.   | Returns `null` if the conversion fails, otherwise the casted object. |
| Type Check         | Performs a type check without casting the object.        | Performs a type check and casts the object if compatible.   |
| Exception Handling | Does not throw an exception.                             | Does not throw an exception.                                |
| Performance        | Generally faster than using the `as` operator.           | Generally slower than using the `is` operator.              |
| Example            | `if (obj is MyClass)`                                   | `MyClass myObj = obj as MyClass;`                          |
|                   |                                                          | `if (myObj != null)`                                        |

In summary:
- **`is` Operator**: Used for type checking and returns a boolean value indicating whether the object is compatible with the specified type. Does not perform casting.
- **`as` Operator**: Used for casting an object to a specified type. Returns `null` if the cast fails, otherwise, returns the casted object. Does not throw exceptions.

## **typeof vs GetType Operator:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

| Feature            | `typeof`                                          | `GetType()`                                       |
|--------------------|---------------------------------------------------|--------------------------------------------------|
| Purpose            | Obtains the `Type` object for a specified type.  | Obtains the `Type` object for the current instance. |
| Usage              | Used with compile-time types.                     | Used with runtime objects.                        |
| Syntax             | `typeof(TypeName)`                                | `instance.GetType()`                             |
| Result             | Returns the `Type` object representing the specified type. | Returns the `Type` object representing the runtime type of the object. |
| Type Information   | Works with types at compile time.                 | Works with objects at runtime.                   |
| Compile Time       | Resolved at compile time.                         | Resolved at runtime.                              |
| Exceptions         | Does not throw exceptions.                        | Does not throw exceptions.                        |
| Example            | `Type t = typeof(MyClass);`                      | `object obj = new MyClass();`<br>`Type t = obj.GetType();` |

In summary:
- **`typeof` Operator**: Used to get the `Type` object of a compile-time type. It's resolved at compile time and does not throw exceptions. It's used when you need type information for a type known at compile time.
- **`GetType()` Method**: Used to get the `Type` object of a runtime object. It's resolved at runtime and doesn't throw exceptions. It's used when you need type information for an object whose type is determined at runtime.

## **ref in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/2%20-%20Fundamentals.md#fundamentals-)

In C#, the `ref` keyword is used to pass arguments by reference to a method, allowing the method to modify the value of the variable passed as an argument. When you pass a variable by reference, you are passing the memory address of the variable rather than a copy of its value. This means any changes made to the parameter inside the method will affect the original variable outside the method. Let's explore some scenarios and examples to understand how `ref` works:

### Scenario 1: Modifying Value of a Variable Inside a Method

```csharp
using System;

public class Program
{
    public static void IncrementByRef(ref int num)
    {
        num += 10;
    }

    static void Main()
    {
        int value = 5;
        Console.WriteLine($"Original value: {value}");

        IncrementByRef(ref value);
        Console.WriteLine($"Value after incrementing by reference: {value}");
    }
}
```

**Output:**
```
Original value: 5
Value after incrementing by reference: 15
```

In this example:
- We define a method `IncrementByRef` that takes an integer parameter `num` by reference using the `ref` keyword.
- Inside the method, we increment the value of `num` by 10.
- In the `Main` method, we declare a variable `value` and pass it to `IncrementByRef` by reference using the `ref` keyword.
- After calling the method, the value of `value` is modified to 15.

### Scenario 2: Swapping Values of Two Variables

```csharp
using System;

public class Program
{
    public static void SwapValues(ref int a, ref int b)
    {
        int temp = a;
        a = b;
        b = temp;
    }

    static void Main()
    {
        int x = 5, y = 10;
        Console.WriteLine($"Before swapping: x = {x}, y = {y}");

        SwapValues(ref x, ref y);
        Console.WriteLine($"After swapping: x = {x}, y = {y}");
    }
}
```

**Output:**
```
Before swapping: x = 5, y = 10
After swapping: x = 10, y = 5
```

In this example:
- We define a method `SwapValues` that takes two integer parameters `a` and `b` by reference using the `ref` keyword.
- Inside the method, we swap the values of `a` and `b`.
- In the `Main` method, we declare two variables `x` and `y` and pass them to `SwapValues` by reference using the `ref` keyword.
- After calling the method, the values of `x` and `y` are swapped.

### Key Points about `ref`:

- `ref` parameters must be initialized before being passed to a method.
- Any changes made to a `ref` parameter inside the method are reflected in the original variable outside the method.
- It's often used when you need to modify the value of a variable inside a method and want those changes to be visible outside the method.