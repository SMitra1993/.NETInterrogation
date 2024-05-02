# Fundamentals ❤🍕

**Links:**

- [C# Identifier](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#c-identifier-)
- [Data Types](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#data-types-)
- [Data Variables](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#data-variables-)
- [Types of Variables](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#types-of-variables-)
- [Instance variable Vs Static variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#instance-variable-vs-static-variable-)
- [Constants variable Vs Read-Only variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#constants-variable-vs-read-only-variable-)
- [Var - Implicitely typed variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#var---implicitely-typed-variable-)
- [Dynamic Type](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#dynamic-type-)
- [Var Vs Dynamic Type](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#var-vs-dynamic-type-)
- [Scope of Variable](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#scope-of-variable-)
- [Access Modifiers](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#access-modifiers-)
- [Literals in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#literals-in-c-)

## **C# Identifier:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Data Types:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Data Variables:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Types of Variables:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Instance variable Vs Static variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

| Aspect                 | Instance Variable                         | Static Variable                                |
|------------------------|-------------------------------------------|------------------------------------------------|
| Declaration            | Declared within a class, but outside any method. | Declared with the `static` keyword within a class. |
| Scope                  | Belongs to an instance of the class.      | Belongs to the class itself rather than to any instance. |
| Accessibility          | Accessed using an instance of the class.   | Accessed using the class name directly or via an instance. |
| Memory Allocation      | Memory allocated separately for each instance of the class. | Memory allocated only once for all instances of the class. |
| Lifetime               | Exist as long as the instance of the class exists. | Exist as long as the program is running or until explicitly modified. |
| Initialization         | Initialized when an instance of the class is created. | Initialized when the class is loaded into memory. |

In summary, instance variables are specific to each instance of a class and are accessed through instances of the class, whereas static variables belong to the class itself and are accessed directly using the class name. Instance variables have separate memory allocations for each instance, while static variables have a single memory allocation shared across all instances of the class.

## **Constants variable Vs Read-Only variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Var - Implicitely typed variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Dynamic Type:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Var Vs Dynamic Type:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Scope of Variable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Access Modifiers:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## **Literals in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/Fundamentals.md#fundamentals-)

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

## 