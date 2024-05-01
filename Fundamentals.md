# Fundamentals ❤🍕


## **C# Identifier:**

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

## **Data Types:**

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

## **Data Variables:**

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

## **Types of Variables:**

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

## **Instance variable Vs Static variable:**

| Aspect                 | Instance Variable                         | Static Variable                                |
|------------------------|-------------------------------------------|------------------------------------------------|
| Declaration            | Declared within a class, but outside any method. | Declared with the `static` keyword within a class. |
| Scope                  | Belongs to an instance of the class.      | Belongs to the class itself rather than to any instance. |
| Accessibility          | Accessed using an instance of the class.   | Accessed using the class name directly or via an instance. |
| Memory Allocation      | Memory allocated separately for each instance of the class. | Memory allocated only once for all instances of the class. |
| Lifetime               | Exist as long as the instance of the class exists. | Exist as long as the program is running or until explicitly modified. |
| Initialization         | Initialized when an instance of the class is created. | Initialized when the class is loaded into memory. |

In summary, instance variables are specific to each instance of a class and are accessed through instances of the class, whereas static variables belong to the class itself and are accessed directly using the class name. Instance variables have separate memory allocations for each instance, while static variables have a single memory allocation shared across all instances of the class.

## **Constants variable Vs Read-Only variable:**

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