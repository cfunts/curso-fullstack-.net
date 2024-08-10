# Interfaces

Here are the important notes from the text about interfaces in C#:

1. **Definition of Interface:**
   - An interface in C# is described as a fully unimplemented class, meaning it only declares methods but does not provide their implementation.
   - It is considered a "pure abstract class" as it allows defining only abstract methods.

2. **Syntax and Declaration:**
   - Interfaces are created using the `interface` keyword.
   - By convention, interface names often start with "I" (e.g., `IRectangle`, `IBankAccount`), though this is optional.

3. **Characteristics of Interface Methods:**
   - All methods in an interface are public and abstract by default, meaning they must be implemented by any class that inherits the interface.
   - Interfaces cannot have fields, private members, or any concrete method implementations.

4. **Purpose of Interfaces:**
   - Interfaces specify what a class must do (the methods it must implement), but not how it should do it.
   - They are used to achieve loose coupling, total abstraction, component-based programming, and multiple inheritance.

5. **Multiple Inheritance:**
   - Unlike classes, where a class can inherit only one other class, a class can inherit multiple interfaces, allowing for multiple inheritance in C#.

6. **Practical Implementation:**
   - When a class implements an interface, it must provide concrete implementations for all of the abstract methods declared in the interface.
   - The text provides an example of implementing an `IBankAccount` interface and demonstrates how a class can implement multiple interfaces (`IBankAccount` and `IManageBank`).

7. **Dependency Injection and Component-Based Design:**
   - Interfaces add a plug-and-play architecture to applications, making it easier to inject dependencies and integrate components.

8. **Example Overview:**
   - The text walks through the creation of an interface `IBankAccount` with abstract methods and a class `SavingAccount` that implements these methods. 
   - It also shows how multiple interfaces can be implemented in a single class, demonstrating the concept of multiple inheritance.

9. **Conclusion:**
   - Interfaces enforce a strict contract that must be implemented by concrete classes, enabling structured and modular programming in C#. 
   - The concept of interfaces, along with examples of implementation, is discussed in a practical context, emphasizing their role in achieving multiple inheritance and separation of concerns.

These notes summarize the key concepts and practical implications of using interfaces in C#.

## Example

Here’s an example to illustrate how interfaces work in C# based on the notes provided:

### 1. Define the Interface

Let's create an interface called `IBankAccount` which will include abstract methods for deposit, withdrawal, and checking balance.

```csharp
public interface IBankAccount
{
    void Deposit(decimal amount);
    void Withdraw(decimal amount);
    decimal GetBalance();
}
```

### 2. Implement the Interface in a Class

Now, we'll create a class `SavingAccount` that implements the `IBankAccount` interface. This class must provide concrete implementations for the methods declared in the interface.

```csharp
public class SavingAccount : IBankAccount
{
    private decimal balance;

    public void Deposit(decimal amount)
    {
        balance += amount;
        Console.WriteLine($"Deposited {amount}, new balance is {balance}");
    }

    public void Withdraw(decimal amount)
    {
        if (amount <= balance)
        {
            balance -= amount;
            Console.WriteLine($"Withdrew {amount}, new balance is {balance}");
        }
        else
        {
            Console.WriteLine("Insufficient funds");
        }
    }

    public decimal GetBalance()
    {
        return balance;
    }
}
```

### 3. Using the Interface and Class

Here's how you can use the `SavingAccount` class with the `IBankAccount` interface:

```csharp
class Program
{
    static void Main(string[] args)
    {
        IBankAccount account = new SavingAccount();

        account.Deposit(500);
        account.Withdraw(200);
        Console.WriteLine($"Current balance is: {account.GetBalance()}");

        // Output:
        // Deposited 500, new balance is 500
        // Withdrew 200, new balance is 300
        // Current balance is: 300
    }
}
```

### 4. Example of Multiple Inheritance

If you want to add another interface, `IManageBank`, you can implement both interfaces in the same class.

```csharp
public interface IManageBank
{
    void OpenAccount();
    void CloseAccount();
}

public class SavingAccount : IBankAccount, IManageBank
{
    private decimal balance;

    public void Deposit(decimal amount)
    {
        balance += amount;
        Console.WriteLine($"Deposited {amount}, new balance is {balance}");
    }

    public void Withdraw(decimal amount)
    {
        if (amount <= balance)
        {
            balance -= amount;
            Console.WriteLine($"Withdrew {amount}, new balance is {balance}");
        }
        else
        {
            Console.WriteLine("Insufficient funds");
        }
    }

    public decimal GetBalance()
    {
        return balance;
    }

    public void OpenAccount()
    {
        Console.WriteLine("Opening Saving Account");
    }

    public void CloseAccount()
    {
        Console.WriteLine("Closing Saving Account");
    }
}

class Program
{
    static void Main(string[] args)
    {
        SavingAccount account = new SavingAccount();

        account.Deposit(500);
        account.Withdraw(200);
        Console.WriteLine($"Current balance is: {account.GetBalance()}");

        account.OpenAccount();
        account.CloseAccount();

        // Output:
        // Deposited 500, new balance is 500
        // Withdrew 200, new balance is 300
        // Current balance is: 300
        // Opening Saving Account
        // Closing Saving Account
    }
}
```

### Key Points:
- **Interface Implementation:** `SavingAccount` must implement all methods from `IBankAccount` and `IManageBank`.
- **Multiple Inheritance:** A single class can implement multiple interfaces, allowing it to inherit methods from more than one interface.

This example demonstrates the core concepts of interfaces in C#, including their role in enforcing contracts and enabling multiple inheritance.