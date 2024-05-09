# Array ❤🍕

**Links:**

- [Array](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [1-D, 2-D, 3-D and N-D Array](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Jagged Array](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Array Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Array Methods](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Array Properties](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Dynamic Array](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [ArrayList](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [ArrayList Methods](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [ArrayList Properties](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [ArrayList Constructors](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Array Vs ArrayList](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)
- [Arrayist Vs List](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#class--object-)

## **Array** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, an array is a data structure that stores a fixed-size collection of elements of the same type in contiguous memory locations. Arrays provide a convenient way to work with collections of data and are widely used in programming for various tasks, such as storing data, accessing elements by index, and performing operations on elements.

### Declaration and Initialization:

Arrays in C# are declared using square brackets (`[]`). There are two main ways to declare and initialize arrays:

1. **Using Array Initializer Syntax:**
   ```csharp
   // Declaration and initialization using array initializer syntax
   int[] numbers = { 1, 2, 3, 4, 5 };
   ```

2. **Using the `new` Keyword:**
   ```csharp
   // Declaration and initialization using the new keyword
   int[] numbers = new int[5]; // Creates an array of size 5 with default values (0 for int)
   ```

### Accessing Elements:

Array elements are accessed using an index, which is an integer value representing the position of the element in the array. Array indices start at 0 for the first element and go up to `length - 1` for the last element, where `length` is the size of the array.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
int firstElement = numbers[0]; // Accessing the first element (index 0)
int thirdElement = numbers[2]; // Accessing the third element (index 2)
```

### Length Property:

Arrays in C# have a `Length` property that returns the total number of elements in the array.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
int arrayLength = numbers.Length; // Returns 5
```

### Multi-Dimensional Arrays:

C# supports multi-dimensional arrays, allowing you to store data in two or more dimensions. The most common types of multi-dimensional arrays are 2-dimensional arrays (matrices) and jagged arrays.

```csharp
// 2-dimensional array (matrix)
int[,] matrix = { { 1, 2, 3 }, { 4, 5, 6 } };

// Jagged array (array of arrays)
int[][] jaggedArray = new int[3][];
jaggedArray[0] = new int[] { 1, 2, 3 };
jaggedArray[1] = new int[] { 4, 5 };
jaggedArray[2] = new int[] { 6, 7, 8 };
```

### Manipulating Arrays:

Arrays in C# can be manipulated using various methods and operations, such as iterating over elements, modifying values, sorting, searching, and performing mathematical operations.

### Summary:

Arrays in C# provide a convenient and efficient way to store and manipulate collections of data. They are versatile and widely used in programming for tasks involving structured data storage and processing. By understanding how to declare, initialize, access, and manipulate arrays, you can leverage this fundamental data structure to solve a wide range of programming problems.

## **1-D, 2-D, 3-D and N-D Array:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Arrays in C# are used to store multiple values of the same type in a contiguous memory location. They provide a convenient way to work with collections of data.

### 1-Dimensional Array:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // 1-D array declaration and initialization
        int[] numbers = new int[] { 1, 2, 3, 4, 5 };

        // Accessing elements of the 1-D array
        Console.WriteLine("1-D Array:");
        for (int i = 0; i < numbers.Length; i++)
        {
            Console.Write(numbers[i] + " ");
        }
    }
}
```

**Output:**
```
1-D Array:
1 2 3 4 5
```

### 2-Dimensional Array:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // 2-D array declaration and initialization
        int[,] matrix = { { 1, 2, 3 }, { 4, 5, 6 } };

        // Accessing elements of the 2-D array
        Console.WriteLine("2-D Array:");
        for (int i = 0; i < matrix.GetLength(0); i++)
        {
            for (int j = 0; j < matrix.GetLength(1); j++)
            {
                Console.Write(matrix[i, j] + " ");
            }
            Console.WriteLine();
        }
    }
}
```

**Output:**
```
2-D Array:
1 2 3 
4 5 6
```

### 3-Dimensional Array:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // 3-D array declaration and initialization
        int[,,] cube = { { { 1, 2 }, { 3, 4 } }, { { 5, 6 }, { 7, 8 } } };

        // Accessing elements of the 3-D array
        Console.WriteLine("3-D Array:");
        for (int i = 0; i < cube.GetLength(0); i++)
        {
            for (int j = 0; j < cube.GetLength(1); j++)
            {
                for (int k = 0; k < cube.GetLength(2); k++)
                {
                    Console.Write(cube[i, j, k] + " ");
                }
                Console.WriteLine();
            }
            Console.WriteLine();
        }
    }
}
```

**Output:**
```
3-D Array:
1 2 
3 4 

5 6 
7 8
```

### N-Dimensional Array:

N-dimensional arrays can be created similarly by adding additional commas and dimensions in the array declaration.

```csharp
int[,,,] nDArray = new int[,,,...]; // N-dimensional array declaration
```

### Scenario:

Consider a scenario where you are developing a chess game. You can use a 2-dimensional array to represent the chessboard where each cell stores information about the piece occupying it. For example, '0' can represent an empty cell, '1' can represent a white pawn, and '-1' can represent a black pawn. You can then manipulate this array to make moves, check for legal moves, and update the display accordingly.

Arrays in C# provide a flexible and efficient way to manage and manipulate multi-dimensional data structures like game boards, matrices, or any other structured data.

## **Jagged Array:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, a jagged array (also known as an array of arrays) is an array whose elements are arrays themselves. Unlike a multi-dimensional array where each row has the same number of columns, in a jagged array, each row can have a different number of columns. This flexibility allows jagged arrays to represent irregular or ragged data structures efficiently.

### Declaration and Initialization:

Jagged arrays are declared and initialized using nested array initialization syntax. Each element of the jagged array is itself an array, and you can specify the size of each inner array independently.

```csharp
// Declaration and initialization of a jagged array
int[][] jaggedArray = new int[3][];

// Initialize individual arrays
jaggedArray[0] = new int[] { 1, 2, 3 };
jaggedArray[1] = new int[] { 4, 5 };
jaggedArray[2] = new int[] { 6, 7, 8 };
```

In the above example:
- `jaggedArray` is a jagged array of type `int[][]`.
- It contains three elements, each of which is an array of integers.
- The size of each inner array can be different.

### Accessing Elements:

You can access elements of a jagged array using multiple indices. Since a jagged array is an array of arrays, you first specify the index of the outer array (the row) and then the index of the inner array (the column).

```csharp
// Accessing elements of a jagged array
int[][] jaggedArray = new int[2][];
jaggedArray[0] = new int[] { 1, 2 };
jaggedArray[1] = new int[] { 3, 4, 5 };

int element = jaggedArray[1][2]; // Accessing element at row 1, column 2 (value: 5)
```

### Iterating Over Elements:

You can iterate over the elements of a jagged array using nested loops. Since each element of the jagged array is an array itself, you need nested loops to traverse both the outer and inner arrays.

```csharp
// Iterating over elements of a jagged array
int[][] jaggedArray = new int[2][];
jaggedArray[0] = new int[] { 1, 2 };
jaggedArray[1] = new int[] { 3, 4, 5 };

for (int i = 0; i < jaggedArray.Length; i++)
{
    for (int j = 0; j < jaggedArray[i].Length; j++)
    {
        Console.Write(jaggedArray[i][j] + " ");
    }
    Console.WriteLine();
}
```

### Usage Scenarios:

Jagged arrays are useful when dealing with data structures that have varying lengths for different elements. Some common scenarios where jagged arrays are used include:
- Representing irregular grids or matrices.
- Storing data of varying sizes, such as lists of different lengths.
- Managing hierarchical or tree-like data structures.

### Summary:

Jagged arrays provide a flexible way to represent and work with collections of data where each element may have a different size. They offer versatility and efficiency in handling irregular data structures and are commonly used in a variety of programming scenarios where fixed-size multi-dimensional arrays may not suffice.

## **Array Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, the `Array` class is a fundamental class that provides methods and properties for working with arrays. It contains static methods for creating, manipulating, sorting, and searching arrays, as well as properties for obtaining information about arrays such as length and rank. The `Array` class is part of the `System` namespace.

### Example:

Let's explore some common methods and properties of the `Array` class with an example:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // Creating and initializing an array
        int[] numbers = { 3, 7, 1, 9, 4, 6, 2, 8, 5 };

        // Displaying the original array
        Console.WriteLine("Original array:");
        DisplayArray(numbers);

        // Sorting the array
        Array.Sort(numbers);

        // Displaying the sorted array
        Console.WriteLine("\nSorted array:");
        DisplayArray(numbers);

        // Searching for an element in the array
        int index = Array.BinarySearch(numbers, 6);
        Console.WriteLine("\nIndex of 6 in the sorted array: " + index);
    }

    static void DisplayArray(int[] arr)
    {
        foreach (int num in arr)
        {
            Console.Write(num + " ");
        }
        Console.WriteLine();
    }
}
```

### Output:

```
Original array:
3 7 1 9 4 6 2 8 5

Sorted array:
1 2 3 4 5 6 7 8 9

Index of 6 in the sorted array: 5
```

### Explanation:

1. **Creation and Initialization:**
   - The `numbers` array is created and initialized with some integer values.

2. **Displaying the Original Array:**
   - The `DisplayArray` method is called to display the original contents of the array.

3. **Sorting the Array:**
   - The `Array.Sort` method is used to sort the elements of the array in ascending order.

4. **Displaying the Sorted Array:**
   - After sorting, the `DisplayArray` method is called again to display the sorted array.

5. **Searching for an Element:**
   - The `Array.BinarySearch` method is used to search for the value `6` in the sorted array. Since the array is sorted, binary search is efficient.

6. **Output:**
   - The output displays the original array, the sorted array, and the index of `6` in the sorted array.

### Summary:

The `Array` class in C# provides powerful methods and properties for working with arrays. It offers functionality for creating, manipulating, sorting, and searching arrays efficiently. By leveraging the methods and properties of the `Array` class, you can perform a wide range of array-related operations with ease and efficiency in your C# programs.

## **Array Methods:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Method               | Description                                                                                                                                                       | Example                                                                                                                                                              |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Array.Clear()`      | Sets a range of elements in the array to zero, false, or null, depending on the element type.                                                                    | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; Array.Clear(numbers, 1, 3); // Clears elements from index 1 to 3 (inclusive) ```                                 |
| `Array.Sort()`       | Sorts the elements of the array in ascending order.                                                                                                              | ```csharp int[] numbers = { 5, 3, 1, 4, 2 }; Array.Sort(numbers); // Sorts the array in ascending order ```                                                          |
| `Array.Reverse()`    | Reverses the order of the elements in the array.                                                                                                                  | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; Array.Reverse(numbers); // Reverses the order of elements in the array ```                                                 |
| `Array.IndexOf()`    | Searches for the specified object and returns the index of the first occurrence within the entire array.                                                          | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int index = Array.IndexOf(numbers, 3); // Returns the index of the first occurrence of 3 (index 2) ```              |
| `Array.BinarySearch()` | Searches for the specified object in a sorted array and returns the index of its occurrence using a binary search algorithm.                                     | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int index = Array.BinarySearch(numbers, 3); // Returns the index of 3 in the sorted array ```                       |
| `Array.Copy()`       | Copies a range of elements from one array to another array.                                                                                                       | ```csharp int[] source = { 1, 2, 3 }; int[] destination = new int[3]; Array.Copy(source, destination, 3); // Copies elements from source to destination array ``` |
| `Array.Resize()`     | Changes the size of the specified array.                                                                                                                          | ```csharp int[] numbers = { 1, 2, 3 }; Array.Resize(ref numbers, 5); // Resizes the array to have a length of 5 ```                                                  |
| `Array.GetLength()`  | Gets the length of the specified dimension in the array.                                                                                                          | ```csharp int[,] matrix = new int[2, 3]; int rows = matrix.GetLength(0); // Gets the number of rows (2) int columns = matrix.GetLength(1); // Gets the number of columns (3) ``` |
| `Array.Rank`         | Gets the rank (number of dimensions) of the array.                                                                                                                | ```csharp int[] numbers = { 1, 2, 3 }; int rank = numbers.Rank; // Gets the rank of the array (1) ```                                                                |
| `Array.CreateInstance()` | Creates a new array with the specified type and dimensions.                                                                                                       | ```csharp Array array = Array.CreateInstance(typeof(int), 3); // Creates a new integer array with length 3 ```                                                       |
| `Array.Exists()`     | Determines whether any element of the array satisfies a condition defined by the specified predicate.                                                            | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; bool exists = Array.Exists(numbers, x => x % 2 == 0); // Checks if any even number exists in the array ```             |
| `Array.TrueForAll()` | Determines whether all elements of the array satisfy a condition defined by the specified predicate.                                                             | ```csharp int[] numbers = { 2, 4, 6, 8, 10 }; bool allEven = Array.TrueForAll(numbers, x => x % 2 == 0); // Checks if all numbers are even in the array ```      |
| `Array.ForEach()`    | Performs the specified action on each element of the array.                                                                                                       | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; Array.ForEach(numbers, x => Console.WriteLine(x)); // Prints each element of the array ```                               |
| `Array.Find()`       | Searches for an element that matches the conditions defined by the specified predicate and returns the first occurrence within the array.                        | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int result = Array.Find(numbers, x => x % 2 == 0); // Finds the first even number in the array (2) ```              |
| `Array.FindAll()`    | Retrieves all the elements that match the conditions defined by the specified predicate.                                                                         | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int[] evenNumbers = Array.FindAll(numbers, x => x % 2 == 0); // Finds all even numbers in the array ```            |
| `Array.FindIndex()`  | Searches for an element that matches the conditions defined by the specified predicate and returns the zero-based index of the first occurrence within the array. | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int index = Array.FindIndex(numbers, x => x % 2 == 0); // Finds the index of the first even number in the array (1) ``` |
| `Array.FindLast()`   | Searches for an element that matches the conditions defined by the specified predicate and returns the last occurrence within the array.                          | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int result = Array.FindLast(numbers, x => x % 2 == 0); // Finds the last even number in the array (4) ```             |
| `Array.FindLastIndex()` |

 Searches for an element that matches the conditions defined by the specified predicate and returns the zero-based index of the last occurrence within the array. | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int index = Array.FindLastIndex(numbers, x => x % 2 == 0); // Finds the index of the last even number in the array (3) ``` |

 ## **Array Properties:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Property             | Description                                                                                                                                                       | Example                                                                                                                                                     |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Length`             | Gets the total number of elements in all dimensions of the array.                                                                                                 | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; int length = numbers.Length; // Gets the length of the array (5) ```                                           |
| `LongLength`         | Gets the total number of elements in all dimensions of the array as a 64-bit integer.                                                                             | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; long longLength = numbers.LongLength; // Gets the long length of the array (5) ```                         |
| `Rank`               | Gets the rank (number of dimensions) of the array.                                                                                                                | ```csharp int[,] matrix = new int[2, 3]; int rank = matrix.Rank; // Gets the rank of the array (2) ```                                                     |
| `IsFixedSize`        | Gets a value indicating whether the array has a fixed size.                                                                                                       | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; bool isFixedSize = Array.IsFixedSize(numbers); // Checks if the array has a fixed size (true) ```         |
| `IsReadOnly`         | Gets a value indicating whether the array is read-only.                                                                                                           | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; bool isReadOnly = Array.IsReadOnly(numbers); // Checks if the array is read-only (false) ```             |
| `IsSynchronized`     | Gets a value indicating whether access to the array is synchronized (thread safe).                                                                                 | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; bool isSynchronized = Array.IsSynchronized(numbers); // Checks if the array is synchronized (false) ``` |
| `SyncRoot`           | Gets an object that can be used to synchronize access to the array.                                                                                               | ```csharp int[] numbers = { 1, 2, 3, 4, 5 }; object syncRoot = Array.SyncRoot(numbers); // Gets the synchronization root of the array ```            |

## **Dynamic Array:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

A dynamic array, also known as a resizable array or a dynamic array list, is a data structure that allows elements to be added or removed dynamically, unlike traditional arrays in C# which have a fixed size. The `List<T>` class in C# provides a dynamic array implementation.

Here's an example of using a dynamic array in C#:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Create a dynamic array using List<T>
        List<int> numbers = new List<int>();

        // Add elements to the dynamic array
        numbers.Add(1);
        numbers.Add(2);
        numbers.Add(3);

        // Output the elements of the dynamic array
        Console.WriteLine("Elements in the dynamic array:");
        foreach (int num in numbers)
        {
            Console.WriteLine(num);
        }

        // Remove an element from the dynamic array
        numbers.Remove(2);

        // Output the updated elements of the dynamic array
        Console.WriteLine("Updated elements in the dynamic array:");
        foreach (int num in numbers)
        {
            Console.WriteLine(num);
        }
    }
}
```

Output:
```
Elements in the dynamic array:
1
2
3
Updated elements in the dynamic array:
1
3
```

In this example, we first create a dynamic array using the `List<T>` class. We add elements to the dynamic array using the `Add()` method, which automatically resizes the array as needed. We then iterate over the elements using a `foreach` loop to output them. After that, we remove an element from the dynamic array using the `Remove()` method. Finally, we iterate over the updated dynamic array again to show the changes.

Dynamic arrays provide flexibility by automatically resizing themselves as elements are added or removed. This makes them suitable for scenarios where the size of the data structure may vary during runtime.

## **ArrayList:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

`ArrayList` is a class in C# that provides a resizable array implementation. It belongs to the `System.Collections` namespace. `ArrayList` dynamically resizes itself as elements are added or removed, making it suitable for scenarios where the size of the data structure may vary during runtime.

Here's an example of using `ArrayList` in C#:

```csharp
using System;
using System.Collections;

class Program
{
    static void Main()
    {
        // Create an ArrayList
        ArrayList list = new ArrayList();

        // Add elements to the ArrayList
        list.Add(1);
        list.Add("two");
        list.Add(3.0);

        // Output the elements of the ArrayList
        Console.WriteLine("Elements in the ArrayList:");
        foreach (var item in list)
        {
            Console.WriteLine(item);
        }

        // Remove an element from the ArrayList
        list.Remove("two");

        // Output the updated elements of the ArrayList
        Console.WriteLine("Updated elements in the ArrayList:");
        foreach (var item in list)
        {
            Console.WriteLine(item);
        }
    }
}
```

Output:
```
Elements in the ArrayList:
1
two
3
Updated elements in the ArrayList:
1
3
```

In this example, we first create an `ArrayList` and add elements of different types (integer, string, and double) using the `Add()` method. We then iterate over the elements using a `foreach` loop to output them. After that, we remove an element from the `ArrayList` using the `Remove()` method. Finally, we iterate over the updated `ArrayList` again to show the changes.

Benefits of `ArrayList`:
1. **Dynamic Resizing**: `ArrayList` automatically resizes itself as elements are added or removed, providing flexibility.
2. **Heterogeneous Elements**: `ArrayList` can store elements of different types, allowing for flexibility in data storage.

Limitations of `ArrayList`:
1. **Boxing and Unboxing**: Since `ArrayList` stores elements as objects, value types are boxed when added to the `ArrayList` and unboxed when retrieved, which can impact performance.
2. **Type Safety**: `ArrayList` does not provide type safety at compile time, increasing the risk of runtime errors if incorrect types are used.
3. **No Generic Support**: `ArrayList` does not support generics, so type checking is not enforced, leading to potential errors and inefficiencies.
4. **Inefficient to multi-dimensional array**: `ArrayList` cannot be utilized for multi-dimenstional array.

Overall, while `ArrayList` provides flexibility and dynamic resizing, it lacks type safety and may incur performance overhead due to boxing and unboxing. In modern C# development, `List<T>` from the `System.Collections.Generic` namespace is preferred over `ArrayList` due to its type safety and better performance.

## **ArrayList Methods:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Method                        | Description                                                                                                                                                                                         |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Add(object)`                 | Adds an object to the end of the `ArrayList`.                                                                                                                                                      |
| `AddRange(ICollection)`      | Adds the elements of the specified collection to the end of the `ArrayList`.                                                                                                                       |
| `BinarySearch(object)`       | Searches for the specified object and returns the zero-based index of the first occurrence within the entire `ArrayList`.                                                                           |
| `Clear()`                     | Removes all elements from the `ArrayList`.                                                                                                                                                         |
| `Clone()`                     | Creates a shallow copy of the `ArrayList`.                                                                                                                                                         |
| `Contains(object)`           | Determines whether the `ArrayList` contains the specified object.                                                                                                                                 |
| `CopyTo(Array)`              | Copies the elements of the `ArrayList` to a new array.                                                                                                                                            |
| `GetEnumerator()`            | Returns an enumerator that iterates through the `ArrayList`.                                                                                                                                      |
| `GetRange(int, int)`         | Returns an `ArrayList` containing a range of elements from the original `ArrayList`.                                                                                                              |
| `IndexOf(object)`            | Searches for the specified object and returns the zero-based index of the first occurrence within the entire `ArrayList`.                                                                           |
| `IndexOf(object, int)`       | Searches for the specified object and returns the zero-based index of the first occurrence within the range of elements in the `ArrayList` that starts at the specified index.                      |
| `Insert(int, object)`        | Inserts an element into the `ArrayList` at the specified index.                                                                                                                                   |
| `InsertRange(int, ICollection)` | Inserts the elements of a collection into the `ArrayList` at the specified index.                                                                                                                  |
| `LastIndexOf(object)`        | Searches for the specified object and returns the zero-based index of the last occurrence within the entire `ArrayList`.                                                                            |
| `LastIndexOf(object, int)`   | Searches for the specified object and returns the zero-based index of the last occurrence within the range of elements in the `ArrayList` that ends at the specified index.                         |
| `Remove(object)`             | Removes the first occurrence of the specified object from the `ArrayList`.                                                                                                                         |
| `RemoveAt(int)`              | Removes the element at the specified index of the `ArrayList`.                                                                                                                                    |
| `RemoveRange(int, int)`      | Removes a range of elements from the `ArrayList`.                                                                                                                                                 |
| `Reverse()`                  | Reverses the order of the elements in the entire `ArrayList`.                                                                                                                                     |
| `Sort()`                     | Sorts the elements in the entire `ArrayList`.                                                                                                                                                     |
| `ToArray()`                  | Copies the elements of the `ArrayList` to a new array.                                                                                                                                            |
| `ToArray(Type)`              | Copies the elements of the `ArrayList` to a new array of the specified element type.                                                                                                              |
| `TrimToSize()`               | Sets the capacity of the `ArrayList` to the actual number of elements it contains.                                                                                                                |

These methods offer a wide range of functionalities for manipulating and working with the elements stored in an `ArrayList`. They provide operations for adding, removing, searching, sorting, and manipulating elements, making `ArrayList` a versatile choice for various scenarios.

## **ArrayList Properties:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a detailed explanation of the `ArrayList` properties in C# presented in a tabular format:

| Property          | Description                                                                                                                                                     |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Capacity`        | Gets or sets the number of elements that the `ArrayList` can contain.                                                                                           |
| `Count`           | Gets the number of elements actually contained in the `ArrayList`.                                                                                              |
| `IsFixedSize`     | Gets a value indicating whether the `ArrayList` has a fixed size.                                                                                               |
| `IsReadOnly`      | Gets a value indicating whether the `ArrayList` is read-only.                                                                                                    |
| `IsSynchronized`  | Gets a value indicating whether access to the `ArrayList` is synchronized (thread-safe).                                                                                      |
| `SyncRoot`        | Gets an object that can be used to synchronize access to the `ArrayList`.                                                                                        |

These properties provide various information and capabilities for working with `ArrayList` objects:

- **Capacity**: Represents the number of elements that the `ArrayList` can currently store without resizing. When the number of elements exceeds the capacity, the `ArrayList` automatically reallocates space to accommodate more elements.
  
- **Count**: Indicates the number of elements currently stored in the `ArrayList`.

- **IsFixedSize**: Indicates whether the size of the `ArrayList` is fixed. If `true`, the `ArrayList` cannot be resized, and attempting to add or remove elements will result in an exception.

- **IsReadOnly**: Indicates whether the `ArrayList` is read-only. If `true`, elements cannot be added, removed, or modified.

- **IsSynchronized**: Indicates whether access to the `ArrayList` is synchronized, meaning that it is thread-safe. If `true`, the `ArrayList` can be safely accessed from multiple threads concurrently.

- **SyncRoot**: Provides an object that can be used to synchronize access to the `ArrayList` when accessed by multiple threads. It is recommended to use explicit locking mechanisms instead of relying solely on `SyncRoot` for thread safety.

These properties offer valuable information about the state and behavior of `ArrayList` instances and enable developers to manage and manipulate them effectively.

## **ArrayList Constructors:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a detailed explanation of the `ArrayList` constructors in C# presented in a tabular format:

| Constructor                                | Description                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ArrayList()`                             | Initializes a new instance of the `ArrayList` class that is empty and has the default initial capacity.                                                                                                                                                                                                                                                          |
| `ArrayList(ICollection)`                  | Initializes a new instance of the `ArrayList` class containing the elements of the specified collection.                                                                                                                                                                                                                                                          |
| `ArrayList(int)`                          | Initializes a new instance of the `ArrayList` class that is empty and has the specified initial capacity.                                                                                                                                                                                                                                                        |
| `ArrayList(int, IEqualityComparer)`       | Initializes a new instance of the `ArrayList` class that is empty, has the specified initial capacity, and uses the specified equality comparer for the elements.                                                                                                                                                                                               |
| `ArrayList(ArrayList)`                    | Initializes a new instance of the `ArrayList` class that contains elements copied from the specified `ArrayList`.                                                                                                                                                                                                                                                 |
| `ArrayList(int, ArrayList)`               | Initializes a new instance of the `ArrayList` class that is empty, has the specified initial capacity, and contains elements copied from the specified `ArrayList`.                                                                                                                                                                                             |
| `ArrayList(int, int)`                     | Initializes a new instance of the `ArrayList` class that is empty, has the specified initial capacity, and increases its capacity in increments of the specified value.                                                                                                                                                                                          |
| `ArrayList(SerializationInfo, StreamingContext)` | Initializes a new instance of the `ArrayList` class with serialized data.                                                                                                                                                                                                                                                                                     |

These constructors provide various ways to create instances of the `ArrayList` class:

- **Default constructor**: Creates an empty `ArrayList` with the default initial capacity.
- **Constructor with ICollection parameter**: Initializes an `ArrayList` with the elements of a specified collection.
- **Constructor with int parameter**: Creates an empty `ArrayList` with the specified initial capacity.
- **Constructor with int and IEqualityComparer parameters**: Creates an `ArrayList` with the specified initial capacity and uses the specified equality comparer for the elements.
- **Constructor with ArrayList parameter**: Creates an `ArrayList` with the elements copied from a specified `ArrayList`.
- **Constructor with int and ArrayList parameters**: Creates an `ArrayList` with the specified initial capacity and copies elements from a specified `ArrayList`.
- **Constructor with int and int parameters**: Creates an `ArrayList` with the specified initial capacity and increases its capacity in increments of the specified value.
- **Constructor with SerializationInfo and StreamingContext parameters**: Initializes an `ArrayList` with serialized data.

These constructors offer flexibility in creating and initializing `ArrayList` instances based on different requirements and scenarios.

## **Array Vs ArrayList:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a detailed comparison of `Array` and `ArrayList` in C#:

| Feature                 | Array                                                  | ArrayList                                              |
|-------------------------|--------------------------------------------------------|--------------------------------------------------------|
| Namespace               | `System`                                               | `System.Collections`                                   |
| Type safety             | Compile-time type safety                              | Runtime type safety                                    |
| Dynamic resizing        | No                                                     | Yes                                                    |
| Heterogeneous elements  | No                                                     | Yes                                                    |
| Performance             | Better (direct memory access)                         | Worse (due to boxing/unboxing)                         |
| Accessing elements      | Direct indexing                                        | Indexing or iteration                                  |
| Length/Size             | Fixed size                                             | Dynamic size                                           |
| Generic support         | No                                                     | No                                                     |
| Usage                   | Typically used when the size is known and fixed       | Typically used when size may vary or heterogeneous    |

**Array:**
- Arrays have a fixed size determined at compile time.
- They provide direct memory access, resulting in better performance.
- Arrays are type-safe at compile time, ensuring type correctness.
- Arrays do not support dynamic resizing or heterogeneous elements.

**ArrayList:**
- ArrayLists have a dynamic size and can grow or shrink as needed.
- They store elements as objects, resulting in boxing/unboxing overhead and potentially slower performance.
- ArrayLists are not type-safe at compile time, allowing heterogeneous elements.
- ArrayLists support dynamic resizing and can hold elements of different types.

**Usage Scenarios:**
- Use arrays when the size is known and fixed, and when type safety and direct memory access are important.
- Use ArrayLists when the size may vary or when storing heterogeneous elements.

In modern C# development, `List<T>` from the `System.Collections.Generic` namespace is preferred over `ArrayList` due to its type safety, better performance, and support for generics.


## **Arrayist Vs List:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a comparison between `ArrayList` and `List<T>` in tabular form:

| Feature                               | `ArrayList`                                        | `List<T>`                                      |
|---------------------------------------|----------------------------------------------------|------------------------------------------------|
| Type Safety                           | Not type-safe. Elements can be of any type.       | Type-safe. Elements are of a specific type `T`.|
| Performance                           | Poor performance due to boxing/unboxing.           | Better performance as it avoids boxing/unboxing.|
| Capacity Management                   | Capacity needs to be managed manually.             | Capacity is managed automatically.             |
| Resizing Behavior                     | Resizes dynamically by doubling its capacity.      | Resizes dynamically by 50% of current capacity.|
| Type Inference                        | No type inference.                                 | Supports type inference with generics.         |
| Syntax                                | Uses non-generic syntax.                           | Uses generic syntax.                           |
| Memory Usage                          | Consumes more memory due to boxing.                | Consumes less memory as it's type-safe.        |
| Compatibility                         | Compatible with .NET Framework versions prior to 2.0. | Introduced in .NET Framework 2.0.            |
| Usage                                 | Mostly used in legacy code or scenarios requiring compatibility with older versions. | Preferred choice for new development and modern scenarios. |

In summary, `List<T>` offers better type safety, performance, and syntax compared to `ArrayList`. It is the preferred choice for new development and modern scenarios due to its type safety, better performance, and compatibility with generics. However, `ArrayList` may still be used in scenarios requiring compatibility with older .NET Framework versions or in legacy codebases.
