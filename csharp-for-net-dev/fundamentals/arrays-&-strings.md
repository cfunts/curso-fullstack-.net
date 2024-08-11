# C-Sharp Arrays and Strings

## Arrays and Types of Arrays

Here are the important notes from the text:

1. **Introduction to Arrays**:
   - Arrays are fundamental in programming, allowing storage of multiple literal values in contiguous memory locations.
   - Unlike variables that store a single value, arrays store a collection of elements of the same data type.
   - Elements in an array are identified by their index, starting from zero up to `n-1` where `n` is the size of the array.

2. **Syntax for Declaring Arrays**:
   - Arrays in C# are declared using square brackets `[]` after the data type, followed by the array name.
   - Example: `int[] arrayName = new int[5];` declares an array of 5 integers.
   - Arrays can also be initialized during declaration.

3. **Advantages of Arrays**:
   - Code optimization: Declaring an array reduces the need to declare multiple variables.
   - Random access: Array elements can be accessed randomly using their index.
   - Easy traversal: Elements can be easily traversed using loops.
   - Data manipulation: Arrays allow easy modification of existing data.
   - Sorting: In C#, arrays are a class that supports data sorting and arrangement.

4. **Types of Arrays in C#**:
   - **Single-Dimensional Array**:
     - Also known as a one-dimensional array.
     - Contains a single row of elements, stored in a homogeneous manner.
     - Syntax: `int[] arrayName = new int[5];`
   
   - **Multi-Dimensional Array**:
     - Contains more than one row of elements, forming a matrix-like structure.
     - Can be two-dimensional or three-dimensional, depending on requirements.
     - Example: `int[,] arrayName = new int[3,3];` creates a 3x3 array.
     - In C#, dimensions are separated by commas within square brackets.
   
   - **Jagged Array**:
     - An array of arrays where each sub-array can have different lengths.
     - Useful for storing collections of arrays with varying sizes.
     - Syntax: `int[][] jaggedArray = new int[3][];` where each sub-array can have different lengths.
     - The first bracket specifies the number of parent arrays, while the second specifies the dimensions of each sub-array.
     - Jagged arrays can contain single-dimensional or multi-dimensional sub-arrays.

5. **Practical Implementation**:
   - Practical examples and implementation details will be covered in the upcoming session for better understanding.

6. **Conclusion**:
   - The session wraps up with an invitation to the next session where more practical examples will be discussed.

These notes capture the key concepts and details discussed in the text.

### Example

Here are examples based on the key points from the text:

1. **Single-Dimensional Array Example**:
   - **Declaration**:
     ```csharp
     int[] ages = new int[5]; // Declares an array to hold 5 integers
     ```
   - **Initialization**:
     ```csharp
     ages[0] = 21;
     ages[1] = 25;
     ages[2] = 30;
     ages[3] = 35;
     ages[4] = 40;
     ```
   - **Combined Declaration and Initialization**:
     ```csharp
     int[] ages = new int[] { 21, 25, 30, 35, 40 };
     ```

2. **Multi-Dimensional Array Example**:
   - **Declaration**:
     ```csharp
     int[,] matrix = new int[3, 3]; // Declares a 3x3 two-dimensional array
     ```
   - **Initialization**:
     ```csharp
     matrix[0, 0] = 1; matrix[0, 1] = 2; matrix[0, 2] = 3;
     matrix[1, 0] = 4; matrix[1, 1] = 5; matrix[1, 2] = 6;
     matrix[2, 0] = 7; matrix[2, 1] = 8; matrix[2, 2] = 9;
     ```
   - **Combined Declaration and Initialization**:
     ```csharp
     int[,] matrix = {
         { 1, 2, 3 },
         { 4, 5, 6 },
         { 7, 8, 9 }
     };
     ```

3. **Jagged Array Example**:
   - **Declaration**:
     ```csharp
     int[][] jaggedArray = new int[3][]; // Declares a jagged array with 3 sub-arrays
     ```
   - **Initialization**:
     ```csharp
     jaggedArray[0] = new int[] { 1, 2, 3 };    // First sub-array with 3 elements
     jaggedArray[1] = new int[] { 4, 5 };       // Second sub-array with 2 elements
     jaggedArray[2] = new int[] { 6, 7, 8, 9 }; // Third sub-array with 4 elements
     ```
   - **Accessing Elements**:
     ```csharp
     int firstElement = jaggedArray[0][0]; // Accesses the first element of the first sub-array (value is 1)
     int secondElement = jaggedArray[1][1]; // Accesses the second element of the second sub-array (value is 5)
     ```

These examples demonstrate the practical application of the concepts discussed in the text.

## Manipulating Arrays

Here are the key notes from the text:

1. **Arrays in Programming**:
   - The text discusses how to manipulate different types of arrays: single-dimensional, multidimensional, and jagged arrays.
   - **Single-Dimensional Array**:
     - An array is declared with a specific size, e.g., `marks` with size 5.
     - Values can be assigned to each index, e.g., `marks[0] = 25`.
     - Arrays can be initialized at the time of declaration.
     - The `foreach` loop is recommended for printing array elements.

2. **Multidimensional Array**:
   - Arrays can have multiple dimensions, e.g., a 2D array with rows and columns.
   - The example given declares a multidimensional array with 3 rows and 4 columns.
   - Values can be assigned to specific positions in the array, e.g., `multiArray[0, 0] = 23`.
   - Initialization can also be done at the time of declaration, grouping values by rows.

3. **Printing Array Elements**:
   - For multidimensional arrays, a traditional `for` loop is suggested for printing elements.
   - The outer loop represents rows, and the inner loop represents columns.
   - The text emphasizes printing elements in a matrix format, using a tab between elements and a new line after each row.

4. **Jagged Array**:
   - A jagged array is an array of arrays, where the second dimension does not have a fixed size.
   - The example provided declares a jagged array with two arrays, the first with size 2 and the second with size 3.
   - The jagged array can have varying sizes for each inner array, based on requirements.

5. **Conclusion**:
   - The text concludes with a brief recap, ensuring that the concept of arrays is clear, and mentions that the next session will continue the discussion.

These notes summarize the key points related to array manipulation, initialization, and printing techniques.

### Example

Here’s an example based on the text that demonstrates how to work with single-dimensional, multidimensional, and jagged arrays in C#:

### 1. Single-Dimensional Array
```csharp
// Declaration and initialization of a single-dimensional array
int[] marks = new int[5] { 25, 45, 60, 55, 78 };

// Printing array elements using foreach loop
foreach (int mark in marks)
{
    Console.WriteLine(mark);
}
```

### 2. Multidimensional Array
```csharp
// Declaration and initialization of a 2D array (3 rows, 4 columns)
int[,] multiArray = new int[3, 4]
{
    { 23, 45, 67, 89 },
    { 12, 34, 56, 78 },
    { 90, 81, 72, 63 }
};

// Printing elements in matrix format using nested for loops
for (int i = 0; i < 3; i++)  // Loop through rows
{
    for (int j = 0; j < 4; j++)  // Loop through columns
    {
        Console.Write(multiArray[i, j] + "\t");
    }
    Console.WriteLine();  // New line after each row
}
```

### 3. Jagged Array
```csharp
// Declaration and initialization of a jagged array
int[][] jaggedArray = new int[2][];

// Assigning arrays with different sizes to each element
jaggedArray[0] = new int[2] { 10, 20 };  // First row with 2 elements
jaggedArray[1] = new int[3] { 30, 40, 50 };  // Second row with 3 elements

// Printing elements of the jagged array
for (int i = 0; i < jaggedArray.Length; i++)
{
    for (int j = 0; j < jaggedArray[i].Length; j++)
    {
        Console.Write(jaggedArray[i][j] + "\t");
    }
    Console.WriteLine();  // New line after each inner array
}
```

### Explanation
- **Single-Dimensional Array**: This example shows how to declare an array, initialize it with values, and print those values using a `foreach` loop.
- **Multidimensional Array**: A 2D array (matrix) is declared and initialized. The elements are printed in a matrix format using nested `for` loops.
- **Jagged Array**: This example demonstrates a jagged array where each row can have a different number of elements. The array is printed using nested loops, showing how the jagged structure works.

## Strings and String Methods

Here are the key notes from the text about strings and string methods in C#:

1. **String Basics**:
   - In C#, a string is a sequence of characters stored in the `System.String` class.
   - A string represents a group of characters that can be stored in a single variable.
   - Internally, strings are stored as an array of characters but are treated as a single variable.

2. **String Operations**:
   - Common operations on strings include concatenation, comparison, substring extraction, searching within a string, trimming whitespace, and replacing characters.

3. **String Keyword**:
   - The `string` keyword in C# is an alias for the `System.String` class. Both `string` and `String` are equivalent and can be used interchangeably.

4. **String Declaration**:
   - Strings can be declared using the `string` keyword or directly using the `System.String` class.

5. **Immutable vs. Mutable Strings**:
   - **Immutable Strings**:
     - Strings created from the `System.String` class are immutable, meaning that any modification creates a new string object in memory, leaving the original unchanged.
     - When modifying an existing string, a new memory location is allocated, and the original string becomes unreferenced.
   - **Mutable Strings**:
     - The `StringBuilder` class is used for mutable strings, allowing modifications without creating new instances in memory.
     - `StringBuilder` is preferred when frequent modifications are needed, as it improves performance by not allocating new memory with each change.

6. **String Methods**:
   - **Clone**: Creates a copy of the string.
   - **CompareTo**: Compares two strings and returns an integer indicating their equality.
   - **Contains**: Checks if a specified character or substring exists within the string.
   - **EndsWith**: Checks if the string ends with a specified character or substring.
   - **Equals**: Compares two strings and returns a Boolean value indicating if they are equal.
   - **ToUpper/ToLower**: Converts the string to uppercase or lowercase, respectively.
   - **Insert**: Inserts a string or character at a specified position within the string.
   - **IndexOf**: Returns the index position of the first occurrence of a specified character or substring within the string.

7. **Conclusion**:
   - Mutable strings (`StringBuilder`) can be modified, while immutable strings (`System.String`) cannot.
   - The speaker is excited to teach various implementations of strings in the next session.

### Example

Here are some examples illustrating the concepts discussed:

### 1. **String Declaration**
```csharp
// Using the string keyword
string greeting = "Hello, World!";

// Using the System.String class
System.String farewell = "Goodbye!";
```

### 2. **Immutable String Example**
```csharp
string original = "Hello";
string modified = original + ", World!";

// original is still "Hello"
// modified is "Hello, World!"
```
- In this example, modifying `original` by concatenating `", World!"` creates a new string `modified`. The original string remains unchanged.

### 3. **Mutable String Example with StringBuilder**
```csharp
StringBuilder sb = new StringBuilder("Hello");
sb.Append(", World!");

// sb now contains "Hello, World!"
```
- Here, `StringBuilder` allows you to append to the string without creating a new object, thus using the same memory location.

### 4. **String Methods Examples**

- **Clone**
```csharp
string original = "Hello";
string copy = (string)original.Clone();
```

- **CompareTo**
```csharp
string s1 = "apple";
string s2 = "banana";
int comparison = s1.CompareTo(s2); // Returns -1 because "apple" is less than "banana"
```

- **Contains**
```csharp
string phrase = "The quick brown fox";
bool containsQuick = phrase.Contains("quick"); // Returns true
```

- **EndsWith**
```csharp
string fileName = "document.txt";
bool endsWithTxt = fileName.EndsWith(".txt"); // Returns true
```

- **Equals**
```csharp
string str1 = "Hello";
string str2 = "Hello";
bool areEqual = str1.Equals(str2); // Returns true
```

- **ToUpper / ToLower**
```csharp
string lowerCase = "hello";
string upperCase = lowerCase.ToUpper(); // Returns "HELLO"
```

- **Insert**
```csharp
string name = "John";
string fullName = name.Insert(0, "Mr. "); // Returns "Mr. John"
```

- **IndexOf**
```csharp
string sentence = "Hello, World!";
int index = sentence.IndexOf('W'); // Returns 7
```

These examples demonstrate how strings can be manipulated and the different methods available to work with them in C#.

## Manipulating Strings

Here are the key notes from the text on manipulating strings in C#:

### Introduction to String Manipulation
- **Declaration and Printing**: 
  - Strings are declared using `string str1 = "hello world";`.
  - To print a string, use `Console.WriteLine(str1);`.

### Basic String Operations
- **String Length**: 
  - To get the length of a string, including spaces, use `str1.Length`.
- **Concatenation**: 
  - To concatenate two strings, use `Console.WriteLine(str1.Concat(str2));`.
  - Alternatively, store the concatenation result in a variable: `string str3 = str1 + str2;`.
- **String Comparison**: 
  - To compare two strings, use `Console.WriteLine(str1.Equals(str2));`. It returns `true` if they are equal, otherwise `false`.

### Running the Program
- The text walks through running a simple program that prints the string, its length, and the result of concatenation and comparison.
- A syntax error occurs when concatenating, which is resolved by correcting the syntax and re-running the program.

### Mutable vs Immutable Strings
- **Immutable Strings**:
  - Declared normally using `string s1 = "C Sharp programming";`.
  - Immutable means the string cannot be changed once created; any modification creates a new string.

- **Mutable Strings (StringBuilder)**:
  - Use the `StringBuilder` class from `System.Text` for mutable strings.
  - Strings in `StringBuilder` can be modified using `Append`, allowing continuous modification without creating new strings.
  - `StringBuilder` is efficient for scenarios requiring multiple modifications to a string.

### Summary
- The session explains basic string operations in C#, including how to handle both mutable and immutable strings.
- The concept of `StringBuilder` is introduced as a way to efficiently handle mutable strings.

### Conclusion
- The session ends by reinforcing the concepts and encouraging practice for better understanding.

### Example

Here's an example based on the text, demonstrating string manipulation in C#:

```csharp
using System;
using System.Text;

class Program
{
    static void Main()
    {
        // Declaring a string
        string str1 = "hello world";
        Console.WriteLine("Original string: " + str1);

        // Getting the length of the string
        int length = str1.Length;
        Console.WriteLine("Length of the string: " + length);

        // Concatenating two strings
        string str2 = " C Sharp programming";
        string str3 = str1 + str2;
        Console.WriteLine("Concatenated string: " + str3);

        // Comparing two strings
        bool areEqual = str1.Equals(str2);
        Console.WriteLine("Are the strings equal? " + areEqual);

        // Immutable string example
        string s1 = "C Sharp programming";
        string s2 = "Java programming";
        Console.WriteLine("Immutable string s1: " + s1);
        Console.WriteLine("Immutable string s2: " + s2);

        // Mutable string example using StringBuilder
        StringBuilder sb = new StringBuilder();
        sb.Append("C Sharp programming");
        sb.Append(" and Java programming");
        Console.WriteLine("Mutable string using StringBuilder: " + sb.ToString());

        // Modifying the StringBuilder
        sb.Append(" are popular languages.");
        Console.WriteLine("Modified StringBuilder string: " + sb.ToString());
    }
}
```

### Explanation:
1. **String Declaration and Printing**:
   - `str1` is declared as `"hello world"`.
   - The string is printed using `Console.WriteLine`.

2. **String Length**:
   - The length of `str1` is obtained using `str1.Length`.

3. **Concatenation**:
   - `str1` and `str2` are concatenated and stored in `str3`.
   - The concatenated string is printed.

4. **String Comparison**:
   - `str1` is compared with `str2` using `str1.Equals(str2)`.

5. **Immutable Strings**:
   - `s1` and `s2` are declared as immutable strings.

6. **Mutable Strings with StringBuilder**:
   - A `StringBuilder` object is created and modified using `Append`.
   - The mutable string is printed after each modification. 

This example covers basic string operations, and the use of `StringBuilder` for handling mutable strings in C#.

## Quiz

Here's a summary of the key concepts covered in the questions:

1. **Arrays in C#**:
   - An array is a collection of values of the same data type, stored in contiguous memory locations.
   - Types of arrays in C#: 
     - **Single-dimensional arrays**: A simple list of elements.
     - **Multi-dimensional arrays**: Arrays with more than one dimension, like matrices.
     - **Jagged arrays**: Arrays of arrays, where each array can be of different lengths.

2. **Strings in C#**:
   - A string is a sequence of characters stored as an array of characters in contiguous memory locations.
   - The **Length** property is used for strings to determine the number of characters, while **Count** is a method used for certain types of collections in C#.

3. **ToString() Method in C#**:
   - `ToString()` is a predefined function provided by the .NET framework for manipulating strings. It allows conversion of objects to their string representation and can be used to perform various operations like concatenation, searching, and replacing.

These questions test knowledge of fundamental concepts in C#, such as arrays, strings, and basic string operations, which are essential for understanding data storage and manipulation in the language.