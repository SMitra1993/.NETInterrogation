# Collections & Generics ❤🍕

**Links:**

- [List](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [Sorted List](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#sorted-list-)
- [List Vs SortedList](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-vs-sortedlist-)
- [HashSet](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#hashset-)
- [List Vs HashSet](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-vs-hashset-)
- [SortedSet](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#sortedset-)
- [HashSet Vs SortedSet](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#hashset-vs-sortedset-)
- [Dictionary](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#dictionary-)
- [List Vs Dictionary](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-vs-dictionary-)
- [SortedDictionary](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#sorteddictionary-)
- [Dictionary Vs SortedDictionary](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#dictionary-vs-sorteddictionary-)
- [HashTable](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#hashtable-)
- [Dictionary Vs HashTable](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#dictionary-vs-hashtable-)
- [Stack](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#stack-)
- [Queue](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#queue-)
- [Linked List](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#linked-list-)
- [SortedDictionary Vs SortedList](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#sorteddictionary-vs-sortedlist-)
- [List Vs Enumerable](https://github.com/SMitra1993/.NETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-vs-ienumerable-)

## **List:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

List is a generic collection class in C# that represents a dynamic list of elements. It provides functionalities to add, remove, and access elements by index. Unlike arrays, lists can dynamically resize themselves to accommodate additional elements as needed.

Here's an example demonstrating the usage of List:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new List instance
        List<string> myList = new List<string>();

        // Add elements to the list
        myList.Add("Apple");
        myList.Add("Banana");
        myList.Add("Orange");

        // Display the contents of the list
        foreach (string fruit in myList)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

Output:
```
Apple
Banana
Orange
```

In this example:
- We create a new instance of List called `myList` that stores strings.
- We add elements "Apple", "Banana", and "Orange" to the list using the `Add` method.
- We iterate over the elements in the list using a foreach loop and display each element.

Lists provide a flexible and efficient way to store and manipulate collections of items. They offer various methods for adding, removing, and accessing elements, making them widely used in C# programming for managing collections of data.

## **Sorted List:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

SortedList is a collection class in C# that represents a collection of key/value pairs that are sorted by the keys. It maintains the items in sorted order based on the keys, allowing for efficient searching and retrieval operations.

Here's an example demonstrating the usage of SortedList:

```csharp
using System;
using System.Collections;

class Program
{
    static void Main(string[] args)
    {
        // Create a new SortedList instance
        SortedList sortedList = new SortedList();

        // Add items to the SortedList
        sortedList.Add("John", 25);
        sortedList.Add("Alice", 30);
        sortedList.Add("Bob", 20);

        // Display the contents of the SortedList
        foreach (DictionaryEntry entry in sortedList)
        {
            Console.WriteLine($"Key: {entry.Key}, Value: {entry.Value}");
        }
    }
}
```

Output:
```
Key: Alice, Value: 30
Key: Bob, Value: 20
Key: John, Value: 25
```

In this example:
- We create a new instance of SortedList called `sortedList`.
- We add key/value pairs to the SortedList using the `Add` method.
- The keys are automatically sorted in ascending order.
- We iterate over the items in the SortedList using a foreach loop and display the key/value pairs.

SortedList provides efficient search operations based on the keys, making it suitable for scenarios where items need to be sorted and retrieved based on their keys. It is implemented as a combination of a dynamic array and a binary search tree, ensuring efficient insertion, removal, and retrieval operations while maintaining sorted order.

## **List Vs SortedList:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a comparison between List and SortedList in tabular form:

| Feature                | List                                | SortedList                                 |
|------------------------|-------------------------------------|--------------------------------------------|
| Ordering               | Does not maintain any specific order. | Maintains elements in sorted order based on keys. |
| Performance            | Operations like Add, Remove, and Access have O(1) time complexity. | Operations like Add, Remove, and Access have O(log n) time complexity due to sorting. |
| Sorting                | Not automatically sorted.            | Automatically sorted based on keys.       |
| Memory Usage           | Less memory overhead since it doesn't maintain sorting. | Slightly more memory overhead due to sorting. |
| Retrieval Efficiency   | Accessing elements by index has O(1) time complexity. | Accessing elements by key has O(log n) time complexity. |
| Flexibility            | Offers flexibility in adding, removing, and accessing elements. | Offers efficient searching and retrieval operations based on keys. |
| Use Cases              | Suitable for scenarios where ordering is not important or where elements are frequently added or removed. | Suitable for scenarios where elements need to be maintained in sorted order based on keys and efficient searching is required. |

In summary, List is more suitable for scenarios where ordering is not important or where elements are frequently added or removed, while SortedList is suitable for scenarios where elements need to be maintained in sorted order based on keys and efficient searching is required.

## **HashSet:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

HashSet is a collection class in C# that represents a set of unique elements. It does not allow duplicate elements, and it does not maintain the order of elements. HashSet provides fast lookup operations, making it suitable for scenarios where uniqueness of elements and efficient membership testing are required.

Here's an example demonstrating the usage of HashSet:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new HashSet instance
        HashSet<string> mySet = new HashSet<string>();

        // Add elements to the set
        mySet.Add("Apple");
        mySet.Add("Banana");
        mySet.Add("Orange");
        mySet.Add("Apple"); // This will be ignored since it's a duplicate

        // Display the contents of the set
        foreach (string fruit in mySet)
        {
            Console.WriteLine(fruit);
        }
    }
}
```

Output:
```
Orange
Banana
Apple
```

In this example:
- We create a new instance of HashSet called `mySet` that stores strings.
- We add elements "Apple", "Banana", "Orange", and "Apple" to the set using the `Add` method. Note that the duplicate element "Apple" is automatically ignored.
- We iterate over the elements in the set using a foreach loop and display each unique element.

HashSet provides efficient operations for adding, removing, and testing for membership of elements. It internally uses a hash table to store elements, allowing for fast lookup operations. Additionally, HashSet provides various set operations such as union, intersection, and difference, making it a versatile choice for working with sets of data.

## **List Vs HashSet:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a detailed comparison between List and HashSet in tabular form:

| Feature                | List                                 | HashSet                                      |
|------------------------|--------------------------------------|----------------------------------------------|
| Ordering               | Maintains the order of elements.     | Does not maintain any specific order.       |
| Duplicates             | Allows duplicate elements.           | Does not allow duplicate elements.          |
| Memory Usage           | Slightly less memory overhead.       | Slightly more memory overhead due to hashing.|
| Retrieval Efficiency   | Accessing elements by index has O(1) time complexity. | Accessing elements has O(1) time complexity on average. |
| Membership Testing     | Slower membership testing compared to HashSet. | Faster membership testing due to hashing.   |
| Use Cases              | Suitable for scenarios where ordering is important or where duplicates are allowed. | Suitable for scenarios where uniqueness of elements and efficient membership testing are required. |
| Example                | `List<int> numbers = new List<int>();` | `HashSet<int> uniqueNumbers = new HashSet<int>();` |

In summary, List is suitable for scenarios where ordering is important or where duplicates are allowed, while HashSet is suitable for scenarios where uniqueness of elements and efficient membership testing are required. HashSet provides faster membership testing and does not allow duplicate elements, making it more efficient for scenarios requiring uniqueness. However, it does not maintain the order of elements like List does.

## **SortedSet:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

SortedSet is a collection class in C# that represents a set of unique elements sorted in ascending order. It is similar to HashSet but maintains the elements in sorted order based on their natural ordering or using a custom comparer.

Here's an example demonstrating the usage of SortedSet:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new SortedSet instance
        SortedSet<int> mySet = new SortedSet<int>();

        // Add elements to the set
        mySet.Add(5);
        mySet.Add(2);
        mySet.Add(8);
        mySet.Add(3);

        // Display the contents of the set
        foreach (int number in mySet)
        {
            Console.WriteLine(number);
        }
    }
}
```

Output:
```
2
3
5
8
```

In this example:
- We create a new instance of SortedSet called `mySet` that stores integers.
- We add elements 5, 2, 8, and 3 to the set using the `Add` method.
- The elements are automatically sorted in ascending order.
- We iterate over the elements in the set using a foreach loop and display each element.

SortedSet provides efficient operations for adding, removing, and testing for membership of elements while maintaining them in sorted order. It is particularly useful in scenarios where elements need to be sorted and uniqueness is required.

## **HashSet Vs SortedSet:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a detailed comparison between HashSet and SortedSet in tabular form:

| Feature                | HashSet                                       | SortedSet                                      |
|------------------------|-----------------------------------------------|------------------------------------------------|
| Ordering               | Does not maintain any specific order.         | Maintains elements in sorted order.            |
| Duplicates             | Does not allow duplicate elements.            | Does not allow duplicate elements.            |
| Memory Usage           | Slightly less memory overhead.                | Slightly more memory overhead due to sorting. |
| Retrieval Efficiency   | Accessing elements has O(1) time complexity on average. | Accessing elements has O(log n) time complexity. |
| Sorting                | Not automatically sorted.                     | Automatically sorted based on natural ordering or custom comparer. |
| Use Cases              | Suitable for scenarios where uniqueness of elements is required and order is not important. | Suitable for scenarios where uniqueness of elements is required and maintaining elements in sorted order is necessary. |
| Example                | `HashSet<int> uniqueNumbers = new HashSet<int>();` | `SortedSet<int> sortedNumbers = new SortedSet<int>();` |

In summary, HashSet is suitable for scenarios where uniqueness of elements is required and the order is not important, while SortedSet is suitable for scenarios where uniqueness of elements is required and maintaining elements in sorted order is necessary. HashSet provides faster membership testing but does not maintain order, while SortedSet maintains elements in sorted order but has slightly slower access times due to sorting.

## **Dictionary:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Dictionary is a collection class in C# that represents a collection of key-value pairs. It provides fast lookup operations based on keys and allows you to store and retrieve values associated with unique keys. Each key in a dictionary must be unique, and it provides efficient methods for adding, removing, and accessing elements.

Here's an example demonstrating the usage of Dictionary:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new Dictionary instance
        Dictionary<string, int> myDictionary = new Dictionary<string, int>();

        // Add elements to the dictionary
        myDictionary.Add("Apple", 10);
        myDictionary.Add("Banana", 20);
        myDictionary.Add("Orange", 15);

        // Access elements in the dictionary
        Console.WriteLine("Number of Apples: " + myDictionary["Apple"]);
        Console.WriteLine("Number of Bananas: " + myDictionary["Banana"]);
        Console.WriteLine("Number of Oranges: " + myDictionary["Orange"]);

        // Modify an element in the dictionary
        myDictionary["Banana"] = 25;

        // Remove an element from the dictionary
        myDictionary.Remove("Orange");

        // Display all key-value pairs in the dictionary
        foreach (KeyValuePair<string, int> pair in myDictionary)
        {
            Console.WriteLine("Key: " + pair.Key + ", Value: " + pair.Value);
        }
    }
}
```

Output:
```
Number of Apples: 10
Number of Bananas: 20
Number of Oranges: 15
Key: Apple, Value: 10
Key: Banana, Value: 25
```

In this example:
- We create a new instance of Dictionary called `myDictionary` that maps strings (fruit names) to integers (quantities).
- We add key-value pairs ("Apple", 10), ("Banana", 20), and ("Orange", 15) to the dictionary using the `Add` method.
- We access elements in the dictionary using square brackets (`[]`) and print their values.
- We modify the value associated with the key "Banana" to 25.
- We remove the element with the key "Orange" from the dictionary using the `Remove` method.
- We iterate over all key-value pairs in the dictionary using a foreach loop and print each key-value pair.

Dictionaries provide efficient lookup operations based on keys, making them suitable for scenarios where fast retrieval of values based on keys is required. They are commonly used for caching, storing configuration settings, and mapping identifiers to values.

## **List Vs Dictionary:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a detailed comparison between List and Dictionary in tabular form:

| Feature                | List                                             | Dictionary                                       |
|------------------------|--------------------------------------------------|--------------------------------------------------|
| Purpose                | Stores a collection of elements.                 | Stores key-value pairs.                          |
| Accessing Elements     | Accessed by index.                               | Accessed by key.                                 |
| Element Retrieval      | O(1) time complexity for accessing elements by index. | O(1) time complexity for accessing elements by key on average. |
| Ordering               | Maintains the order of elements.                | Does not maintain any specific order.            |
| Duplicates             | Allows duplicate elements.                       | Keys must be unique.                             |
| Memory Usage           | Lower memory overhead.                           | Slightly higher memory overhead due to key-value pairs. |
| Use Cases              | Suitable for scenarios where ordered collection of elements is required or duplicates are allowed. | Suitable for scenarios where efficient key-based lookup is required or key-value mapping is necessary. |
| Example                | `List<int> numbers = new List<int>();`           | `Dictionary<string, int> keyValuePairs = new Dictionary<string, int>();` |

In summary, List is suitable for scenarios where ordered collection of elements is required or duplicates are allowed, while Dictionary is suitable for scenarios where efficient key-based lookup is required or key-value mapping is necessary. List provides fast access by index and maintains the order of elements, while Dictionary provides fast access by key but does not maintain any specific order.

## **SortedDictionary:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

SortedDictionary is a collection class in C# that represents a collection of key-value pairs sorted by keys. It is similar to Dictionary but maintains its elements in sorted order based on the keys. Each key in a SortedDictionary must be unique, and it provides efficient methods for adding, removing, and accessing elements while maintaining them in sorted order.

Here's an example demonstrating the usage of SortedDictionary:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new SortedDictionary instance
        SortedDictionary<string, int> myDictionary = new SortedDictionary<string, int>();

        // Add elements to the dictionary
        myDictionary.Add("Apple", 10);
        myDictionary.Add("Banana", 20);
        myDictionary.Add("Orange", 15);

        // Access elements in the dictionary
        Console.WriteLine("Number of Apples: " + myDictionary["Apple"]);
        Console.WriteLine("Number of Bananas: " + myDictionary["Banana"]);
        Console.WriteLine("Number of Oranges: " + myDictionary["Orange"]);

        // Modify an element in the dictionary
        myDictionary["Banana"] = 25;

        // Remove an element from the dictionary
        myDictionary.Remove("Orange");

        // Display all key-value pairs in the dictionary
        foreach (KeyValuePair<string, int> pair in myDictionary)
        {
            Console.WriteLine("Key: " + pair.Key + ", Value: " + pair.Value);
        }
    }
}
```

Output:
```
Number of Apples: 10
Number of Bananas: 25
Key: Apple, Value: 10
Key: Banana, Value: 25
```

In this example:
- We create a new instance of SortedDictionary called `myDictionary` that maps strings (fruit names) to integers (quantities).
- We add key-value pairs ("Apple", 10), ("Banana", 20), and ("Orange", 15) to the dictionary using the `Add` method.
- The elements are automatically sorted in ascending order based on the keys.
- We access elements in the dictionary using square brackets (`[]`) and print their values.
- We modify the value associated with the key "Banana" to 25.
- We remove the element with the key "Orange" from the dictionary using the `Remove` method.
- We iterate over all key-value pairs in the dictionary using a foreach loop and print each key-value pair.

SortedDictionary provides efficient operations for adding, removing, and accessing elements while maintaining them in sorted order. It is particularly useful in scenarios where elements need to be sorted by keys and uniqueness is required.

## **Dictionary Vs SortedDictionary:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a detailed comparison between Dictionary and SortedDictionary in tabular form:

| Feature                | Dictionary                                      | SortedDictionary                                |
|------------------------|-------------------------------------------------|-------------------------------------------------|
| Ordering               | Does not maintain any specific order.           | Maintains elements in sorted order based on keys. |
| Duplicates             | Does not allow duplicate keys.                 | Does not allow duplicate keys.                 |
| Element Retrieval      | O(1) time complexity for accessing elements by key on average. | O(log n) time complexity for accessing elements by key. |
| Memory Usage           | Slightly less memory overhead.                  | Slightly more memory overhead due to sorting.  |
| Use Cases              | Suitable for scenarios where order is not important and fast key-based lookup is required. | Suitable for scenarios where elements need to be sorted by keys and efficient key-based lookup is required. |
| Example                | `Dictionary<string, int> keyValuePairs = new Dictionary<string, int>();` | `SortedDictionary<string, int> keyValuePairs = new SortedDictionary<string, int>();` |

In summary, Dictionary is suitable for scenarios where order is not important and fast key-based lookup is required, while SortedDictionary is suitable for scenarios where elements need to be sorted by keys and efficient key-based lookup is required. Dictionary provides faster access by key on average but does not maintain order, while SortedDictionary maintains elements in sorted order based on keys but has slightly slower access times due to sorting.

## **HashTable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Hashtable is a collection class in C# that represents a collection of key-value pairs. It is similar to Dictionary but is a legacy class and is not type-safe. Hashtable stores key-value pairs in a hash table data structure, providing fast lookup operations based on keys. Each key in a Hashtable must be unique, and it provides efficient methods for adding, removing, and accessing elements.

Here's an example demonstrating the usage of Hashtable:

```csharp
using System;
using System.Collections;

class Program
{
    static void Main(string[] args)
    {
        // Create a new Hashtable instance
        Hashtable myHashtable = new Hashtable();

        // Add elements to the hashtable
        myHashtable.Add("Apple", 10);
        myHashtable.Add("Banana", 20);
        myHashtable.Add("Orange", 15);

        // Access elements in the hashtable
        Console.WriteLine("Number of Apples: " + myHashtable["Apple"]);
        Console.WriteLine("Number of Bananas: " + myHashtable["Banana"]);
        Console.WriteLine("Number of Oranges: " + myHashtable["Orange"]);

        // Modify an element in the hashtable
        myHashtable["Banana"] = 25;

        // Remove an element from the hashtable
        myHashtable.Remove("Orange");

        // Display all key-value pairs in the hashtable
        foreach (DictionaryEntry entry in myHashtable)
        {
            Console.WriteLine("Key: " + entry.Key + ", Value: " + entry.Value);
        }
    }
}
```

Output:
```
Number of Apples: 10
Number of Bananas: 20
Number of Oranges: 15
Key: Banana, Value: 25
Key: Apple, Value: 10
```

In this example:
- We create a new instance of Hashtable called `myHashtable`.
- We add key-value pairs ("Apple", 10), ("Banana", 20), and ("Orange", 15) to the hashtable using the `Add` method.
- We access elements in the hashtable using square brackets (`[]`) and print their values.
- We modify the value associated with the key "Banana" to 25.
- We remove the element with the key "Orange" from the hashtable using the `Remove` method.
- We iterate over all key-value pairs in the hashtable using a foreach loop and print each key-value pair.

Hashtable provides efficient operations for adding, removing, and accessing elements based on keys. However, it is not type-safe and does not preserve the order of elements. Hashtable is primarily used in legacy code and is recommended to use the generic Dictionary class for type-safe collections.

## **Dictionary Vs HashTable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a detailed comparison between Dictionary and Hashtable in tabular form:

| Feature                | Dictionary                                      | Hashtable                                       |
|------------------------|-------------------------------------------------|-------------------------------------------------|
| Type Safety            | Type-safe collection class.                    | Not type-safe.                                  |
| Ordering               | Does not maintain any specific order.           | Does not maintain any specific order.           |
| Duplicates             | Does not allow duplicate keys.                 | Does not allow duplicate keys.                 |
| Element Retrieval      | O(1) time complexity for accessing elements by key on average. | O(1) time complexity for accessing elements by key on average. |
| Memory Usage           | Slightly less memory overhead.                  | Slightly more memory overhead.                  |
| Use Cases              | Suitable for modern applications where type safety is important and fast key-based lookup is required. | Used in legacy code or scenarios where type safety is not critical and fast key-based lookup is required. |
| Example                | `Dictionary<string, int> keyValuePairs = new Dictionary<string, int>();` | `Hashtable myHashtable = new Hashtable();`      |

In summary, Dictionary is a type-safe collection class suitable for modern applications where type safety is important and fast key-based lookup is required. Hashtable, on the other hand, is not type-safe and is used in legacy code or scenarios where type safety is not critical and fast key-based lookup is required. Both collections provide efficient operations for adding, removing, and accessing elements based on keys, but Dictionary is recommended for most modern applications due to its type safety and improved syntax.

## **Stack:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

In C#, a Stack is a collection class that represents a Last-In-First-Out (LIFO) data structure, meaning that the last element added to the stack is the first one to be removed. It provides operations for adding elements to the top of the stack (push) and removing elements from the top of the stack (pop). Stack is commonly used in scenarios where elements need to be processed in the reverse order of their addition.

Here's an example demonstrating the usage of Stack:

```csharp
using System;
using System.Collections;

class Program
{
    static void Main(string[] args)
    {
        // Create a new Stack instance
        Stack myStack = new Stack();

        // Push elements onto the stack
        myStack.Push("Apple");
        myStack.Push("Banana");
        myStack.Push("Orange");

        // Peek at the top element of the stack (without removing it)
        Console.WriteLine("Top element of the stack: " + myStack.Peek());

        // Pop elements from the stack and print them
        Console.WriteLine("Popping elements from the stack:");
        while (myStack.Count > 0)
        {
            Console.WriteLine(myStack.Pop());
        }
    }
}
```

Output:
```
Top element of the stack: Orange
Popping elements from the stack:
Orange
Banana
Apple
```

In this example:
- We create a new instance of Stack called `myStack`.
- We push elements ("Apple", "Banana", "Orange") onto the stack using the `Push` method.
- We peek at the top element of the stack (without removing it) using the `Peek` method and print its value.
- We pop elements from the stack using the `Pop` method and print them. As expected in a stack, the elements are popped in reverse order of their addition.

Stack provides efficient operations for adding and removing elements from the top of the stack. It is commonly used in scenarios such as expression evaluation, backtracking algorithms, and maintaining function call stacks.

## **Queue:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

In C#, a Queue is a collection class that represents a First-In-First-Out (FIFO) data structure, meaning that the first element added to the queue is the first one to be removed. It provides operations for adding elements to the end of the queue (enqueue) and removing elements from the beginning of the queue (dequeue). Queue is commonly used in scenarios where elements need to be processed in the same order as their addition.

Here's an example demonstrating the usage of Queue:

```csharp
using System;
using System.Collections;

class Program
{
    static void Main(string[] args)
    {
        // Create a new Queue instance
        Queue myQueue = new Queue();

        // Enqueue elements into the queue
        myQueue.Enqueue("Apple");
        myQueue.Enqueue("Banana");
        myQueue.Enqueue("Orange");

        // Peek at the front element of the queue (without removing it)
        Console.WriteLine("Front element of the queue: " + myQueue.Peek());

        // Dequeue elements from the queue and print them
        Console.WriteLine("Dequeuing elements from the queue:");
        while (myQueue.Count > 0)
        {
            Console.WriteLine(myQueue.Dequeue());
        }
    }
}
```

Output:
```
Front element of the queue: Apple
Dequeuing elements from the queue:
Apple
Banana
Orange
```

In this example:
- We create a new instance of Queue called `myQueue`.
- We enqueue elements ("Apple", "Banana", "Orange") into the queue using the `Enqueue` method.
- We peek at the front element of the queue (without removing it) using the `Peek` method and print its value.
- We dequeue elements from the queue using the `Dequeue` method and print them. As expected in a queue, the elements are dequeued in the same order as their addition.

Queue provides efficient operations for adding and removing elements from the beginning and end of the queue, respectively. It is commonly used in scenarios such as job scheduling, breadth-first search algorithms, and handling tasks in the order they were received.

## **Linked List:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

In C#, a Linked List is a collection class that represents a linear data structure where each element (node) contains a reference to the next element in the sequence. Unlike arrays, linked lists do not have a fixed size, and elements can be dynamically added or removed at any position within the list. Linked lists are commonly used when frequent insertion or deletion of elements is required, as they provide efficient operations for these operations.

Here's an example demonstrating the usage of Linked List:

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        // Create a new LinkedList instance
        LinkedList<string> myList = new LinkedList<string>();

        // Add elements to the linked list
        myList.AddLast("Apple");
        myList.AddLast("Banana");
        myList.AddLast("Orange");

        // Print all elements in the linked list
        Console.WriteLine("Elements in the linked list:");
        foreach (string item in myList)
        {
            Console.WriteLine(item);
        }

        // Insert an element after "Banana"
        LinkedListNode<string> node = myList.Find("Banana");
        myList.AddAfter(node, "Mango");

        // Print all elements in the linked list after insertion
        Console.WriteLine("\nElements in the linked list after insertion:");
        foreach (string item in myList)
        {
            Console.WriteLine(item);
        }

        // Remove "Banana" from the linked list
        myList.Remove("Banana");

        // Print all elements in the linked list after removal
        Console.WriteLine("\nElements in the linked list after removal:");
        foreach (string item in myList)
        {
            Console.WriteLine(item);
        }
    }
}
```

Output:
```
Elements in the linked list:
Apple
Banana
Orange

Elements in the linked list after insertion:
Apple
Banana
Mango
Orange

Elements in the linked list after removal:
Apple
Mango
Orange
```

In this example:
- We create a new instance of LinkedList called `myList`.
- We add elements ("Apple", "Banana", "Orange") to the linked list using the `AddLast` method.
- We print all elements in the linked list using a foreach loop.
- We insert an element ("Mango") after the node containing "Banana" using the `AddAfter` method.
- We print all elements in the linked list after the insertion.
- We remove "Banana" from the linked list using the `Remove` method.
- We print all elements in the linked list after the removal.

Linked List provides efficient operations for adding, removing, and accessing elements at any position within the list. It is commonly used in scenarios where dynamic resizing and efficient insertion or deletion of elements are required, such as implementing stacks, queues, and certain algorithms like graph traversal.

## **SortedDictionary Vs SortedList:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Here's a comparison between SortedDictionary and SortedList in tabular form:

| Feature               | SortedDictionary                                                | SortedList                                                        |
|-----------------------|------------------------------------------------------------------|-------------------------------------------------------------------|
| Data Structure        | Uses a tree-based data structure (Red-Black Tree) for storage.   | Uses an array-based data structure for storage.                   |
| Ordering             | Maintains elements in sorted order based on keys.                | Maintains elements in sorted order based on keys.                 |
| Lookup Complexity     | O(log n) for lookup operations (ContainsKey, Item[...]).         | O(log n) for lookup operations (ContainsKey, Item[...]).          |
| Insertion/Deletion    | Slightly slower compared to SortedList due to tree restructuring.| Slightly faster compared to SortedDictionary for small collections.|
| Memory Overhead       | Higher memory overhead due to tree structure.                    | Lower memory overhead compared to SortedDictionary.               |
| Implementation        | Implemented as a balanced binary search tree.                    | Implemented as an array with binary search algorithm for retrieval.|
| Suitable For         | Suitable for scenarios where frequent insertions and deletions are needed, and memory usage is not a concern. | Suitable for scenarios where frequent lookups are needed and memory efficiency is important. |
| Example               | ```SortedDictionary<int, string> dict = new SortedDictionary<int, string>();``` | ```SortedList<int, string> list = new SortedList<int, string>();``` |
| Use Case              | Dictionary with frequent insertions and deletions.                | Dictionary with frequent lookups and memory efficiency is important.|

Both SortedDictionary and SortedList provide sorted collection semantics, but they use different underlying data structures, resulting in differences in performance characteristics and memory usage. The choice between the two depends on the specific requirements of your application, such as the frequency of insertions, deletions, lookups, and memory constraints.

## **List Vs IEnumerable:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Let's compare `List` and `IEnumerable` in C# in a detailed tabular form:

| **Feature**                  | **List<T>**                                                    | **IEnumerable<T>**                                         |
|------------------------------|----------------------------------------------------------------|------------------------------------------------------------|
| **Namespace**                | `System.Collections.Generic`                                  | `System.Collections.Generic`                               |
| **Type**                     | Concrete class                                                | Interface                                                  |
| **Instantiation**            | Can be directly instantiated using `new List<T>()`            | Cannot be directly instantiated; requires implementation   |
| **Usage**                    | Use when you need dynamic array-like data structures with random access and modification capabilities | Use when you need a simple iteration over a collection      |
| **Random Access**            | Provides O(1) access via index                                | Does not provide direct access by index                    |
| **Modification**             | Supports adding, removing, and modifying elements             | Read-only; does not support modification                    |
| **Memory Consumption**       | Higher memory consumption due to storage overhead             | Lower memory consumption                                   |
| **Performance**              | Faster for accessing elements by index and modifying          | Better for streaming data and forward-only iteration       |
| **Linq Support**             | Fully supported with extension methods                        | Fully supported with extension methods                     |
| **Methods and Properties**   | Rich set of methods and properties (e.g., `Add`, `Remove`, `Count`) | Limited to `GetEnumerator`                                 |
| **Deferred Execution**       | Does not support deferred execution; evaluates immediately    | Supports deferred execution                                |
| **Use Cases**                | Use when collection needs to be modified frequently or accessed randomly | Use when only iteration or read-only operations are needed |

### Examples

#### Example using `List<T>`

```csharp
using System;
using System.Collections.Generic;

public class ListExample
{
    public static void Main()
    {
        List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

        // Add an element
        numbers.Add(6);

        // Remove an element
        numbers.Remove(3);

        // Access elements by index
        Console.WriteLine($"First element: {numbers[0]}");

        // Iterate over the list
        foreach (var number in numbers)
        {
            Console.WriteLine(number);
        }
    }
}
```

**Output:**
```
First element: 1
1
2
4
5
6
```

#### Example using `IEnumerable<T>`

```csharp
using System;
using System.Collections.Generic;
using System.Linq;

public class IEnumerableExample
{
    public static void Main()
    {
        IEnumerable<int> numbers = GetNumbers();

        // Iterate over the collection
        foreach (var number in numbers)
        {
            Console.WriteLine(number);
        }

        // Use Linq methods
        var evenNumbers = numbers.Where(n => n % 2 == 0);

        foreach (var number in evenNumbers)
        {
            Console.WriteLine($"Even number: {number}");
        }
    }

    public static IEnumerable<int> GetNumbers()
    {
        yield return 1;
        yield return 2;
        yield return 3;
        yield return 4;
        yield return 5;
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
Even number: 2
Even number: 4
```

### Detailed Explanation

1. **Namespace**: Both `List<T>` and `IEnumerable<T>` are part of the `System.Collections.Generic` namespace, making them part of the generic collection framework in .NET.

2. **Type**: `List<T>` is a concrete class that provides a dynamic array functionality, whereas `IEnumerable<T>` is an interface that defines a sequence of values that can be iterated over.

3. **Instantiation**: You can create an instance of a `List<T>` using `new List<T>()`. However, `IEnumerable<T>` cannot be instantiated directly since it is an interface; instead, it must be implemented by a class or provided by a method.

4. **Usage**: Use `List<T>` when you need to frequently access elements by index or modify the collection. Use `IEnumerable<T>` when you need to iterate over a collection without modifying it.

5. **Random Access**: `List<T>` allows you to access elements by their index, providing O(1) time complexity. `IEnumerable<T>` does not support random access; you must iterate through the collection.

6. **Modification**: `List<T>` provides methods for adding, removing, and modifying elements in the collection. `IEnumerable<T>` is read-only and does not support modification methods.

7. **Memory Consumption**: `List<T>` has higher memory consumption due to its internal array and resizing overhead. `IEnumerable<T>` typically has lower memory consumption since it is more lightweight.

8. **Performance**: `List<T>` is faster for operations that require accessing elements by index or modifying the collection. `IEnumerable<T>` is more suitable for streaming data and forward-only iteration scenarios.

9. **Linq Support**: Both `List<T>` and `IEnumerable<T>` support Linq extension methods, enabling powerful querying capabilities.

10. **Methods and Properties**: `List<T>` has a rich set of methods and properties, such as `Add`, `Remove`, `Insert`, `Count`, etc. `IEnumerable<T>` primarily has the `GetEnumerator` method to support iteration.

11. **Deferred Execution**: Linq queries on `IEnumerable<T>` support deferred execution, meaning the query is not executed until the results are enumerated. `List<T>` evaluates immediately when the methods are called.

12. **Use Cases**: Use `List<T>` when you need a mutable, dynamic collection with fast access and modification capabilities. Use `IEnumerable<T>` for read-only operations and scenarios where you are only interested in iterating over a sequence of values.

This comparison should help you understand when to use `List<T>` and `IEnumerable<T>` in your C# applications and their respective benefits and limitations.