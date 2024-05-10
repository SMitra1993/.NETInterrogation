# Namespace ❤🍕

**Links:**

- [Stack Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [Queue Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [HashTable Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [SortedList Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [HashSet Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [LinkedList Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [List Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [SortedSet Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [Dictionary Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [SortedDictionary Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)
- [BitArray Class](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#list-)

## **Stack Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **Stack()**: Initializes a new instance of the Stack class that is empty and has the default initial capacity.
   - Example:
     ```csharp
     Stack<int> stack = new Stack<int>();
     ```

2. **Stack(IEnumerable<T> collection)**: Initializes a new instance of the Stack class that contains elements copied from the specified collection and has the same initial capacity as the number of elements copied.
   - Example:
     ```csharp
     List<int> list = new List<int> { 1, 2, 3, 4, 5 };
     Stack<int> stack = new Stack<int>(list);
     ```

3. **Stack(Int32)**: Initializes a new instance of the Stack class that is empty and has the specified initial capacity.
   - Example:
     ```csharp
     Stack<int> stack = new Stack<int>(10);
     ```

### Methods:
1. **Push(T item)**: Inserts an element at the top of the stack.
   - Example:
     ```csharp
     stack.Push(10);
     ```

2. **Pop()**: Removes and returns the object at the top of the Stack.
   - Example:
     ```csharp
     int topItem = stack.Pop();
     ```

3. **Peek()**: Returns the object at the top of the Stack without removing it.
   - Example:
     ```csharp
     int topItem = stack.Peek();
     ```

4. **Clear()**: Removes all objects from the Stack.
   - Example:
     ```csharp
     stack.Clear();
     ```

5. **Contains(T item)**: Determines whether an element is in the Stack.
   - Example:
     ```csharp
     bool exists = stack.Contains(10);
     ```

6. **CopyTo(T[] array, int arrayIndex)**: Copies the Stack to an existing one-dimensional Array, starting at the specified array index.
   - Example:
     ```csharp
     int[] array = new int[stack.Count];
     stack.CopyTo(array, 0);
     ```

7. **GetEnumerator()**: Returns an enumerator for the Stack.
   - Example:
     ```csharp
     foreach (int item in stack)
     {
         Console.WriteLine(item);
     }
     ```

### Properties:
1. **Count**: Gets the number of elements contained in the Stack.
   - Example:
     ```csharp
     int count = stack.Count;
     ```

2. **IsSynchronized**: Gets a value indicating whether access to the Stack is synchronized (thread-safe).
   - Example:
     ```csharp
     bool isSynchronized = stack.IsSynchronized;
     ```

3. **SyncRoot**: Gets an object that can be used to synchronize access to the Stack.
   - Example:
     ```csharp
     object syncRoot = stack.SyncRoot;
     ```

These constructors, methods, and properties provide various functionalities to manipulate and access elements in a Stack collection.


## **Queue Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **Queue()**: Initializes a new instance of the Queue class that is empty and has the default initial capacity.
   - Example:
     ```csharp
     Queue<int> queue = new Queue<int>();
     ```

2. **Queue(IEnumerable<T> collection)**: Initializes a new instance of the Queue class that contains elements copied from the specified collection and has the same initial capacity as the number of elements copied.
   - Example:
     ```csharp
     List<int> list = new List<int> { 1, 2, 3, 4, 5 };
     Queue<int> queue = new Queue<int>(list);
     ```

3. **Queue(Int32)**: Initializes a new instance of the Queue class that is empty and has the specified initial capacity.
   - Example:
     ```csharp
     Queue<int> queue = new Queue<int>(10);
     ```

### Methods:
1. **Enqueue(T item)**: Adds an object to the end of the Queue.
   - Example:
     ```csharp
     queue.Enqueue(10);
     ```

2. **Dequeue()**: Removes and returns the object at the beginning of the Queue.
   - Example:
     ```csharp
     int frontItem = queue.Dequeue();
     ```

3. **Peek()**: Returns the object at the beginning of the Queue without removing it.
   - Example:
     ```csharp
     int frontItem = queue.Peek();
     ```

4. **Clear()**: Removes all objects from the Queue.
   - Example:
     ```csharp
     queue.Clear();
     ```

5. **Contains(T item)**: Determines whether an element is in the Queue.
   - Example:
     ```csharp
     bool exists = queue.Contains(10);
     ```

6. **ToArray()**: Copies the Queue elements to a new array.
   - Example:
     ```csharp
     T[] array = queue.ToArray();
     ```

7. **CopyTo(T[] array, int arrayIndex)**: Copies the Queue elements to an existing one-dimensional Array, starting at the specified array index.
   - Example:
     ```csharp
     T[] array = new T[queue.Count];
     queue.CopyTo(array, 0);
     ```

### Properties:
1. **Count**: Gets the number of elements contained in the Queue.
   - Example:
     ```csharp
     int count = queue.Count;
     ```

2. **IsSynchronized**: Gets a value indicating whether access to the Queue is synchronized (thread-safe).
   - Example:
     ```csharp
     bool isSynchronized = queue.IsSynchronized;
     ```

3. **SyncRoot**: Gets an object that can be used to synchronize access to the Queue.
   - Example:
     ```csharp
     object syncRoot = queue.SyncRoot;
     ```

These constructors, methods, and properties provide various functionalities to manipulate and access elements in a Queue collection.

## **HashTable Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **Hashtable()**: Initializes a new instance of the Hashtable class that is empty, has the default initial capacity, and uses the default load factor.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable();
     ```

2. **Hashtable(Int32)**: Initializes a new instance of the Hashtable class with the specified initial capacity and uses the default load factor.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100);
     ```
3. **Hashtable(IDictionary)**: Initializes a new instance of the Hashtable class containing elements copied from the specified dictionary.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(dictionary);
     ```
4. **Hashtable(SerializationInfo, StreamingContext)**: Initializes a new instance of the Hashtable class with serialized data.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(serializationInfo, streamingContext);
     ```

5. **Hashtable(Int32, Single, IHashCodeProvider, IComparer)**: Initializes a new instance of the Hashtable class with the specified initial capacity, load factor, hash code provider, and comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100, 0.75f, hashCodeProvider, comparer);
     ```

6. **Hashtable(Int32, Single, IEqualityComparer)**: Initializes a new instance of the Hashtable class with the specified initial capacity, load factor, and equality comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100, 0.75f, equalityComparer);
     ```

7. **Hashtable(Int32, Single)**: Initializes a new instance of the Hashtable class with the specified initial capacity and load factor.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100, 0.75f);
     ```

8. **Hashtable(Int32, IHashCodeProvider, IComparer)**: Initializes a new instance of the Hashtable class with the specified initial capacity, hash code provider, and comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100, hashCodeProvider, comparer);
     ```

9. **Hashtable(Int32, IEqualityComparer)**: Initializes a new instance of the Hashtable class with the specified initial capacity and equality comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(100, equalityComparer);
     ```

10. **Hashtable(IHashCodeProvider, IComparer)**: Initializes a new instance of the Hashtable class with the specified hash code provider and comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(hashCodeProvider, comparer);
     ```

11. **Hashtable(IEqualityComparer)**: Initializes a new instance of the Hashtable class with the specified equality comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(equalityComparer);
     ```

12. **Hashtable(IDictionary, Single, IHashCodeProvider, IComparer)**: Initializes a new instance of the Hashtable class with the specified dictionary, load factor, hash code provider, and comparer.
   - Example:
     ```csharp
     Hashtable hashtable = new Hashtable(dictionary, 0.75f, hashCodeProvider, comparer);
     ```

13. **Hashtable(IDictionary, Single, IEqualityComparer)**: Initializes a new instance of the Hashtable class with the specified dictionary, load factor, and equality comparer.
    - Example:
      ```csharp
      Hashtable hashtable = new Hashtable(dictionary, 0.75f, equalityComparer);
      ```

### Methods:
1. **Add(Object, Object)**: Adds an element with the specified key and value into the Hashtable.
   - Example:
     ```csharp
     hashtable.Add("key", "value");
     ```

2. **Remove(Object)**: Removes the element with the specified key from the Hashtable.
   - Example:
     ```csharp
     hashtable.Remove("key");
     ```

3. **Contains(Object)**: Determines whether the Hashtable contains a specific key.
   - Example:
     ```csharp
     bool containsKey = hashtable.Contains("key");
     ```

4. **Clear()**: Removes all elements from the Hashtable.
   - Example:
     ```csharp
     hashtable.Clear();
     ```

5. **Clone()**: Creates a shallow copy of the Hashtable.
   - Example:
     ```csharp
     Hashtable copy = (Hashtable)hashtable.Clone();
     ```

6. **Keys**: Gets a collection containing the keys in the Hashtable.
   - Example:
     ```csharp
     ICollection keys = hashtable.Keys;
     ```

7. **Values**: Gets a collection containing the values in the Hashtable.
   - Example:
     ```csharp
     ICollection values = hashtable.Values;
     ```

### Properties:
1. **Count**: Gets the number of key/value pairs contained in the Hashtable.
   - Example:
     ```csharp
     int count = hashtable.Count;
     ```

2. **IsFixedSize**: Gets a value indicating whether the Hashtable has a fixed size.
   - Example:
     ```csharp
     bool isFixedSize = hashtable.IsFixedSize;
     ```

3. **IsReadOnly**: Gets a value indicating whether the Hashtable is read-only.
   - Example:
     ```csharp
     bool isReadOnly = hashtable.IsReadOnly;
     ```

4. **Item[Object]**: Gets or sets the value associated with the specified key.
   - Example:
     ```csharp
     object value = hashtable["key"];
     ```
These constructors, methods, and properties provide various functionalities to manipulate and access elements in a Hashtable collection.

## **SortedList Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Certainly! Here's a breakdown of SortedList constructors, methods, and properties with examples:

### Constructors:
1. **SortedList()**: Initializes a new instance of the SortedList class that is empty, has the default initial capacity, and is sorted according to the natural order of its elements.
   ```csharp
   SortedList sortedList = new SortedList();
   ```

2. **SortedList(IComparer)**: Initializes a new instance of the SortedList class that is empty, has the default initial capacity, and is sorted according to the specified comparer.
   ```csharp
   SortedList sortedList = new SortedList(new CustomComparer());
   ```

3. **SortedList(Int32)**: Initializes a new instance of the SortedList class that is empty, has the specified initial capacity, and is sorted according to the natural order of its elements.
   ```csharp
   SortedList sortedList = new SortedList(100);
   ```

4. **SortedList(IDictionary)**: Initializes a new instance of the SortedList class that contains elements copied from the specified dictionary, sorted according to the keys.
   ```csharp
   var dictionary = new Dictionary<int, string>
   {
       { 3, "Three" },
       { 1, "One" },
       { 2, "Two" }
   };
   SortedList sortedList = new SortedList(dictionary);
   ```

### Properties:
1. **Count**: Gets the number of key/value pairs contained in the SortedList.
   ```csharp
   int count = sortedList.Count;
   ```

2. **IsFixedSize**: Gets a value indicating whether the SortedList has a fixed size.
   ```csharp
   bool isFixedSize = sortedList.IsFixedSize;
   ```

### Methods:
1. **Add(Object, Object)**: Adds an element with the specified key and value into the SortedList.
   ```csharp
   sortedList.Add(4, "Four");
   ```

2. **Clear()**: Removes all elements from the SortedList.
   ```csharp
   sortedList.Clear();
   ```

3. **Contains(Object)**: Determines whether the SortedList contains a specific key.
   ```csharp
   bool containsKey = sortedList.Contains(1);
   ```

4. **ContainsKey(Object)**: Determines whether the SortedList contains a specific key.
   ```csharp
   bool containsKey = sortedList.ContainsKey(2);
   ```

5. **ContainsValue(Object)**: Determines whether the SortedList contains a specific value.
   ```csharp
   bool containsValue = sortedList.ContainsValue("Three");
   ```

6. **GetByIndex(Int32)**: Gets the value at the specified index of the SortedList.
   ```csharp
   var value = sortedList.GetByIndex(0);
   ```

7. **Remove(Object)**: Removes the element with the specified key from the SortedList.
   ```csharp
   sortedList.Remove(2);
   ```

These constructors, properties, and methods provide various functionalities to work with SortedList instances in C#.

## **HashSet Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **HashSet()**: Initializes a new instance of the HashSet class that is empty and uses the default equality comparer for the set type.
   ```csharp
   HashSet<int> hashSet = new HashSet<int>();
   ```

2. **HashSet(IEnumerable<T>)**: Initializes a new instance of the HashSet class that contains elements copied from the specified collection and uses the default equality comparer for the set type.
   ```csharp
   var collection = new List<int> { 1, 2, 3 };
   HashSet<int> hashSet = new HashSet<int>(collection);
   ```

3. **HashSet(IEqualityComparer<T>)**: Initializes a new instance of the HashSet class that is empty and uses the specified equality comparer for the set type.
   ```csharp
   IEqualityComparer<int> comparer = EqualityComparer<int>.Default;
   HashSet<int> hashSet = new HashSet<int>(comparer);
   ```

### Properties:
1. **Count**: Gets the number of elements contained in the HashSet.
   ```csharp
   int count = hashSet.Count;
   ```

2. **IsReadOnly**: Gets a value indicating whether the HashSet is read-only.
   ```csharp
   bool isReadOnly = hashSet.IsReadOnly;
   ```

### Methods:
1. **Add(T)**: Adds the specified element to the HashSet.
   ```csharp
   hashSet.Add(4);
   ```

2. **Clear()**: Removes all elements from the HashSet.
   ```csharp
   hashSet.Clear();
   ```

3. **Contains(T)**: Determines whether the HashSet contains a specific value.
   ```csharp
   bool contains = hashSet.Contains(3);
   ```

4. **ExceptWith(IEnumerable<T>)**: Removes all elements in the specified collection from the HashSet.
   ```csharp
   var otherCollection = new List<int> { 2, 3 };
   hashSet.ExceptWith(otherCollection);
   ```

5. **IntersectWith(IEnumerable<T>)**: Modifies the current HashSet so that it contains only elements that are also in a specified collection.
   ```csharp
   var otherCollection = new List<int> { 3, 4 };
   hashSet.IntersectWith(otherCollection);
   ```

6. **UnionWith(IEnumerable<T>)**: Modifies the current HashSet so that it contains all elements that are present in the current HashSet, in the specified collection, or in both.
   ```csharp
   var otherCollection = new List<int> { 3, 4 };
   hashSet.UnionWith(otherCollection);
   ```

7. **Remove(T)**: Removes the specified element from the HashSet.
   ```csharp
   hashSet.Remove(2);
   ```

8. **Clear()**: Removes all elements from the HashSet.
   ```csharp
   hashSet.Clear();
   ```

These constructors, properties, and methods provide various functionalities to work with HashSet instances in C#.

## **LinkedList Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **LinkedList()**: Initializes a new instance of the LinkedList class that is empty.
   ```csharp
   LinkedList<int> linkedList = new LinkedList<int>();
   ```

2. **LinkedList(IEnumerable<T>)**: Initializes a new instance of the LinkedList class that contains elements copied from the specified collection.
   ```csharp
   var collection = new List<int> { 1, 2, 3 };
   LinkedList<int> linkedList = new LinkedList<int>(collection);
   ```

### Properties:
1. **Count**: Gets the number of nodes actually contained in the LinkedList.
   ```csharp
   int count = linkedList.Count;
   ```

2. **First**: Gets the first node of the LinkedList.
   ```csharp
   var firstNode = linkedList.First;
   ```

3. **Last**: Gets the last node of the LinkedList.
   ```csharp
   var lastNode = linkedList.Last;
   ```

### Methods:
1. **AddFirst(T)**: Adds a new node containing the specified value at the start of the LinkedList.
   ```csharp
   linkedList.AddFirst(0);
   ```

2. **AddLast(T)**: Adds a new node containing the specified value at the end of the LinkedList.
   ```csharp
   linkedList.AddLast(4);
   ```

3. **AddAfter(LinkedListNode<T>, T)**: Inserts a new node containing the specified value after the specified existing node in the LinkedList.
   ```csharp
   var node = linkedList.First.Next;
   linkedList.AddAfter(node, 2.5);
   ```

4. **AddBefore(LinkedListNode<T>, T)**: Inserts a new node containing the specified value before the specified existing node in the LinkedList.
   ```csharp
   var node = linkedList.Last.Previous;
   linkedList.AddBefore(node, 3.5);
   ```

5. **Remove(T)**: Removes the first occurrence of the specified value from the LinkedList.
   ```csharp
   linkedList.Remove(2);
   ```

6. **RemoveFirst()**: Removes the node at the start of the LinkedList.
   ```csharp
   linkedList.RemoveFirst();
   ```

7. **RemoveLast()**: Removes the node at the end of the LinkedList.
   ```csharp
   linkedList.RemoveLast();
   ```

These constructors, properties, and methods provide various functionalities to work with LinkedList instances in C#.

## **List Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **List()**: Initializes a new instance of the List class that is empty and has the default initial capacity.
   ```csharp
   List<int> myList = new List<int>();
   ```

2. **List(IEnumerable<T>)**: Initializes a new instance of the List class that contains elements copied from the specified collection and has sufficient capacity to accommodate the number of elements copied.
   ```csharp
   var collection = new List<int> { 1, 2, 3 };
   List<int> myList = new List<int>(collection);
   ```

3. **List(Int32)**: Initializes a new instance of the List class that is empty and has the specified initial capacity.
   ```csharp
   List<int> myList = new List<int>(10);
   ```

### Properties:
1. **Capacity**: Gets or sets the total number of elements the internal data structure can hold without resizing.
   ```csharp
   int capacity = myList.Capacity;
   ```

2. **Count**: Gets the number of elements actually contained in the List.
   ```csharp
   int count = myList.Count;
   ```

### Methods:
1. **Add(T)**: Adds an object to the end of the List.
   ```csharp
   myList.Add(4);
   ```

2. **Insert(Int32, T)**: Inserts an element into the List at the specified index.
   ```csharp
   myList.Insert(2, 10);
   ```

3. **Remove(T)**: Removes the first occurrence of a specific object from the List.
   ```csharp
   myList.Remove(2);
   ```

4. **RemoveAt(Int32)**: Removes the element at the specified index of the List.
   ```csharp
   myList.RemoveAt(0);
   ```

5. **Contains(T)**: Determines whether an element is in the List.
   ```csharp
   bool contains = myList.Contains(3);
   ```

6. **Clear()**: Removes all elements from the List.
   ```csharp
   myList.Clear();
   ```

7. **Sort()**: Sorts the elements in the entire List.
   ```csharp
   myList.Sort();
   ```

8. **ToArray()**: Copies the elements of the List to a new array.
   ```csharp
   int[] newArray = myList.ToArray();
   ```

9. **IndexOf(T)**: Searches for the specified object and returns the zero-based index of the first occurrence within the entire List.
   ```csharp
   int index = myList.IndexOf(3);
   ```

These constructors, properties, and methods provide various functionalities to work with List instances in C#.

## **SortedSet Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **SortedSet()**: Initializes a new instance of the SortedSet class that is empty and uses the default comparer for the element type.
   ```csharp
   SortedSet<int> sortedSet = new SortedSet<int>();
   ```

2. **SortedSet(IEnumerable<T>)**: Initializes a new instance of the SortedSet class that contains elements copied from the specified collection and uses the default comparer for the element type.
   ```csharp
   var collection = new List<int> { 3, 2, 1 };
   SortedSet<int> sortedSet = new SortedSet<int>(collection);
   ```

3. **SortedSet(IComparer<T>)**: Initializes a new instance of the SortedSet class that is empty and uses the specified comparer for the element type.
   ```csharp
   SortedSet<int> sortedSet = new SortedSet<int>(Comparer<int>.Create((x, y) => y.CompareTo(x)));
   ```

### Properties (continued):
1. **Comparer**: Gets the IComparer<T> object that is used to order the elements in the SortedSet.
   ```csharp
   var comparer = sortedSet.Comparer;
   ```

2. **IsReadOnly**: Gets a value indicating whether the SortedSet is read-only.
   ```csharp
   bool isReadOnly = sortedSet.IsReadOnly;
   ```

3. **Max**: Gets the maximum value in the SortedSet according to the comparer.
   ```csharp
   var max = sortedSet.Max;
   ```

4. **Min**: Gets the minimum value in the SortedSet according to the comparer.
   ```csharp
   var min = sortedSet.Min;
   ```

5. **Count**: Gets the number of elements contained in the SortedSet.
   ```csharp
   int count = sortedSet.Count;
   ```

### Methods:
1. **Add(T)**: Adds the specified element to the SortedSet.
   ```csharp
   sortedSet.Add(4);
   ```

2. **Remove(T)**: Removes the specified element from the SortedSet.
   ```csharp
   sortedSet.Remove(2);
   ```

3. **Contains(T)**: Determines whether the SortedSet contains a specific value.
   ```csharp
   bool contains = sortedSet.Contains(3);
   ```

4. **Clear()**: Removes all elements from the SortedSet.
   ```csharp
   sortedSet.Clear();
   ```

5. **UnionWith(IEnumerable<T>)**: Modifies the current SortedSet so that it contains all elements that are present in itself, the specified collection, or both.
   ```csharp
   var otherCollection = new List<int> { 5, 6, 7 };
   sortedSet.UnionWith(otherCollection);
   ```

6. **IntersectWith(IEnumerable<T>)**: Modifies the current SortedSet so that it contains only elements that are also in a specified collection.
   ```csharp
   sortedSet.IntersectWith(otherCollection);
   ```

7. **ExceptWith(IEnumerable<T>)**: Removes all elements in the specified collection from the current SortedSet.
   ```csharp
   sortedSet.ExceptWith(otherCollection);
   ```

8. **SymmetricExceptWith(IEnumerable<T>)**: Modifies the current SortedSet so that it contains only elements that are present either in the current SortedSet or in the specified collection, but not both.
   ```csharp
   sortedSet.SymmetricExceptWith(otherCollection);
   ```

These constructors, properties, and methods provide functionalities for working with SortedSet instances in C#.

## **Dictionary Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **Dictionary()**: Initializes a new instance of the Dictionary<TKey, TValue> class that is empty.
   ```csharp
   Dictionary<string, int> dictionary = new Dictionary<string, int>();
   ```

2. **Dictionary(IDictionary<TKey, TValue>)**: Initializes a new instance of the Dictionary<TKey, TValue> class that contains elements copied from the specified IDictionary<TKey, TValue>.
   ```csharp
   var sourceDictionary = new Dictionary<string, int> { { "one", 1 }, { "two", 2 } };
   Dictionary<string, int> dictionary = new Dictionary<string, int>(sourceDictionary);
   ```

3. **Dictionary(IEqualityComparer<TKey>)**: Initializes a new instance of the Dictionary<TKey, TValue> class that is empty and uses the specified equality comparer for the key type.
   ```csharp
   var comparer = StringComparer.OrdinalIgnoreCase;
   Dictionary<string, int> dictionary = new Dictionary<string, int>(comparer);
   ```

### Properties:
1. **Count**: Gets the number of key/value pairs contained in the Dictionary<TKey, TValue>.
   ```csharp
   int count = dictionary.Count;
   ```

2. **Comparer**: Gets the IEqualityComparer<TKey> implementation to use when comparing keys.
   ```csharp
   var comparer = dictionary.Comparer;
   ```

3. **Item[TKey]**: Gets or sets the value associated with the specified key.
   ```csharp
   dictionary["three"] = 3;
   int value = dictionary["three"];
   ```

4. **Keys**: Gets a collection containing the keys in the dictionary.
   ```csharp
   ICollection<TKey> keys = dictionary.Keys;
   ```

5. **Values**: Gets a collection containing the values in the dictionary.
   ```csharp
   ICollection<TValue> values = dictionary.Values;
   ```

6. **IsReadOnly**: Gets a value indicating whether the Dictionary<TKey, TValue> is read-only.
   ```csharp
   bool isReadOnly = dictionary.IsReadOnly;
   ```

7. **Item[object]**: Gets or sets the value associated with the specified key.
   ```csharp
   object value = dictionary["three"];
   ```

### Methods:
1. **Add(TKey, TValue)**: Adds the specified key and value to the dictionary.
   ```csharp
   dictionary.Add("three", 3);
   ```

2. **Remove(TKey)**: Removes the value with the specified key from the dictionary.
   ```csharp
   dictionary.Remove("two");
   ```

3. **ContainsKey(TKey)**: Determines whether the dictionary contains the specified key.
   ```csharp
   bool containsKey = dictionary.ContainsKey("one");
   ```

4. **ContainsValue(TValue)**: Determines whether the dictionary contains a specific value.
   ```csharp
   bool containsValue = dictionary.ContainsValue(3);
   ```

5. **TryGetValue(TKey, out TValue)**: Gets the value associated with the specified key.
   ```csharp
   if (dictionary.TryGetValue("one", out int value))
   {
       Console.WriteLine($"The value of 'one' is {value}");
   }
   ```

6. **Clear()**: Removes all keys and values from the dictionary.
   ```csharp
   dictionary.Clear();
   ```

7. **Keys**: Gets a collection containing the keys in the dictionary.
   ```csharp
   var keys = dictionary.Keys;
   ```

8. **Values**: Gets a collection containing the values in the dictionary.
   ```csharp
   var values = dictionary.Values;
   ```

These constructors, properties, and methods provide functionalities for working with Dictionary instances in C#.

## **SortedDictionary Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

### Constructors:
1. **SortedDictionary()**: Initializes a new instance of the SortedDictionary<TKey, TValue> class that is empty and uses the default comparer for the key type.
   ```csharp
   SortedDictionary<string, int> sortedDictionary = new SortedDictionary<string, int>();
   ```

2. **SortedDictionary(IDictionary<TKey, TValue>)**: Initializes a new instance of the SortedDictionary<TKey, TValue> class that contains elements copied from the specified IDictionary<TKey, TValue> and uses the default comparer for the key type.
   ```csharp
   var sourceDictionary = new Dictionary<string, int> { { "one", 1 }, { "two", 2 } };
   SortedDictionary<string, int> sortedDictionary = new SortedDictionary<string, int>(sourceDictionary);
   ```

3. **SortedDictionary(IComparer<TKey>)**: Initializes a new instance of the SortedDictionary<TKey, TValue> class that is empty and uses the specified comparer for the key type.
   ```csharp
   var comparer = StringComparer.OrdinalIgnoreCase;
   SortedDictionary<string, int> sortedDictionary = new SortedDictionary<string, int>(comparer);
   ```

### Properties (continued):
1. **Comparer**: Gets the IComparer<TKey> implementation used to sort keys.
   ```csharp
   var comparer = sortedDictionary.Comparer;
   ```

2. **Item[TKey]**: Gets or sets the value associated with the specified key.
   ```csharp
   sortedDictionary["three"] = 3;
   int value = sortedDictionary["three"];
   ```

3. **Count**: Gets the number of key/value pairs contained in the SortedDictionary<TKey, TValue>.
   ```csharp
   int count = sortedDictionary.Count;
   ```

4. **Keys**: Gets a collection containing the keys in the dictionary.
   ```csharp
   ICollection<TKey> keys = sortedDictionary.Keys;
   ```

5. **Values**: Gets a collection containing the values in the dictionary.
   ```csharp
   ICollection<TValue> values = sortedDictionary.Values;
   ```

6. **IsReadOnly**: Gets a value indicating whether the SortedDictionary<TKey, TValue> is read-only.
   ```csharp
   bool isReadOnly = sortedDictionary.IsReadOnly;
   ```

7. **Item[int]**: Gets or sets the value associated with the specified index.
   ```csharp
   int value = sortedDictionary[0];
   ```

### Methods:
1. **Add(TKey, TValue)**: Adds the specified key and value to the dictionary.
   ```csharp
   sortedDictionary.Add("three", 3);
   ```

2. **Remove(TKey)**: Removes the value with the specified key from the dictionary.
   ```csharp
   sortedDictionary.Remove("two");
   ```

3. **ContainsKey(TKey)**: Determines whether the dictionary contains the specified key.
   ```csharp
   bool containsKey = sortedDictionary.ContainsKey("one");
   ```

4. **TryGetValue(TKey, out TValue)**: Gets the value associated with the specified key.
   ```csharp
   if (sortedDictionary.TryGetValue("one", out int value))
   {
       Console.WriteLine($"The value of 'one' is {value}");
   }
   ```

5. **Clear()**: Removes all keys and values from the dictionary.
   ```csharp
   sortedDictionary.Clear();
   ```

6. **Keys**: Gets a collection containing the keys in the dictionary.
   ```csharp
   var keys = sortedDictionary.Keys;
   ```

7. **Values**: Gets a collection containing the values in the dictionary.
   ```csharp
   var values = sortedDictionary.Values;
   ```

These constructors, properties, and methods provide functionalities for working with SortedDictionary instances in C#.

## **BitArray Class:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/11%20-%20Collections%26Generics.md#collections--generics-)

Certainly! Here's an explanation of the constructors, methods, and properties of the BitArray class in C#:

### Constructors:
1. **BitArray(Int32)**: Initializes a new instance of the BitArray class that can hold the specified number of bits, all set to false.
   ```csharp
   BitArray bitArray = new BitArray(8); // Creates a BitArray with 8 bits, all set to false.
   ```

2. **BitArray(Boolean[])**: Initializes a new instance of the BitArray class that contains values copied from the specified array of Booleans.
   ```csharp
   bool[] boolArray = { true, false, true, true };
   BitArray bitArray = new BitArray(boolArray); // Creates a BitArray with values from boolArray.
   ```

3. **BitArray(Byte[])**: Initializes a new instance of the BitArray class that contains values copied from the specified array of bytes.
   ```csharp
   byte[] byteArray = { 0x05, 0x0A }; // Binary: 0000 0101, 0000 1010
   BitArray bitArray = new BitArray(byteArray); // Creates a BitArray with values from byteArray.
   ```

### Methods:
1. **And(BitArray)**: Performs a bitwise AND operation on the elements of the current BitArray and another specified BitArray.
   ```csharp
   BitArray otherBitArray = new BitArray(new bool[] { true, false, false, true });
   bitArray.And(otherBitArray); // Performs a bitwise AND operation.
   ```

2. **Or(BitArray)**: Performs a bitwise OR operation on the elements of the current BitArray and another specified BitArray.
   ```csharp
   BitArray otherBitArray = new BitArray(new bool[] { true, false, false, true });
   bitArray.Or(otherBitArray); // Performs a bitwise OR operation.
   ```

3. **Xor(BitArray)**: Performs a bitwise XOR operation on the elements of the current BitArray and another specified BitArray.
   ```csharp
   BitArray otherBitArray = new BitArray(new bool[] { true, false, false, true });
   bitArray.Xor(otherBitArray); // Performs a bitwise XOR operation.
   ```

4. **Not()**: Negates all the bits in the current BitArray, so that elements set to true are changed to false, and elements set to false are changed to true.
   ```csharp
   bitArray.Not(); // Negates all bits in the BitArray.
   ```

5. **SetAll(Boolean)**: Sets all the bits in the BitArray to the specified value.
   ```csharp
   bitArray.SetAll(true); // Sets all bits in the BitArray to true.
   ```

6. **CopyTo(Array, Int32)**: Copies the entire BitArray to a compatible one-dimensional array, starting at the specified index of the target array.
   ```csharp
   bool[] targetArray = new bool[bitArray.Count];
   bitArray.CopyTo(targetArray, 0); // Copies the BitArray to targetArray.
   ```

7. **Get(Int32)**: Gets the value of the bit at the specified index.
   ```csharp
   bool bitValue = bitArray.Get(2); // Gets the value of the bit at index 2.
   ```

8. **Set(Int32, Boolean)**: Sets the bit at the specified index to the specified value.
   ```csharp
   bitArray.Set(2, true); // Sets the bit at index 2 to true.
   ```

9. **Clone()**: Creates a shallow copy of the BitArray.
   ```csharp
   BitArray cloneBitArray = bitArray.Clone() as BitArray; // Creates a shallow copy of the BitArray.
   ```

10. **Equals(Object)**: Determines whether the specified object is equal to the current BitArray.
   ```csharp
   BitArray otherBitArray = new BitArray(new bool[] { true, false, true });
   bool isEqual = bitArray.Equals(otherBitArray); // Checks if the two BitArrays are equal.
   ```

### Properties:
1. **Count**: Gets the number of elements contained in the BitArray.
   ```csharp
   int count = bitArray.Count; // Gets the number of elements.
   ```

2. **IsReadOnly**: Gets a value indicating whether the BitArray is read-only.
   ```csharp
   bool isReadOnly = bitArray.IsReadOnly; // Checks if BitArray is read-only.
   ```

3. **Item[Int32]**: Gets or sets the value of the bit at the specified index.
   ```csharp
   bool value = bitArray[3]; // Gets the value of the bit at index 3.
   bitArray[3] = false; // Sets the value of the bit at index 3 to false.
   ```

4. **Length**: Gets or sets the number of elements in the BitArray. This property is synonymous with the Count property.
   ```csharp
   int length = bitArray.Length; // Gets the number of elements in the BitArray.
   ```

5. **SyncRoot**: Gets an object that can be used to synchronize access to the BitArray.
   ```csharp
   object syncRoot = bitArray.SyncRoot; // Gets the synchronization root object.
   ```

6. **IsSynchronized**: Gets a value indicating whether access to the BitArray is synchronized (thread safe).
   ```csharp
   bool isSynchronized = bitArray.IsSynchronized; // Checks if access to the BitArray is synchronized.
   ```

These properties provide additional information and functionality for managing and accessing BitArray instances in C#.
These constructors, methods, and properties provide functionalities for working with BitArray instances in C#.