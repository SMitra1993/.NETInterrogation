# String ❤🍕

**Links:**

- [String](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#array--1)
- [`string` vs `System.String`](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#1-d-2-d-3-d-and-n-d-array-)
- [Verbatim String Literal – `@`](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#jagged-array-)
- [String Methods](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#array-class-)
- [String Properties](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#array-methods-)
- [String Constructors](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#array-properties-)
- [String Builder](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#dynamic-array-)
- [String Builder Methods](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#arraylist-)
- [String Vs String Builder](https://github.com/SMitra1993/theNETInterrogation/blob/master/9%20-%20Array.md#arraylist-methods-)

## **String:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, a string is a sequence of characters that represents text. It is a data type used to store textual data. Strings are immutable, meaning their values cannot be changed after they are created.

Here's an example of how strings are used in C#:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declaring a string variable
        string message = "Hello, World!";

        // Displaying the string
        Console.WriteLine(message);
    }
}
```

Output:
```
Hello, World!
```

In this example:
- We declare a string variable `message` and initialize it with the text `"Hello, World!"`.
- We then use `Console.WriteLine` to display the value of the `message` string to the console.

## **`string` vs `System.String`:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a detailed comparison between `string` and `System.String` in tabular form:

| Feature                         | `string`                                              | `System.String`                                   |
|---------------------------------|-------------------------------------------------------|--------------------------------------------------|
| Syntax                          | Uses C# keyword `string`.                             | Uses fully qualified name `System.String`.        |
| Mutability                      | Immutable; once created, cannot be changed.          | Immutable; once created, cannot be changed.      |
| Memory Allocation               | Compiled to `string` in IL code.                      | Represents the same `string` type but with a different name.|
| Compiler Optimization           | C# compiler treats `string` as an alias for `System.String`. | Treated as a distinct type by the compiler.      |
| Ease of Use                     | Simplified syntax for creating and using strings.     | Requires explicit use of fully qualified name.   |
| Preferred Usage                 | Preferred for general use and readability.            | Rarely used due to verbosity and redundancy.     |
| Interchangeability             | Interchangeable with `System.String`.                 | Interchangeable with `string`.                   |
| Clarity and Readability         | Offers clearer and more concise code.                 | May lead to confusion or verbosity in code.      |

In summary, while `string` and `System.String` are functionally equivalent in C#, the `string` keyword is preferred for its simplicity, readability, and familiarity. However, `System.String` can be used interchangeably with `string` when necessary, although it is less common due to its verbosity.

## **Verbatim String Literal – `@`** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

In C#, the "@" symbol serves a dual purpose: as a verbatim string literal prefix and as an identifier prefix to create valid identifiers with reserved keywords. Let's merge both explanations into a comprehensive one:

The "@" symbol in C# is a versatile character that serves different purposes depending on its usage context. 

1. **Verbatim String Literal Prefix**: When used before a string literal, the "@" symbol denotes a verbatim string literal. This allows the inclusion of escape characters or special characters without the need for escaping. Verbatim string literals are particularly useful for representing file paths, regular expressions, or any string that contains backslashes or escape sequences.

   ```csharp
   string regularPath = "C:\\Windows\\System32\\"; // Regular string literal
   string verbatimPath = @"C:\Windows\System32\";   // Verbatim string literal
   ```

   In this example, `verbatimPath` contains the same value as `regularPath`, but the verbatim string literal is more readable and requires fewer escape characters.

2. **Identifier Prefix**: When "@" is used as a prefix for an identifier (variable, class name, etc.), it allows the creation of valid identifiers that would otherwise conflict with C# keywords. This is particularly useful when working with external systems or data sources where reserved keywords are used as identifiers.

   ```csharp
   string @class = "Class";
   int @int = 10;
   ```

   Here, `@class` and `@int` are valid identifiers, allowing the use of reserved keywords as variable names without causing compilation errors.

By leveraging the "@" symbol, developers can write cleaner and more readable code, especially in scenarios involving special characters in strings or when interfacing with systems using reserved keywords as identifiers.

## **String Methods:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

| Method                  | Description                                                                                                                             | Example                                                     | Output                                     |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------|
| `Length`                | Returns the number of characters in the string.                                                                                         | `string.Length`                                             | Returns an integer representing the length of the string.  |
| `ToUpper`               | Converts all characters in the string to uppercase.                                                                                     | `string.ToUpper()`                                          | Converts the string to uppercase.            |
| `ToLower`               | Converts all characters in the string to lowercase.                                                                                     | `string.ToLower()`                                          | Converts the string to lowercase.            |
| `Trim`                  | Removes leading and trailing white-space characters from the string.                                                                     | `string.Trim()`                                             | Removes leading and trailing white-space characters. |
| `Substring`             | Returns a substring of the string starting at the specified index and optionally continuing up to the specified length.                | `string.Substring(startIndex)` or `string.Substring(startIndex, length)` | Returns the specified substring.              |
| `IndexOf`               | Returns the index of the first occurrence of a specified substring within the string.                                                   | `string.IndexOf(substring)`                                | Returns the index of the first occurrence of the substring. |
| `LastIndexOf`           | Returns the index of the last occurrence of a specified substring within the string.                                                    | `string.LastIndexOf(substring)`                            | Returns the index of the last occurrence of the substring.  |
| `Contains`              | Determines whether the string contains a specified substring.                                                                            | `string.Contains(substring)`                               | Returns true if the string contains the substring; otherwise, false. |
| `StartsWith`            | Determines whether the string starts with the specified substring.                                                                      | `string.StartsWith(substring)`                             | Returns true if the string starts with the substring; otherwise, false. |
| `EndsWith`              | Determines whether the string ends with the specified substring.                                                                        | `string.EndsWith(substring)`                               | Returns true if the string ends with the substring; otherwise, false. |
| `Replace`               | Returns a new string in which all occurrences of a specified substring are replaced with another specified substring.                     | `string.Replace(oldValue, newValue)`                       | Returns a new string with replaced substrings. |
| `Split`                 | Splits the string into substrings based on the specified separator and returns an array of substrings.                                  | `string.Split(separator)`                                  | Returns an array of substrings.              |
| `Concat`                | Concatenates two or more strings.                                                                                                       | `string.Concat(str1, str2)` or `str1 + str2`                | Returns a new string that is the concatenation of the input strings. |
| `Equals`                | Determines whether two string objects have the same value.                                                                              | `string.Equals(otherString)`                               | Returns true if the strings are equal; otherwise, false. |
| `CompareTo`             | Compares two string objects and returns an integer indicating their relative position in the sort order.                                 | `string.CompareTo(otherString)`                           | Returns a negative value if the string is less than the otherString, 0 if they are equal, and a positive value if the string is greater. |
| `Concat` (Overload)     | Concatenates an array of strings.                                                                                                       | `string.Concat(strArray)`                                  | Returns a new string that is the concatenation of the input strings. |
| `Join`                  | Concatenates the elements of a string array, using the specified separator between each element.                                        | `string.Join(separator, strArray)`                         | Returns a single string with elements of the array separated by the specified separator. |
| `PadLeft`               | Returns a new string that left-aligns the characters in the string by padding them on the left with a specified character, for a specified total length. | `string.PadLeft(totalWidth, paddingChar)`                 | Returns a new string padded on the left.    |
| `PadRight`              | Returns a new string that right-aligns the characters in the string by padding them on the right with a specified character, for a specified total length. | `string.PadRight(totalWidth, paddingChar)`                | Returns a new string padded on the right.   |
| `ToUpperInvariant`      | Converts all characters in the string to uppercase using the casing rules of the invariant culture.                                    | `string.ToUpperInvariant()`                                | Converts the string to uppercase.            |
| `ToLowerInvariant`      | Converts all characters in the string to lowercase using the casing rules of the invariant culture.                                    | `string.ToLowerInvariant()`                                | Converts the string to lowercase.            |
| `TrimStart`             | Removes all leading occurrences of a set of characters specified in an array from the current string.                                  | `string.TrimStart(trimChars)`                              | Removes leading characters specified in the array. |
| `TrimEnd`               | Removes all trailing occurrences of a set of characters specified in an array from the current string.                                 | `string

## **String Properties:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here are the properties of the String class in C# explained in detail:

| Property      | Description                                                                                                       | Example                                   |
|---------------|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| `Chars`       | Gets the Char object at a specified position in the current String object.                                        | `char c = str.Chars[index];`             |
| `Length`      | Gets the number of characters in the current String object.                                                       | `int length = str.Length;`                |
| `IsReadOnly`  | Gets a value indicating whether the current String object is read-only.                                            | `bool isReadOnly = str.IsReadOnly;`      |
| `Item`        | Gets or sets the Char object at a specified position in the current String object.                                 | `str[0] = 'A'; char firstChar = str[0];` |

These properties provide access to various aspects of a string in C#, allowing for manipulation and retrieval of characters and length information. They offer valuable functionality for working with strings efficiently and effectively.

## **String Constructors:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here are the constructors of the String class in C# explained in detail:

| Constructor                      | Description                                                                                         | Example                                                     |
|----------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| `String(Char*, Int32)`           | Initializes a new instance of the String class to the value indicated by a specified pointer to an array of Unicode characters. | `string str = new string(charArray, startIndex, length);`  |
| `String(Char, Int32)`            | Initializes a new instance of the String class to the value indicated by a specified Unicode character repeated a specified number of times. | `string str = new string('a', 5);`                          |
| `String(Char[])`                 | Initializes a new instance of the String class to the value indicated by an array of Unicode characters. | `string str = new string(charArray);`                       |
| `String(Char[], Int32, Int32)`  | Initializes a new instance of the String class to the value indicated by a specified substring of Unicode characters. | `string str = new string(charArray, startIndex, length);`  |
| `String(SByte*)`                 | Initializes a new instance of the String class to the value indicated by a specified pointer to an array of signed bytes. | `string str = new string(bytePointer);`                    |
| `String(SByte*, Int32)`          | Initializes a new instance of the String class to the value indicated by a specified pointer to an array of signed bytes, and a specified length. | `string str = new string(bytePointer, length);`            |
| `String(SByte*, Int32, Encoding)`| Initializes a new instance of the String class to the value indicated by a specified pointer to an array of signed bytes, a specified length, and an encoding. | `string str = new string(bytePointer, length, encoding);`  |

These constructors provide various ways to create string instances, allowing for flexibility in initializing strings from different sources such as character arrays or byte arrays. They offer essential functionality for string manipulation and processing in C#.

## **String Builder:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

StringBuilder is a mutable sequence of characters that allows efficient manipulation of strings in C#. Unlike the String class, which is immutable (meaning its value cannot be changed after creation), StringBuilder provides a way to modify strings without creating new instances. This can lead to better performance, especially when dealing with a large number of string concatenations or modifications.

Here's an example demonstrating the usage of StringBuilder:

```csharp
using System;
using System.Text;

class Program
{
    static void Main(string[] args)
    {
        // Initialize a StringBuilder instance
        StringBuilder sb = new StringBuilder();

        // Append strings to the StringBuilder
        sb.Append("Hello, ");
        sb.Append("world!");
        
        // Insert a string at a specific position
        sb.Insert(6, "beautiful ");

        // Replace a substring with another string
        sb.Replace("world", "C# programming");

        // Convert StringBuilder to a string
        string result = sb.ToString();

        // Output the result
        Console.WriteLine(result);
    }
}
```

Output:
```
Hello, beautiful C# programming!
```

In this example:
- We create a StringBuilder instance `sb`.
- We use the `Append` method to add strings "Hello, " and "world!" to the StringBuilder.
- We use the `Insert` method to insert the string "beautiful " at index 6.
- We use the `Replace` method to replace the substring "world" with "C# programming".
- Finally, we convert the StringBuilder to a regular string using the `ToString` method and output the result.

StringBuilder provides various methods such as `Append`, `Insert`, `Replace`, `Remove`, and more for manipulating strings efficiently. It is particularly useful when you need to concatenate or modify strings dynamically, especially within loops or when building strings from multiple parts.

## **String Builder Methods:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here are the StringBuilder methods in C# explained in detail:

| Method                  | Description                                                                                                    | Example                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| `Append(Char)`          | Appends the string representation of a specified Unicode character to this instance.                           | `sb.Append('A');`                                       |
| `Append(String)`        | Appends a specified string to this instance.                                                                   | `sb.Append("Hello");`                                   |
| `AppendLine()`          | Appends the default line terminator to the end of the current StringBuilder instance.                         | `sb.AppendLine();`                                      |
| `AppendLine(String)`    | Appends a specified string followed by the default line terminator to the end of the current StringBuilder instance. | `sb.AppendLine("Hello");`                             |
| `AppendFormat(String, Object)` | Appends the string returned by processing a composite format string, which contains zero or more format items, to this instance. | `sb.AppendFormat("My name is {0}", "John");`       |
| `Clear()`               | Removes all characters from the current StringBuilder instance.                                                | `sb.Clear();`                                           |
| `Insert(Int32, Char)`   | Inserts the string representation of a specified Unicode character into this instance at the specified character position. | `sb.Insert(0, 'X');`                                  |
| `Insert(Int32, String)` | Inserts a specified string into this instance at the specified character position.                            | `sb.Insert(6, "world");`                               |
| `Remove(Int32, Int32)`  | Removes the specified range of characters from this instance.                                                  | `sb.Remove(6, 5);`                                      |
| `Replace(String, String)` | Replaces all occurrences of a specified string in this instance with another specified string.              | `sb.Replace("world", "C# programming");`               |
| `ToString()`            | Converts the value of this instance to a string.                                                              | `string result = sb.ToString();`                        |

These methods provide various ways to manipulate the contents of a StringBuilder instance, such as appending, inserting, replacing, and removing characters. They offer efficient string manipulation capabilities, especially when dealing with dynamic string construction or modification requirements.

## **String Vs String Builder:** [🏠](https://github.com/SMitra1993/theNETInterrogation/blob/master/4%20-%20OOPsConcept.md#oops-concept-)

Here's a detailed comparison between String and StringBuilder in C# presented in tabular form:

| Feature                      | String                                     | StringBuilder                                      |
|------------------------------|--------------------------------------------|----------------------------------------------------|
| Immutability                | Immutable - Cannot be modified once created. | Mutable - Contents can be modified dynamically.   |
| Memory Usage                | Creates a new instance for each modification, leading to memory fragmentation and performance overhead. | Modifies the existing instance, reducing memory fragmentation and overhead. |
| Performance                 | Poor performance for concatenating or modifying strings repeatedly, especially in loops. | Better performance for concatenating or modifying strings repeatedly, especially in loops, due to mutable nature. |
| Usage                       | Suitable for scenarios where strings are relatively static and few modifications are needed. | Suitable for scenarios where strings require frequent concatenation or modifications, especially within loops or dynamic scenarios. |
| Usage Guidelines            | Use when the content is static or requires minimal modifications. | Use when the content requires frequent concatenation or modifications, especially within loops or dynamic scenarios. |
| Syntax                      | Uses concatenation or interpolation for string manipulation. | Uses various methods such as Append, Insert, Replace for string manipulation. |
| Example                     | `string greeting = "Hello, " + name + "!";` | `StringBuilder sb = new StringBuilder();`<br>`sb.Append("Hello, ");`<br>`sb.Append(name);`<br>`sb.Append("!");`<br>`string greeting = sb.ToString();` |

In summary, String is immutable and suitable for scenarios where the content is relatively static or requires minimal modifications. StringBuilder, on the other hand, is mutable and provides better performance for scenarios requiring frequent concatenation or modifications, especially within loops or dynamic scenarios. It is more memory-efficient and leads to cleaner code in such scenarios.
