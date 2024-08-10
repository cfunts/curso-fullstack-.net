# Conditional Statements and Loops

## What you will learn in this course

Here are the key points from the text:

1. **Conditional Statements**:
   - **Purpose**: Allow execution of different code blocks based on specific conditions.
   - **Types**:
     - **if**: Executes a block of code if a condition is true.
     - **if else**: Provides an alternative block of code if the condition is false.
     - **if else if**: Checks multiple conditions in sequence.
     - **switch**: Selects one of many code blocks to execute based on the value of a variable.

2. **Operators and Precedence**:
   - **Purpose**: Operators perform operations on variables and values. Understanding their precedence is crucial for determining the order of execution.

3. **Loops**:
   - **Purpose**: Execute a block of code repeatedly until a condition is met.
   - **Types**:
     - **do while**: Executes the code block at least once and then continues executing as long as the condition is true.
     - **while**: Continuously executes the code block as long as the condition is true.
     - **for**: Executes the code block a specified number of times.
     - **for each**: Iterates through each item in a collection.

4. **Learning Outcome**:
   - Gain a better understanding of conditional statements, loops, and operators in C#.
   - Ability to write more complex and efficient C# applications.

This lesson aims to enhance your ability to create flexible and powerful applications by mastering these essential programming concepts.

## Operators and Operators Precedence

Here are the key points from the text:

1. **Conditional Statements**:
   - **Purpose**: Allow execution of different code blocks based on specific conditions.
   - **Types**:
     - **if**: Executes a block of code if a condition is true.
     - **if else**: Provides an alternative block of code if the condition is false.
     - **if else if**: Checks multiple conditions in sequence.
     - **switch**: Selects one of many code blocks to execute based on the value of a variable.

2. **Operators and Precedence**:
   - **Purpose**: Operators perform operations on variables and values. Understanding their precedence is crucial for determining the order of execution.

3. **Loops**:
   - **Purpose**: Execute a block of code repeatedly until a condition is met.
   - **Types**:
     - **do while**: Executes the code block at least once and then continues executing as long as the condition is true.
     - **while**: Continuously executes the code block as long as the condition is true.
     - **for**: Executes the code block a specified number of times.
     - **for each**: Iterates through each item in a collection.

4. **Learning Outcome**:
   - Gain a better understanding of conditional statements, loops, and operators in C#.
   - Ability to write more complex and efficient C# applications.

This lesson aims to enhance your ability to create flexible and powerful applications by mastering these essential programming concepts.

### Example

Certainly! Here are some examples illustrating conditional statements and loops in C#:

### Conditional Statements

**1. `if` Statement:**
```csharp
int number = 10;

if (number > 5)
{
    Console.WriteLine("The number is greater than 5.");
}
```

**2. `if else` Statement:**
```csharp
int number = 3;

if (number > 5)
{
    Console.WriteLine("The number is greater than 5.");
}
else
{
    Console.WriteLine("The number is 5 or less.");
}
```

**3. `if else if` Statement:**
```csharp
int number = 7;

if (number > 10)
{
    Console.WriteLine("The number is greater than 10.");
}
else if (number > 5)
{
    Console.WriteLine("The number is greater than 5 but less than or equal to 10.");
}
else
{
    Console.WriteLine("The number is 5 or less.");
}
```

**4. `switch` Statement:**
```csharp
int day = 3;
string dayName;

switch (day)
{
    case 1:
        dayName = "Monday";
        break;
    case 2:
        dayName = "Tuesday";
        break;
    case 3:
        dayName = "Wednesday";
        break;
    default:
        dayName = "Unknown day";
        break;
}

Console.WriteLine(dayName);
```

### Loops

**1. `do while` Loop:**
```csharp
int i = 0;

do
{
    Console.WriteLine("Value of i: " + i);
    i++;
} while (i < 5);
```

**2. `while` Loop:**
```csharp
int i = 0;

while (i < 5)
{
    Console.WriteLine("Value of i: " + i);
    i++;
}
```

**3. `for` Loop:**
```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine("Value of i: " + i);
}
```

**4. `foreach` Loop:**
```csharp
string[] fruits = { "Apple", "Banana", "Cherry" };

foreach (string fruit in fruits)
{
    Console.WriteLine(fruit);
}
```

These examples cover the basic usage of conditional statements and loops in C#. Each type of loop or statement is used in different scenarios depending on the requirements of the task you're coding.

## Conditional Statements

Here’s a summary of the key points from the text on conditional statements and loops in C#:

### Conditional Statements
1. **Purpose**: Control the flow of the program based on logical conditions.
2. **Types**:
   - **`if` Statement**: Executes code if the condition is true.
   - **`if-else` Statement**: Executes one block of code if the condition is true, and another block if it is false.
   - **`if-else-if` Ladder**: Used for multiple conditions to test different possibilities.
   - **`switch` Statement**: Useful for menu-driven applications and handling multiple discrete values.

### Examples
- **`if` Statement Example**:
  ```csharp
  bool isAuthenticated = true;
  if (isAuthenticated) {
      Console.WriteLine("You are logged in.");
  } else {
      Console.WriteLine("You are not logged in.");
  }
  ```
- **Ternary Operator Example**:
  ```csharp
  string result = isAuthenticated ? "You are logged in." : "You are not logged in.";
  Console.WriteLine(result);
  ```

- **`if-else-if` Ladder Example**:
  ```csharp
  int temperature = 50;
  if (temperature < 20) {
      Console.WriteLine("It's very cold outside.");
  } else if (temperature <= 50) {
      Console.WriteLine("It's moderate outside.");
  } else {
      Console.WriteLine("It's too hot outside.");
  }
  ```

- **`switch` Statement Example**:
  ```csharp
  string userType = "admin";
  switch (userType) {
      case "admin":
          Console.WriteLine("You have full access.");
          break;
      case "subadmin":
          Console.WriteLine("You can create or delete courses.");
          break;
      case "normal user":
          Console.WriteLine("You can access the courses.");
          break;
      default:
          Console.WriteLine("You are a trial user.");
          break;
  }
  ```

### Loops
1. **`do-while` Loop**:
   - Executes the block of code at least once, and then checks the condition.
   - **Example**:
     ```csharp
     int i = 1;
     do {
         Console.WriteLine(names[i]);
         i++;
     } while (i < names.Length);
     ```
   - **Key Point**: The loop body runs before the condition is evaluated.

2. **`foreach` Loop**:
   - Iterates over collections such as arrays or lists.
   - **Example**:
     ```csharp
     foreach (string name in names) {
         Console.WriteLine(name);
     }
     ```
   - **Key Point**: Simplifies iteration through collections but does not allow modifications of the collection during iteration.

### Summary
- Use **`if`** and **`if-else`** for simple conditions.
- Use **`switch`** for multiple discrete values.
- **`do-while`** ensures at least one execution of the loop body.
- **`foreach`** is ideal for iterating over collections without manual index management.

This overview should help you understand how to use conditional statements and loops effectively in C#.

### Example

Certainly! Here are practical examples for each type of conditional statement and loop in C#:

### 1. **`if` Statement**

```csharp
using System;

class Program
{
    static void Main()
    {
        bool isAuthenticated = true;

        if (isAuthenticated)
        {
            Console.WriteLine("You are logged in.");
        }
    }
}
```

### 2. **`if-else` Statement**

```csharp
using System;

class Program
{
    static void Main()
    {
        bool isAuthenticated = false;

        if (isAuthenticated)
        {
            Console.WriteLine("You are logged in.");
        }
        else
        {
            Console.WriteLine("You are not logged in.");
        }
    }
}
```

### 3. **`if-else-if` Ladder**

```csharp
using System;

class Program
{
    static void Main()
    {
        int temperature = 50;

        if (temperature < 20)
        {
            Console.WriteLine("It's very cold outside.");
        }
        else if (temperature <= 50)
        {
            Console.WriteLine("It's moderate outside.");
        }
        else
        {
            Console.WriteLine("It's too hot outside.");
        }
    }
}
```

### 4. **`switch` Statement**

```csharp
using System;

class Program
{
    static void Main()
    {
        string userType = "admin";

        switch (userType)
        {
            case "admin":
                Console.WriteLine("You have full access.");
                break;
            case "subadmin":
                Console.WriteLine("You can create or delete courses.");
                break;
            case "normal user":
                Console.WriteLine("You can access the courses.");
                break;
            default:
                Console.WriteLine("You are a trial user.");
                break;
        }
    }
}
```

### 5. **`do-while` Loop**

```csharp
using System;

class Program
{
    static void Main()
    {
        int i = 1;
        string[] names = { "Sara", "John", "Roger", "James" };

        do
        {
            Console.WriteLine(names[i]);
            i++;
        } while (i < names.Length);
    }
}
```

### 6. **`foreach` Loop**

```csharp
using System;

class Program
{
    static void Main()
    {
        string[] names = { "Sara", "John", "Roger", "James" };

        foreach (string name in names)
        {
            Console.WriteLine(name);
        }
    }
}
```

In these examples:
- **`if`** and **`if-else`** control the flow based on boolean conditions.
- **`if-else-if`** handles multiple conditions.
- **`switch`** selects one of many blocks of code to execute based on a variable's value.
- **`do-while`** ensures the loop executes at least once before checking the condition.
- **`foreach`** iterates over each item in a collection.

## Loops

Here are some notes on the provided text about loops in C#:

### Overview of Loops in C#
- **Purpose of Loops**: Loops are used to execute a block of statements multiple times. This is useful when the number of repetitions is not known in advance or when it is very large (e.g., 1,000 or 10,000 times).

### Types of Loops in C#
1. **`for` Loop**:
   - Used when the number of iterations is known or fixed.
   - Syntax: 
     ```csharp
     for (initialization; condition; increment/decrement)
     {
         // Statements
     }
     ```
   - Example: Iterating through an array of names.
     ```csharp
     for (int i = 0; i < names.Length; i++)
     {
         Console.WriteLine(names[i]);
     }
     ```
   - Reversing the iteration order:
     ```csharp
     for (int i = names.Length - 1; i >= 0; i--)
     {
         Console.WriteLine(names[i]);
     }
     ```

2. **`while` Loop**:
   - Used when the number of iterations is not predetermined.
   - Syntax:
     ```csharp
     while (condition)
     {
         // Statements
         // Increment/decrement
     }
     ```
   - Example:
     ```csharp
     int i = 0;
     while (i < names.Length)
     {
         Console.WriteLine(names[i]);
         i++;
     }
     ```

3. **`do while` Loop**:
   - Similar to the `while` loop but ensures that the loop body is executed at least once before checking the condition.
   - Syntax:
     ```csharp
     do
     {
         // Statements
         // Increment/decrement
     } while (condition);
     ```

4. **`foreach` Loop**:
   - Specifically used for iterating over collections or arrays.
   - Syntax:
     ```csharp
     foreach (var item in collection)
     {
         // Statements
     }
     ```
   - Example: Iterating through an array of names.
     ```csharp
     foreach (string name in names)
     {
         Console.WriteLine(name);
     }
     ```

### Key Points
- **Initialization**: In a `for` loop, initialization occurs only once at the start. In a `while` loop, initialization happens before entering the loop.
- **Condition Checking**: In a `for` loop, the condition is checked at the beginning of each iteration. In a `while` loop, the condition is checked before each iteration, and in a `do while` loop, it's checked after the loop body has executed.
- **Increment/Decrement**: In a `for` loop, increment or decrement occurs at the end of each iteration. In a `while` loop, it needs to be manually included inside the loop.

The text explains the usage of each loop with practical examples and describes how the flow of execution differs between these loops in C#.

### Example

Here are clear and practical examples for each type of loop in C#:

### 1. **`for` Loop Example**

This example iterates through an array of names and prints each name in the original order and then in reverse order.

```csharp
using System;

class Program
{
    static void Main()
    {
        string[] names = { "Alice", "Bob", "Charlie", "Diana", "Eve" };

        // Print names in original order
        Console.WriteLine("Names in original order:");
        for (int i = 0; i < names.Length; i++)
        {
            Console.WriteLine(names[i]);
        }

        // Print names in reverse order
        Console.WriteLine("Names in reverse order:");
        for (int i = names.Length - 1; i >= 0; i--)
        {
            Console.WriteLine(names[i]);
        }
    }
}
```

### 2. **`while` Loop Example**

This example prints names from an array using a `while` loop.

```csharp
using System;

class Program
{
    static void Main()
    {
        string[] names = { "Alice", "Bob", "Charlie", "Diana", "Eve" };
        int i = 0;

        // Print names using while loop
        Console.WriteLine("Names using while loop:");
        while (i < names.Length)
        {
            Console.WriteLine(names[i]);
            i++;
        }
    }
}
```

### 3. **`do while` Loop Example**

This example prints names from an array using a `do while` loop, ensuring the loop executes at least once.

```csharp
using System;

class Program
{
    static void Main()
    {
        string[] names = { "Alice", "Bob", "Charlie", "Diana", "Eve" };
        int i = 0;

        // Print names using do while loop
        Console.WriteLine("Names using do while loop:");
        do
        {
            Console.WriteLine(names[i]);
            i++;
        } while (i < names.Length);
    }
}
```

### 4. **`foreach` Loop Example**

This example prints names from an array using a `foreach` loop, which is ideal for iterating over collections.

```csharp
using System;

class Program
{
    static void Main()
    {
        string[] names = { "Alice", "Bob", "Charlie", "Diana", "Eve" };

        // Print names using foreach loop
        Console.WriteLine("Names using foreach loop:");
        foreach (string name in names)
        {
            Console.WriteLine(name);
        }
    }
}
```

### Summary

- **`for` Loop**: Used when you know the number of iterations ahead of time.
- **`while` Loop**: Used when the number of iterations is not known in advance.
- **`do while` Loop**: Ensures the loop body is executed at least once.
- **`foreach` Loop**: Simplifies iterating over collections, like arrays.

These examples cover the basic usage of each type of loop and demonstrate their primary applications in C# programming.

## Jump Statements

Here are the notes about the text on jump statements in C#:

### Overview
- **Jump Statements**: Used to transfer control within a program from one point to another based on specified conditions. Key jump statements include `break`, `continue`, `goto`, `return`, and `throw`.

### Key Jump Statements
1. **Break**
   - **Purpose**: Terminates the loop or switch statement in which it is present.
   - **Example**: In a `for` loop, using `break` will exit the loop when a specified condition is met.

2. **Continue**
   - **Purpose**: Skips the current iteration of a loop and proceeds with the next iteration.
   - **Example**: In a `for` loop, using `continue` will skip the rest of the code in the current iteration when a specified condition is met.

3. **Goto**
   - **Purpose**: Transfers control to a labeled statement in the program.
   - **Example**: In a `switch` statement, `goto` can be used to jump to another case label, bypassing any intermediate cases.

4. **Return**
   - **Purpose**: Terminates the execution of a method and returns control to the calling method. It can also return a value from the method.
   - **Example**: Exiting a method early with a return value.

5. **Throw**
   - **Purpose**: Creates an exception object and transfers control to the nearest exception handler. Used for exception handling.
   - **Example**: Using `throw` to manually raise an exception and handle it with `try-catch` blocks.

### Examples and Usage
- **Break Statement**: In a loop, if a condition `i = 5` is met, the loop terminates.
- **Continue Statement**: In a loop, if a condition `i = 5` is met, the current iteration is skipped, but the loop continues.
- **Goto Statement**: Used in `switch` statements to jump to specific cases, and can also jump to labels or line numbers.

### Additional Notes
- **Break vs. Continue**: `break` exits the loop entirely, whereas `continue` only skips the current iteration and continues with the next one.
- **Goto Statement**: Can be used with labels in the program to transfer control, but should be used with caution as it can make code harder to follow.

### Upcoming Sessions
- **Return and Throw**: These will be covered in detail in future sessions.

### Example

Certainly! Here are examples illustrating the use of each jump statement in C#:

### 1. **Break**
The `break` statement is used to exit a loop or switch statement.

```csharp
using System;

class Program
{
    static void Main()
    {
        for (int i = 0; i < 10; i++)
        {
            if (i == 5)
            {
                break; // Exit the loop when i is 5
            }
            Console.WriteLine(i);
        }
    }
}
```

**Output:**
```
0
1
2
3
4
```

### 2. **Continue**
The `continue` statement skips the rest of the current loop iteration and proceeds to the next iteration.

```csharp
using System;

class Program
{
    static void Main()
    {
        for (int i = 0; i < 10; i++)
        {
            if (i == 5)
            {
                continue; // Skip the rest of the loop body when i is 5
            }
            Console.WriteLine(i);
        }
    }
}
```

**Output:**
```
0
1
2
3
4
6
7
8
9
```

### 3. **Goto**
The `goto` statement transfers control to a labeled statement in the program.

```csharp
using System;

class Program
{
    static void Main()
    {
        int x = 10;
        goto Skip;
        
        Console.WriteLine("This line will be skipped");

        Skip:
        Console.WriteLine("This line is executed");
    }
}
```

**Output:**
```
This line is executed
```

### 4. **Return**
The `return` statement exits a method and optionally returns a value.

```csharp
using System;

class Program
{
    static void Main()
    {
        int result = Add(5, 3);
        Console.WriteLine(result);
    }

    static int Add(int a, int b)
    {
        return a + b; // Exit the method and return the sum
    }
}
```

**Output:**
```
8
```

### 5. **Throw**
The `throw` statement is used to throw an exception.

```csharp
using System;

class Program
{
    static void Main()
    {
        try
        {
            ThrowException();
        }
        catch (Exception ex)
        {
            Console.WriteLine("Caught exception: " + ex.Message);
        }
    }

    static void ThrowException()
    {
        throw new InvalidOperationException("This is an exception"); // Throw an exception
    }
}
```

**Output:**
```
Caught exception: This is an exception
```

These examples should give you a good idea of how each jump statement is used in different scenarios.

## Quiz


1. To determine the result of the code, we need to consider operator precedence. In C#, multiplication has higher precedence than addition. 

Given the code:

```csharp
int x = 10;
int y = 20;
int z = x + y * 2;
```

Here's the calculation step-by-step:

-  **Multiply `y` by `2`:**
   \[
   y \times 2 = 20 \times 2 = 40
   \]

- **Add `x` to the result:**
   \[
   x + 40 = 10 + 40 = 50
   \]

So, the result of the expression `z = x + y * 2` is **50**.

2. The correct syntax for a `do-while` loop in C# is:

```csharp
do
{
    // Code to be executed
} while (condition);
```

This loop will execute the code block at least once and then continue to execute it as long as the specified `condition` is `true`.

3. To determine the output of the given code, let's analyze it step-by-step:

```csharp
int x = 5;
int y = 10;

if (x == y)
{
    Console.WriteLine("x equals y");
}
else if (x > y)
{
    Console.WriteLine("x is greater than y");
}
else
{
    Console.WriteLine("y is greater than x");
}
```

- **Check `if (x == y)`**:  
   `x` (5) is not equal to `y` (10), so this condition is `false`.

- **Check `else if (x > y)`**:  
   `x` (5) is not greater than `y` (10), so this condition is also `false`.

- **`else` block**:  
   Since neither of the previous conditions was true, the code in the `else` block will be executed.

The output of the code is:

```
y is greater than x
```

4. The correct answer is:

**A while loop checks the condition before executing the loop body, while a do..while loop checks the condition after executing the loop body at least once.**

Here’s a breakdown:

- **`while` loop**: The condition is checked before executing the loop body. If the condition is `false` initially, the loop body might not execute at all.
  
  ```csharp
  while (condition)
  {
      // Code to be executed
  }
  ```

- **`do..while` loop**: The loop body is executed at least once before checking the condition. The loop will continue executing as long as the condition remains `true`.
  
  ```csharp
  do
  {
      // Code to be executed
  } while (condition);
  ```

5. The purpose of the `else if` statement in a conditional statement is:

**To test another condition if the previous condition tested is false.**

The `else if` statement allows you to specify additional conditions to test if the initial `if` condition is not met, enabling you to handle multiple scenarios within a single conditional structure.

6. The loop best suited for iterating over an array in C# is the:

**foreach loop**

The `foreach` loop is specifically designed to iterate over collections such as arrays, lists, and other enumerable types. It simplifies the code by automatically handling the iteration and access of each element in the array. Here's an example:

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```
7. Among the given operators, the operator with the highest precedence is:

**Increment (++)**

Here’s a brief overview of their precedence from highest to lowest:

- **Increment (++)**: Has the highest precedence among these operators. It is used to increase a variable's value by 1.

- **Multiplication (*)**: Has higher precedence than logical NOT and assignment but lower than increment.

- **Logical NOT (!)**: Checks the negation of a boolean value.

- **Assignment (=)**: Has the lowest precedence among these operators.

So, the `++` operator is evaluated first in expressions involving these operators.

8. The conditional statement that allows for multiple conditions to be tested is:

**if..else if**

The `if..else if` construct allows you to test multiple conditions sequentially. If the initial `if` condition is false, the program can then evaluate additional `else if` conditions in the specified order. If none of the `if` or `else if` conditions are true, the final `else` block (if present) will be executed.

Here's an example:

```csharp
if (condition1)
{
    // Code if condition1 is true
}
else if (condition2)
{
    // Code if condition1 is false and condition2 is true
}
else if (condition3)
{
    // Code if condition1 and condition2 are false and condition3 is true
}
else
{
    // Code if none of the above conditions are true
}
```

9. The loop that will always execute at least once is the:

**do..while**

In a `do..while` loop, the loop body is executed first before the condition is checked. This guarantees that the code inside the loop will run at least once, regardless of whether the condition is initially true or false.

Here’s an example:

```csharp
int count = 0;

do
{
    Console.WriteLine("This will always execute at least once.");
    count++;
} while (count < 0); // The condition is false, but the loop body executes once
```

10. The jump statement that transfers program control to a labeled statement is:

**goto**

The `goto` statement allows you to jump to a specified label within the code, bypassing other code. Here’s a basic example:

```csharp
using System;

class Program
{
    static void Main()
    {
        int x = 10;
        goto Skip; // Jump to the label 'Skip'

        Console.WriteLine("This line will be skipped");

        Skip:
        Console.WriteLine("This line is executed");
    }
}
```

In this example, the program will jump to the `Skip` label and execute the code there, skipping any intermediate lines.