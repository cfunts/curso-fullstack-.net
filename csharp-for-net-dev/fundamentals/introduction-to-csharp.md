# Introduction to the C-Sharp programming language

## What you will learn in this Lessson

- **Introduction to C-Sharp:** The lesson will introduce the C-Sharp programming language, focusing on its basic syntax, datatypes, and code execution.

- **History and Versions:** An overview of the history of C-Sharp and its different versions will be provided.

- **Development Environment Setup:** Instructions on setting up the development environment using Visual Studio, a powerful IDE for C-Sharp programming, will be included.

- **Fundamentals of C-Sharp:** The lesson will cover fundamental concepts in C-Sharp programming, starting with variables and data types.

- **Outcome:** By the end of the lesson, you'll have a solid foundation in C-Sharp programming and be prepared to write your own C-Sharp applications.

- **Next Steps:** The lesson will conclude with an invitation to continue learning in the next video.

## Introduction to C-Sharp

Here are the key notes from the text about C# programming fundamentals:

1. **Overview of C#:**
   - C# is a modern, object-oriented programming language developed by Microsoft.
   - It runs on the .NET framework, which must be installed locally on your machine.
   - C# applications can be developed on various operating systems, including Linux, Windows, iOS, and Android.
   - It is standardized by ECMA and ISO.

2. **Capabilities:**
   - C# is designed for CLI (Common Language Infrastructure) and can be used to develop a wide range of applications, such as:
     - Windows applications
     - Client apps
     - Components and libraries
     - Services and APIs
     - Web applications
     - Mobile applications
     - Cloud applications
     - Gaming applications

3. **Community Support:**
   - There is a large community supporting C#, with resources available on platforms like Stack Overflow and GitHub.

4. **Features of C#:**
   - **Simplicity:** C# is designed to be simple and easy to use.
   - **Performance:** It is fast in terms of performance.
   - **Object-Oriented:** Supports object-oriented programming principles.
   - **Type Safety:** Provides type safety to prevent type errors.
   - **Variable Declarations:** Supports various types and their declarations.
   - **Interoperability:** Allows interaction with other programming languages and systems.
   - **Scalability:** Suitable for scaling applications.
   - **Rich Library:** Includes a comprehensive set of libraries.
   - **Modern Programming Aspects:** Incorporates modern features of programming languages.

5. **Upcoming Sessions:**
   - The speaker expresses excitement about discussing C# programming fundamentals in upcoming sessions.


## History of C# Version

Here are some notes on the text discussing the C# version history:

1. **Introduction to C#**:
   - C# was first introduced with the .NET Framework 1.0 in 2002.
   - The language has evolved significantly since then.

2. **Version Evolution**:
   - Each new version of C# builds on the previous one, adding new features and improvements.
   - Developers can choose the version of C# based on their application's requirements and the features they need.

3. **Features by Version**:
   - **C# 6.0**: Introduced enhancements such as improved syntax for catch blocks.
   - **C# 8.0**: Introduced disposable structs, among other features.

4. **Current Version**:
   - The latest version is C# 11.0, released in November 2022.
   - C# 11.0 is supported in the .NET 7 framework.
   - Visual Studio 2022 is the compatible IDE for this version.

5. **Upcoming Projects**:
   - The speaker is excited to teach C# programming using the latest version, C# 11.0, in Visual Studio 2022.

6. **Conclusion**:
   - The speaker encourages staying tuned for the next session.

## C# Code Execution

Here are the key points from the text about C# code execution:

1. **Overview of C#:** C# is a general-purpose, strongly-typed, lexically scoped, object-oriented, and component-oriented programming language.

2. **Compilation Process:**
   - **Initial Compilation:** When C# code is written, it is first compiled using a C# compiler (also known as CAC compiler). The compiler checks for errors in the code.
   - **Error Handling:** If errors are found, the compiler notifies the developer to correct them. The code is recompiled after corrections are made.

3. **Intermediate Code Generation:**
   - **Intermediate Language (IL):** If no errors are found, the code is converted into Intermediate Language (IL) or Common Intermediate Language (CIL). This IL code is platform-independent, allowing it to run on any operating system.

4. **Execution Management:**
   - **.NET Framework:** The IL code is managed by the .NET Framework, specifically by the Just-In-Time (JIT) compiler, which converts the IL code into native machine code that can be executed.
   - **Executable Files:** The result of the compilation and execution process is typically an executable file (.EXE) or a dynamic link library file (.DLL). An EXE file represents a program that can be executed, while a DLL file contains reusable libraries.

5. **Summary:** The text outlines the compilation and execution process of C# code, emphasizing the role of the compiler, the conversion to IL, and the final execution by the JIT compiler.

## Variable and DataType

Here's a summary and key notes from the text about variables in C#:

1. **Definition of a Variable**:
   - A variable is a symbolic name for a memory location that holds a value.
   - Variables can be manipulated, assigned, or reassigned during program execution.

2. **Declaration in C#**:
   - In C#, variables must be declared before use.
   - This involves specifying both the name and type of the variable.
   - C# is a statically typed language, meaning types are checked at compile-time.

3. **Types of Variables**:
   - **Local Variables**: Declared within a block and used within that block.
   - **Non-static Variables**: Declared at the class level, specific to an instance of a class.
   - **Static Variables**: Declared at the class level and shared across all instances.
   - **Constant Variables**: Cannot be changed once initialized.
   - **Read-only Variables**: Can be assigned only during initialization or in the constructor.

4. **Data Types**:
   - **Value Types**: Store the actual value (e.g., `int`, `float`, `double`).
   - **Reference Types**: Store references to objects (e.g., `string`, classes).
   - **Pointer Types**: Hold references to other variables (less commonly used in modern C#).

5. **Syntax for Declaring Variables**:
   - Define the data type, then the variable name, and optionally initialize it with a value.
   - Example: `string name = "King Coacher";`

6. **Data Types Examples**:
   - **String**: Stores a sequence of characters.
   - **Int**: Stores integer values.
   - **Float**: Stores floating-point values with `F` suffix.
   - **Double**: Stores double-precision floating-point values.
   - **Char**: Stores a single character.
   - **Bool**: Stores boolean values (`true` or `false`).

7. **Practical Example**:
   - A C# console application example demonstrates declaring and printing variables using `Console.WriteLine`.
   - Shows variables of types `string`, `int`, `float`, `double`, `char`, and `bool`.

8. **Upcoming Sessions**:
   - The speaker plans to cover more on using variables in real-time scenarios and their practical applications.

This overview should give you a good understanding of the basics of variables in C# and their usage.

### Example

Here's a simple example demonstrating variable declaration and usage in a C# console application:

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declaring variables
        string name = "King Coacher"; // String variable
        int age = 30;                 // Integer variable
        float discount = 12.50F;      // Float variable (note the 'F' suffix)
        double salary = 50000.75;     // Double variable
        char gender = 'M';            // Char variable
        bool isValid = true;          // Boolean variable

        // Printing variable values
        Console.WriteLine("Name: " + name);
        Console.WriteLine("Age: " + age);
        Console.WriteLine("Discount: " + discount);
        Console.WriteLine("Salary: " + salary);
        Console.WriteLine("Gender: " + gender);
        Console.WriteLine("Is Valid: " + isValid);
    }
}
```

### Explanation:

- **`string name`**: Holds a sequence of characters (e.g., "King Coacher").
- **`int age`**: Stores an integer value (e.g., 30).
- **`float discount`**: Stores a floating-point number (e.g., 12.50), with 'F' suffix indicating it's a float.
- **`double salary`**: Stores a double-precision floating-point number (e.g., 50000.75).
- **`char gender`**: Stores a single character (e.g., 'M').
- **`bool isValid`**: Stores a boolean value (e.g., `true`).

The `Console.WriteLine` statements print the values of these variables to the console. This example demonstrates the basic use of different data types and how to display their values in a C# application.

## Demo: C# Hello World Program

Here are the key points from the text about writing a "Hello World" program in C#:

1. **Introduction to "Hello World" Program:**
   - The "Hello World" program is a simple program that displays "Hello World" on the screen.
   - It is commonly used to introduce beginners to a new programming language.

2. **Creating a New Project:**
   - Start by creating a new Console Application project in C#.
   - Console Applications in C# are supported across various operating systems, including Linux, macOS, and Windows.

3. **Project Setup:**
   - Choose a console application project type and select .NET 6.0 or 7.0 as the framework. These versions are good for training and development.
   - The project setup will generate a basic structure including dependencies and the `Program.cs` file.

4. **Program.cs Overview:**
   - In `Program.cs`, the `Console.WriteLine` method is used to print text to the screen.
   - In .NET 6.0 and 7.0, the `main` method is deprecated; instead, statements are written directly in `Program.cs`.

5. **Running the Application:**
   - You can run the application by using the project's name or pressing the F5 key.
   - The initial output will be "Hello World" as specified.

6. **Customizing Output:**
   - You can modify the text inside `Console.WriteLine` to display different messages.
   - Example: Changing it to `Console.WriteLine("Let's learn C# programming.");` will display both messages when run.

7. **Purpose of the Program:**
   - The "Hello World" program helps familiarize beginners with basic syntax and requirements of C# programming.

8. **Conclusion:**
   - The "Hello World" program is typically the first step when learning a new programming language.
   - It serves as an introduction to the language's syntax and basic operations.

This summary provides a concise overview of the process and purpose of creating a "Hello World" program in C#.

### Example

Here's a simple example of a "Hello World" program in C#:

1. **Create a New Project:**
   - Open your IDE (e.g., Visual Studio).
   - Create a new Console Application project.

2. **Write the Code:**
   - Replace the contents of the `Program.cs` file with the following code:

   ```csharp
   using System;

   namespace HelloWorld
   {
       class Program
       {
           static void Main(string[] args)
           {
               Console.WriteLine("Hello World");
               Console.WriteLine("Let's learn C# programming.");
           }
       }
   }
   ```

3. **Run the Program:**
   - Press F5 or run the application.
   - The output will be:

     ```
     Hello World
     Let's learn C# programming.
     ```

### Breakdown of the Code:

- `using System;` – Imports the System namespace, which contains basic classes like `Console`.
- `namespace HelloWorld` – Defines a namespace for the program.
- `class Program` – Defines a class named `Program`.
- `static void Main(string[] args)` – The entry point of the application. This is where the program starts execution.
- `Console.WriteLine("Hello World");` – Prints "Hello World" to the console.
- `Console.WriteLine("Let's learn C# programming.");` – Prints another message to the console.

Feel free to modify the text inside `Console.WriteLine` to display any message you like.


## Quiz

Sure, here's the summary in English:

1. **What is C#?**
   - **A programming language for developing applications on the .NET framework.**

2. **How do you execute C# code?**
   - **By compiling the code and then running the resulting executable file.**

3. **What is Visual Studio?**
   - **An IDE for developing applications on the .NET framework.**

4. **What is a variable in C#?**
   - **A named memory location used to store a value that can be modified during program execution and has a specific data type.**