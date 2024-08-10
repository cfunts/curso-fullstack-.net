# Polymorphismo

Here are the important notes from the text about polymorphism in C#:

1. **Definition of Polymorphism**:
   - Polymorphism is derived from a Greek word meaning "many forms."
   - It allows methods in a class to have multiple forms with the same name but different functionalities.
   - Example: A class `Person` could have child classes like `Professor`, `Student`, and `Clerk`, each redefining their behaviors while sharing the same method names.

2. **Types of Polymorphism in C#**:
   - **Compile-time Polymorphism** (Static Polymorphism):
     - Achieved through method overloading and constructor overloading.
     - Method overloading allows multiple methods with the same name but different parameters (different numbers, types, or order of parameters).
     - Also called early binding or static binding because the method to be called is determined at compile time.
   - **Runtime Polymorphism** (Dynamic Polymorphism):
     - Achieved through method overriding in derived classes.
     - Requires inheritance and enables methods to be redefined in child classes.
     - Uses `virtual` keyword for methods in the base class and `override` keyword in derived classes.

3. **Method Overloading**:
   - Multiple methods in the same class with the same name but different parameters.
   - Parameters can differ in number, type, or order.
   - Example: A class `ConsolePrinter` with three `Print` methods that have different numbers of string parameters.

4. **Method Overriding**:
   - Overriding occurs in derived classes, allowing them to redefine base class methods.
   - Requires inheritance and enables runtime polymorphism.
   - The base method is marked with the `virtual` keyword, and the overriding method in the derived class is marked with the `override` keyword.
   - Example: An `Animal` class with a `MakeSound` method can be overridden in a `Dog` class to change the behavior from "animal makes a sound" to "dog barks."

5. **Abstract Methods**:
   - An abstract method provides a contract that must be implemented in derived classes.
   - If you don't want to keep the base implementation, the method can be declared as abstract instead of virtual.

6. **Practical Implementation**:
   - The text mentions upcoming sessions where these concepts will be demonstrated practically to solidify understanding.

This summary captures the core ideas and examples related to polymorphism in C# discussed in the text.

## Example

Let's break down the concepts with an example in C# that illustrates both **method overloading** and **method overriding**.

### 1. **Method Overloading (Compile-time Polymorphism)**

```csharp
using System;

public class Calculator
{
    // Method to add two integers
    public int Add(int a, int b)
    {
        return a + b;
    }

    // Overloaded method to add three integers
    public int Add(int a, int b, int c)
    {
        return a + b + c;
    }

    // Overloaded method to add two doubles
    public double Add(double a, double b)
    {
        return a + b;
    }
}

public class Program
{
    public static void Main()
    {
        Calculator calc = new Calculator();

        Console.WriteLine(calc.Add(5, 10));       // Calls the method with two int parameters
        Console.WriteLine(calc.Add(5, 10, 15));   // Calls the method with three int parameters
        Console.WriteLine(calc.Add(5.5, 10.5));   // Calls the method with two double parameters
    }
}
```

### Explanation:
- The `Calculator` class has three `Add` methods with the same name but different parameters:
  - `Add(int, int)`
  - `Add(int, int, int)`
  - `Add(double, double)`
- The compiler determines which method to call based on the method signature during compile-time.

### 2. **Method Overriding (Runtime Polymorphism)**

```csharp
using System;

// Base class
public class Animal
{
    // Virtual method in the base class
    public virtual void MakeSound()
    {
        Console.WriteLine("The animal makes a sound.");
    }
}

// Derived class
public class Dog : Animal
{
    // Overriding the base class method
    public override void MakeSound()
    {
        Console.WriteLine("The dog barks.");
    }
}

// Derived class
public class Cat : Animal
{
    // Overriding the base class method
    public override void MakeSound()
    {
        Console.WriteLine("The cat meows.");
    }
}

public class Program
{
    public static void Main()
    {
        Animal myAnimal = new Animal();  // Base class object
        Animal myDog = new Dog();        // Derived class object
        Animal myCat = new Cat();        // Derived class object

        myAnimal.MakeSound(); // Calls the base class method
        myDog.MakeSound();    // Calls the Dog class method
        myCat.MakeSound();    // Calls the Cat class method
    }
}
```

### Explanation:
- The `Animal` class has a method `MakeSound` marked with the `virtual` keyword.
- The `Dog` and `Cat` classes override this method using the `override` keyword.
- When calling `MakeSound()` on a `Dog` or `Cat` object, the overridden method in the respective derived class is executed instead of the base class method.
- This decision is made at runtime, demonstrating runtime polymorphism.

These examples illustrate how polymorphism works in C#, with method overloading happening at compile-time and method overriding happening at runtime.