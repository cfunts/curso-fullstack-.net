# Abstract Class

Here are the important notes from the text:

1. **Abstract Classes**:
   - An abstract class in C# cannot be instantiated; you cannot create an object of an abstract class.
   - It serves as a base class for other concrete classes to inherit from.
   - Abstract classes are used to define a common set of properties and methods that derived classes should implement.

2. **Concrete Classes**:
   - A concrete class is a class that is not abstract and can be instantiated.
   - Concrete classes must implement the abstract methods defined in their abstract base class.

3. **Creating Abstract Classes**:
   - The `abstract` keyword is used to define an abstract class.
   - Once a class is declared as abstract, it cannot be instantiated directly.

4. **Abstract Methods**:
   - An abstract method is a method that does not have a body and is defined in an abstract class.
   - If a class contains any abstract methods, that class must also be declared as abstract.
   - Abstract methods are essentially contractual; they must be implemented in derived classes.

5. **Non-Abstract Methods in Abstract Classes**:
   - An abstract class can also contain non-abstract methods, which do have a body.
   - These non-abstract methods can be accessed through instances of the derived (concrete) class.

6. **Example Demonstration**:
   - The text provides a practical example using a `BackAccount` abstract class with abstract methods (`deposit`, `withdraw`, `balance`), which are later implemented in a `SavingAccount` concrete class.
   - The `SavingAccount` class inherits from the `BackAccount` class and provides specific implementations for the abstract methods.
   - The program demonstrates how to instantiate the `SavingAccount` class and call its methods.

7. **Key Takeaways**:
   - An abstract class provides a template for concrete classes to follow.
   - If any method in a class is abstract, the class must be abstract as well.
   - Abstract methods enforce that derived classes implement specific behaviors.

8. **Practical Tips**:
   - In the code editor, quick actions and refactoring tools can be used to automatically implement abstract methods in derived classes.
   - Non-abstract methods in an abstract class can be accessed via instances of the derived class.

9. **Conclusion**:
   - The session concludes with a summary of the fundamental concepts of abstract classes and methods in C#, encouraging further exploration through case studies.


## Example

Here's an example in C# to illustrate the concepts of abstract classes and methods:

```csharp
using System;

namespace AbstractClassExample
{
    // Abstract class definition
    abstract class BankAccount
    {
        // Abstract methods (no implementation)
        public abstract void Deposit(decimal amount);
        public abstract void Withdraw(decimal amount);
        public abstract void ShowBalance();

        // Non-abstract method (has implementation)
        public void GetAccountDetails()
        {
            Console.WriteLine("Welcome to ABC Bank. Here are your account details:");
        }
    }

    // Concrete class that inherits from the abstract class
    class SavingAccount : BankAccount
    {
        private decimal balance = 0;

        // Implementing the abstract methods
        public override void Deposit(decimal amount)
        {
            balance += amount;
            Console.WriteLine($"Deposited: ${amount}. Current balance: ${balance}");
        }

        public override void Withdraw(decimal amount)
        {
            if (amount <= balance)
            {
                balance -= amount;
                Console.WriteLine($"Withdrew: ${amount}. Current balance: ${balance}");
            }
            else
            {
                Console.WriteLine("Insufficient funds for this withdrawal.");
            }
        }

        public override void ShowBalance()
        {
            Console.WriteLine($"Current balance: ${balance}");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Creating an instance of the concrete class
            SavingAccount myAccount = new SavingAccount();

            // Calling the non-abstract method from the abstract class
            myAccount.GetAccountDetails();

            // Calling the implemented abstract methods
            myAccount.Deposit(500);  // Depositing money
            myAccount.Withdraw(200); // Withdrawing money
            myAccount.ShowBalance(); // Showing the balance

            // Note: We cannot create an instance of the abstract class directly
            // BankAccount account = new BankAccount(); // This would cause a compilation error
        }
    }
}
```

### Explanation:
1. **Abstract Class (`BankAccount`)**:
   - Contains abstract methods `Deposit`, `Withdraw`, and `ShowBalance` that have no body. These methods must be implemented by any class that inherits from `BankAccount`.
   - Also includes a non-abstract method `GetAccountDetails` that has an implementation and can be used by derived classes.

2. **Concrete Class (`SavingAccount`)**:
   - Inherits from the `BankAccount` abstract class.
   - Provides implementations for the abstract methods, defining how deposits, withdrawals, and balance displays are handled.
   - The `balance` field stores the account balance, and the methods interact with this balance.

3. **Program Execution (`Main` Method)**:
   - An instance of `SavingAccount` is created.
   - The `GetAccountDetails` method from the abstract class is called to display a welcome message.
   - The implemented methods `Deposit`, `Withdraw`, and `ShowBalance` are called to perform actions on the account and display the results.

### Key Points:
- **Abstract Classes**: Cannot be instantiated directly but provide a blueprint for other classes.
- **Abstract Methods**: Must be implemented by derived classes.
- **Concrete Classes**: Provide the actual implementation of the abstract methods.