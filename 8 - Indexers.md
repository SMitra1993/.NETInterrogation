# Indexers ❤🍕

**Links:**
- [Indexers in c#](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#indexers-in-c-)
- [Properties Vs Indexers](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#properties-vs-indexers-)
- [Multidimensional Indexers](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#multidimensional-indexers-)
- [Overloading of Indexers](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#overloading-of-indexers-)

## **Indexers in c#:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#indexers-)

Indexers in C# allow instances of a class or struct to be indexed just like arrays. They provide a way to access elements of a collection or class using square brackets, similar to array indexing. Indexers are defined using the `this` keyword followed by one or more parameters. When an object of the class or struct is indexed, the indexed property accessor (getter or setter) is invoked, allowing you to get or set the value associated with the index.

### Example:

Let's create an example to demonstrate indexers in C#:

```csharp
using System;

public class MyCollection
{
    private int[] data = new int[5]; // Internal data storage

    // Indexer definition
    public int this[int index]
    {
        get
        {
            // Getter implementation
            return data[index];
        }
        set
        {
            // Setter implementation
            data[index] = value;
        }
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of MyCollection
        MyCollection collection = new MyCollection();

        // Set values using indexer
        collection[0] = 10;
        collection[1] = 20;
        collection[2] = 30;
        collection[3] = 40;
        collection[4] = 50;

        // Get and display values using indexer
        Console.WriteLine("Values from the collection:");
        for (int i = 0; i < 5; i++)
        {
            Console.WriteLine($"Value at index {i}: {collection[i]}");
        }
    }
}
```

### Output:

```
Values from the collection:
Value at index 0: 10
Value at index 1: 20
Value at index 2: 30
Value at index 3: 40
Value at index 4: 50
```

### Explanation:

- We define a class `MyCollection` with an internal array `data` to store the collection elements.
- Inside the class, we define an indexer using the `this` keyword, which allows indexing the instance of `MyCollection`.
- The indexer provides both a getter and a setter, allowing us to get and set values at specific indices in the collection.
- In the `Main` method, we create an instance of `MyCollection` and set values using the indexer.
- We then retrieve and display the values using the indexer in a loop.

### Summary:

- Indexers in C# provide a way to access elements of a collection or class using square brackets, similar to array indexing.
- They are defined using the `this` keyword followed by one or more parameters.
- Indexers can have both getter and setter implementations, allowing you to get and set values at specific indices in the collection or class.

## **Properties Vs Indexers:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#indexers-)

Here's a comparison of properties and indexers in C# presented in a tabular form:

| Feature                      | Properties                                          | Indexers                                               |
|------------------------------|-----------------------------------------------------|--------------------------------------------------------|
| Definition                   | Define member accessors for fields or calculated values. | Define a mechanism to access elements of a collection or class. |
| Syntax                       | Defined using `get` and `set` accessors.           | Defined using `this` keyword followed by parameters.    |
| Access Modifier              | Can have access modifiers (public, private, etc.).  | Can have access modifiers (public, private, etc.).      |
| Parameters                   | No parameters in property definition.               | Can have one or more parameters.                        |
| Usage                        | Typically used to expose private fields with controlled access. | Used to access elements of a collection or class using square brackets. |
| Return Type                  | Can return a single value of a specific type.      | Can return a value of any type, including arrays, collections, etc. |
| Multiple                    | Cannot overload a property with different signatures. | Can overload an indexer with different parameter signatures. |
| Naming Convention            | Typically named with descriptive names (e.g., `FirstName`). | Often named using generic names like `this[int index]`.  |
| Syntax Example               | ```csharp                                         | ```csharp                                                 |
|                              | public string Name { get; set; }                  | public int this[int index] { get; set; }                   |

### Summary:

- **Properties**: Used to provide controlled access to fields or calculated values of a class. They define `get` and `set` accessors and are commonly used to expose private fields with controlled access. Properties can have access modifiers and a single return type, and they cannot be overloaded with different signatures.

- **Indexers**: Used to provide a mechanism to access elements of a collection or class using square brackets. They are defined using the `this` keyword followed by parameters, allowing for indexed access to elements. Indexers can have access modifiers, multiple parameters, and can return a value of any type, including arrays, collections, etc. They can be overloaded with different parameter signatures to provide different access patterns.

## **Multidimensional Indexers:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#indexers-)

In C#, multidimensional indexers allow you to define classes with indexers that take multiple indices, enabling access to elements in a multidimensional array-like manner. This allows for more complex data structures to be represented and accessed conveniently.

### Example:

Let's create an example to demonstrate multidimensional indexers in C#:

```csharp
using System;

public class Matrix
{
    private int[,] data; // 2D array to store matrix data

    // Constructor to initialize matrix dimensions
    public Matrix(int rows, int columns)
    {
        data = new int[rows, columns];
    }

    // Multidimensional indexer
    public int this[int row, int column]
    {
        get { return data[row, column]; }
        set { data[row, column] = value; }
    }

    // Method to display the matrix
    public void Display()
    {
        int rows = data.GetLength(0);
        int columns = data.GetLength(1);

        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < columns; j++)
            {
                Console.Write(data[i, j] + "\t");
            }
            Console.WriteLine();
        }
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create a 3x3 matrix
        Matrix matrix = new Matrix(3, 3);

        // Set values using multidimensional indexer
        matrix[0, 0] = 1;
        matrix[0, 1] = 2;
        matrix[0, 2] = 3;
        matrix[1, 0] = 4;
        matrix[1, 1] = 5;
        matrix[1, 2] = 6;
        matrix[2, 0] = 7;
        matrix[2, 1] = 8;
        matrix[2, 2] = 9;

        // Display the matrix
        Console.WriteLine("Matrix:");
        matrix.Display();
    }
}
```

### Output:

```
Matrix:
1       2       3
4       5       6
7       8       9
```

### Explanation:

- We define a `Matrix` class with a private 2D array `data` to store the matrix elements.
- We provide a constructor to initialize the dimensions of the matrix.
- We define a multidimensional indexer using the `this` keyword, which takes two indices (`row` and `column`) to access elements of the matrix.
- The `Display` method prints the elements of the matrix in row-major order.
- In the `Main` method, we create an instance of the `Matrix` class and set values using the multidimensional indexer.
- Finally, we display the matrix using the `Display` method.

### Summary:

- Multidimensional indexers in C# allow classes to define indexers that take multiple indices, enabling access to elements in a multidimensional array-like manner.
- They provide a convenient way to represent and access elements of complex data structures, such as matrices or grids.
- Multidimensional indexers are defined using the `this` keyword followed by multiple index parameters, and they can have both getter and setter implementations.

## **Overloading of Indexers:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/8%20-%20Indexers.md#indexers-)

Overloading of indexers in C# allows you to define multiple indexers within a class with different sets of parameters. This enables you to provide different ways to access elements or properties of the class based on the context or requirements.

### Example:

Let's create an example to demonstrate overloading of indexers in C#:

```csharp
using System;

public class Matrix
{
    private int[,] data; // 2D array to store matrix data
    private int rows;
    private int columns;

    // Constructor to initialize matrix dimensions
    public Matrix(int rows, int columns)
    {
        this.rows = rows;
        this.columns = columns;
        data = new int[rows, columns];
    }

    // Overloaded indexer for accessing matrix elements by coordinates
    public int this[int row, int column]
    {
        get { return data[row, column]; }
        set { data[row, column] = value; }
    }

    // Overloaded indexer for accessing matrix elements by linear index
    public int this[int index]
    {
        get
        {
            int row = index / columns;
            int column = index % columns;
            return data[row, column];
        }
        set
        {
            int row = index / columns;
            int column = index % columns;
            data[row, column] = value;
        }
    }

    // Method to display the matrix
    public void Display()
    {
        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < columns; j++)
            {
                Console.Write(data[i, j] + "\t");
            }
            Console.WriteLine();
        }
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create a 3x3 matrix
        Matrix matrix = new Matrix(3, 3);

        // Set values using both indexers
        matrix[0, 0] = 1;
        matrix[0, 1] = 2;
        matrix[0, 2] = 3;
        matrix[1, 0] = 4;
        matrix[1, 1] = 5;
        matrix[1, 2] = 6;
        matrix[2, 0] = 7;
        matrix[2, 1] = 8;
        matrix[2, 2] = 9;

        // Display the matrix
        Console.WriteLine("Matrix:");
        matrix.Display();

        // Access elements using the linear indexer
        Console.WriteLine("\nElements using linear indexer:");
        for (int i = 0; i < 9; i++)
        {
            Console.Write(matrix[i] + " ");
        }
    }
}
```

### Output:

```
Matrix:
1       2       3
4       5       6
7       8       9

Elements using linear indexer:
1 2 3 4 5 6 7 8 9 
```

### Explanation:

- We define a `Matrix` class with a private 2D array `data` to store the matrix elements, along with variables to store the number of rows and columns.
- We provide two overloaded indexers within the `Matrix` class:
  - The first indexer allows access to matrix elements by row and column indices.
  - The second indexer allows access to matrix elements by a linear index, where the row index is calculated as `index / columns` and the column index is calculated as `index % columns`.
- In the `Main` method, we create an instance of the `Matrix` class and set values using the first indexer.
- We then display the matrix using the `Display` method.
- Next, we access elements using the linear indexer and print them to the console.

### Summary:

- Overloading of indexers in C# allows a class to define multiple indexers with different sets of parameters.
- This enables providing different ways to access elements or properties of the class based on the context or requirements.
- In the example, we provided two overloaded indexers in the `Matrix` class to allow access to matrix elements either by row and column indices or by a linear index.
- Overloading indexers enhances the flexibility and usability of the class by providing different access patterns tailored to specific scenarios.
