# Object-Oriented Programming in C-Sharp

## Object-Oriented Programming Concepts

Here are the key notes from the text on object-oriented programming (OOP) in C#:

1. **Object-Oriented Programming (OOP) Overview**:
   - OOP is a software development approach that uses real-world terminology to create entities (objects) that interact with each other.
   - C# is an object-oriented programming language that supports the OOP paradigm.

2. **Advantages of OOP**:
   - OOP makes applications flexible, easy to manage, and allows for the addition of new features.
   - Code can be reused without redundancy, making it well-structured, easy to debug, and test.
   - The main aim of OOP is to bind data and the functions that operate on it, preventing other parts of the code from accessing this data directly (data hiding).

3. **Key Components of OOP**:
   - **Classes**: Define the structure using methods and properties that resemble real-world entities. Example: An "Employee" class with properties like `name`, `salary`, and `designation`, and methods like `calculateSalary`.
   - **Objects**: Instances of classes that hold different data in property fields and can interact with other objects.
   - **Encapsulation**: Hides data within a class. Data members are encapsulated by default and can be accessed externally only through access modifiers like `public`, `private`, `protected`, and `internal`.
   - **Abstraction**: (Related to encapsulation) Abstracts complex realities and shows only the necessary parts of an object.
   - **Inheritance**: Enables reusability of code by allowing a new class to inherit properties and methods from an existing class, saving time and effort.
   - **Polymorphism**: Allows one interface to be used for multiple functions, where one operation can be performed differently in various entities. This is often achieved through method overriding.

4. **Conclusion**:
   - The six components—classes, objects, encapsulation, abstraction, inheritance, and polymorphism—are essential in understanding OOP in C#.
   - These components will be discussed in detail in the upcoming sessions.

### Example 

Here’s a simple example in C# that illustrates the key concepts of object-oriented programming (OOP) mentioned in the text:

```csharp
using System;

// Define the 'Employee' class
public class Employee
{
    // Properties of the Employee class
    public string Name { get; set; }
    public double Salary { get; set; }
    public string Designation { get; set; }

    // Constructor to initialize the properties
    public Employee(string name, double salary, string designation)
    {
        Name = name;
        Salary = salary;
        Designation = designation;
    }

    // Method to calculate salary
    public double CalculateSalary()
    {
        // Example logic for calculating salary
        return Salary;
    }

    // Method to display employee details
    public void DisplayDetails()
    {
        Console.WriteLine($"Name: {Name}");
        Console.WriteLine($"Salary: {Salary}");
        Console.WriteLine($"Designation: {Designation}");
    }
}

// Define a subclass 'Manager' that inherits from 'Employee'
public class Manager : Employee
{
    public string Department { get; set; }

    // Constructor for Manager class
    public Manager(string name, double salary, string designation, string department)
        : base(name, salary, designation)
    {
        Department = department;
    }

    // Override the DisplayDetails method
    public new void DisplayDetails()
    {
        base.DisplayDetails();
        Console.WriteLine($"Department: {Department}");
    }
}

class Program
{
    static void Main()
    {
        // Create an instance of the Employee class
        Employee emp = new Employee("Alice", 50000, "Developer");
        emp.DisplayDetails();
        Console.WriteLine($"Calculated Salary: {emp.CalculateSalary()}");

        Console.WriteLine();

        // Create an instance of the Manager class
        Manager mgr = new Manager("Bob", 70000, "Senior Manager", "HR");
        mgr.DisplayDetails();
        Console.WriteLine($"Calculated Salary: {mgr.CalculateSalary()}");
    }
}
```

### Explanation:

1. **Class Definition**:
   - `Employee`: Defines properties (`Name`, `Salary`, `Designation`) and methods (`CalculateSalary`, `DisplayDetails`).
   - `Manager`: Inherits from `Employee`, adds a new property (`Department`), and overrides the `DisplayDetails` method.

2. **Objects**:
   - Instances of `Employee` and `Manager` are created to demonstrate the use of classes and methods.

3. **Encapsulation**:
   - Properties are encapsulated within the classes. They are accessed through public getter and setter methods.

4. **Inheritance**:
   - `Manager` class inherits from `Employee`, gaining its properties and methods while adding new ones.

5. **Polymorphism**:
   - The `DisplayDetails` method is overridden in the `Manager` class to provide additional information specific to the manager.

This example covers the basics of OOP in C# and demonstrates how classes, objects, encapsulation, inheritance, and polymorphism work together.

## Classes and Objects

Here’s a summary of the text on classes and objects in C#:

1. **Classes and Objects**:
   - **Class**: A blueprint or template for creating objects. Defines data members (fields), member functions (methods), properties, and events.
   - **Object**: An instance of a class. Accesses members defined within the class.

2. **Syntax for Declaring a Class**:
   - Format: `access specifier class ClassName { ... }`
   - Example: `public class Student { ... }`

3. **Class Example**:
   - **Student Class**: Contains data members (`studentId`, `studentName`) and a method (`void displayDetails`).
   - Default values are assigned (e.g., `0` for integers, `null` for strings).

4. **Creating and Using an Object**:
   - **Instantiating**: `ClassName objectName = new ClassName();`
   - Access members using the object: `objectName.methodName();`

5. **Encapsulation**:
   - Members are encapsulated by default. To access them from outside the class, use access modifiers (e.g., `public`).

6. **Methods in Class**:
   - **DisplayDetails Method**: Shows the current values of `studentId` and `studentName`.
   - **AcceptDetails Method**: Reads input from the user and assigns it to `studentId` and `studentName`.

7. **Type Conversion**:
   - Input from `Console.ReadLine` is a string. Convert it to other types (e.g., `int`) as needed.

8. **Example Workflow**:
   - Create a `Student` object.
   - Use `acceptDetails` to input data.
   - Use `displayDetails` to show data.

9. **Access Modifiers**:
   - Public members are accessible from outside the class. Private members are not.

This overview covers the basics of defining classes, creating objects, and using methods within a C# program.

### Example

Here’s an example in C# based on the concepts discussed:

```csharp
using System;

namespace Example
{
    // Define the Student class
    public class Student
    {
        // Data members (fields)
        public int studentId;
        public string studentName;

        // Method to display student details
        public void DisplayDetails()
        {
            Console.WriteLine("Student ID: " + studentId);
            Console.WriteLine("Student Name: " + studentName);
        }

        // Method to accept student details from user
        public void AcceptDetails()
        {
            Console.Write("Enter Student ID: ");
            // Read input and convert it to an integer
            studentId = Convert.ToInt32(Console.ReadLine());

            Console.Write("Enter Student Name: ");
            // Read input as a string
            studentName = Console.ReadLine();
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Instantiate the Student class
            Student student = new Student();

            // Accept details from the user
            student.AcceptDetails();

            // Display the details
            student.DisplayDetails();
        }
    }
}
```

### Explanation:
1. **Class Definition (`Student`)**:
   - **Fields**: `studentId` (integer) and `studentName` (string).
   - **Methods**:
     - `DisplayDetails()`: Prints the student’s ID and name.
     - `AcceptDetails()`: Prompts the user for the ID and name, then assigns these values to the fields.

2. **Main Program**:
   - Creates an instance of `Student`.
   - Calls `AcceptDetails()` to get input from the user.
   - Calls `DisplayDetails()` to show the entered details.

To run this code, copy it into a C# development environment like Visual Studio or a similar IDE, and execute it. You’ll be prompted to enter a student ID and name, and then the program will display the details.0

## Encapusulation and Abstraction

Here are the notes on the text discussing encapsulation and abstraction in C#:

### Encapsulation
- **Definition**: Encapsulation involves hiding the internal details of an object from the outside world. It is about bundling the data (variables) and methods (functions) that operate on the data into a single unit, typically a class.
- **Purpose**: It helps in data security by restricting direct access to some of an object's components, which can prevent accidental interference and misuse.
- **Implementation**:
  - **Private Access Modifier**: By default, if no access modifier is specified, class members are private, meaning they cannot be accessed from outside the class.
  - **Public Access Modifier**: To allow external access to certain members, they need to be exposed through public properties or methods.

### Abstraction
- **Definition**: Abstraction is the concept of exposing only the essential details of an object while hiding the complex implementation details.
- **Purpose**: It simplifies interactions by showing only what is necessary and hiding the rest, making the system easier to use and understand.
- **Implementation**:
  - **Abstract Classes and Methods**: Abstraction can be achieved using abstract classes and methods. Abstract classes define methods that must be implemented by derived classes, but do not themselves provide complete implementations.
  - **Real-life Example**: Using an ATM machine—users interact with a simplified interface (card, PIN, amount) without needing to know the internal workings of the ATM.

### Access Modifiers in C#
- **Public**: Least restricted; members are accessible from anywhere outside the class.
- **Private**: Most restricted; members are accessible only within the class itself.
- **Protected**: Members are accessible within the class and by derived classes (child classes).
- **Internal**: Members are accessible only within the same namespace.
- **Protected Internal**: Members are accessible within the same namespace and by derived classes (child classes) in other namespaces.

### Practical Application
- Demonstrated with a `Student` class:
  - Without any access modifier, members are private by default.
  - Members with a public modifier can be accessed from outside the class, while private members cannot.
- Upcoming sessions will explore practical implementations of access modifiers and their impact on encapsulation and abstraction.

This overview covers the key aspects of encapsulation and abstraction in C# and how access modifiers influence these concepts.

### Example
Here’s a simple example to illustrate encapsulation and abstraction in C#:

### Example: A `BankAccount` Class

#### Encapsulation
In this example, the `BankAccount` class encapsulates the details of the account. The balance is hidden from outside access and can only be modified through public methods.

```csharp
public class BankAccount
{
    // Private field, encapsulated from outside
    private decimal balance;

    // Constructor to initialize the account with an initial balance
    public BankAccount(decimal initialBalance)
    {
        balance = initialBalance;
    }

    // Public method to deposit money, encapsulates the balance field
    public void Deposit(decimal amount)
    {
        if (amount > 0)
        {
            balance += amount;
        }
    }

    // Public method to withdraw money, encapsulates the balance field
    public bool Withdraw(decimal amount)
    {
        if (amount > 0 && amount <= balance)
        {
            balance -= amount;
            return true;
        }
        return false;
    }

    // Public method to check balance, provides abstraction
    public decimal GetBalance()
    {
        return balance;
    }
}
```

#### Abstraction
In this example, the `BankAccount` class provides a simplified interface to interact with a bank account, hiding the details of how the balance is managed. Users only need to know how to deposit, withdraw, and check the balance, without knowing the internal details of the balance management.

#### Usage
Here’s how you would use the `BankAccount` class in a program:

```csharp
public class Program
{
    public static void Main()
    {
        // Create a new bank account with an initial balance of 1000
        BankAccount account = new BankAccount(1000m);

        // Deposit money into the account
        account.Deposit(500m);

        // Attempt to withdraw money
        bool success = account.Withdraw(200m);
        if (success)
        {
            Console.WriteLine("Withdrawal successful.");
        }
        else
        {
            Console.WriteLine("Withdrawal failed.");
        }

        // Get the current balance
        decimal balance = account.GetBalance();
        Console.WriteLine($"Current balance: {balance}");
    }
}
```

### Key Points
- **Encapsulation**: The `balance` field is private, meaning it cannot be accessed directly from outside the class. Access is controlled through public methods like `Deposit`, `Withdraw`, and `GetBalance`.
- **Abstraction**: Users interact with the `BankAccount` class through its public methods without needing to understand the internal workings of how the balance is managed.


## Constructurs

Here's a summary of the key points about constructors in C# from the text:

### **Overview of Constructors**
- **Definition**: A constructor is a special method used to initialize an object of a class.
- **Default Constructor**: Automatically provided by the compiler if no constructor is defined by the user. Initializes attributes with default values (e.g., `0` for integers, `null` for strings).

### **Types of Constructors**
1. **Default Constructor**: 
   - Name matches the class name.
   - No return type.
   - Initializes attributes to default values unless explicitly defined.

2. **Parameterized Constructor**:
   - Allows passing parameters to set initial values for attributes.
   - Example: `public Student(int sid, string sName)`.

3. **Copy Constructor**:
   - Initializes an object using another object of the same class.

4. **Private Constructor**:
   - Restricts object creation from outside the class.
   - Useful for implementing singleton patterns or factory methods.

5. **Static Constructor**:
   - Initializes static members of a class.
   - Called automatically before any static member access.

### **Demonstration**
- **Example**: A `Student` class with attributes `studentId` and `studentName`.
  - **Without Parameters**: Uses default values (`studentId` is `0`, `studentName` is `null`).
  - **With Parameters**: Assigns provided values to `studentId` and `studentName`.

### **Constructor Overloading**
- A class can have multiple constructors with different parameters.
- Allows flexibility in object creation.
- Demonstrated through both default and parameterized constructors in the example.

### **Important Points**
- Constructors are invoked implicitly when creating an object.
- Constructors do not need explicit invocation; they are called automatically.
- More details on other types of constructors (copy, private, static) will be covered in future sessions.

This covers the basics of constructors in C# and provides insight into their functionality and different types.

### Example

Here's an example in C# demonstrating the use of different types of constructors:

```csharp
using System;

public class Student
{
    public int StudentId { get; set; }
    public string StudentName { get; set; }

    // Default Constructor
    public Student()
    {
        StudentId = 0;
        StudentName = "Anonymous";
    }

    // Parameterized Constructor
    public Student(int id, string name)
    {
        StudentId = id;
        StudentName = name;
    }

    // Copy Constructor
    public Student(Student other)
    {
        StudentId = other.StudentId;
        StudentName = other.StudentName;
    }

    // Static Constructor
    static Student()
    {
        Console.WriteLine("Static constructor called");
    }

    public void DisplayDetails()
    {
        Console.WriteLine($"Student ID: {StudentId}");
        Console.WriteLine($"Student Name: {StudentName}");
    }
}

public class Program
{
    public static void Main()
    {
        // Calling Default Constructor
        Student student1 = new Student();
        student1.DisplayDetails();
        
        Console.WriteLine();

        // Calling Parameterized Constructor
        Student student2 = new Student(123, "John Doe");
        student2.DisplayDetails();
        
        Console.WriteLine();

        // Calling Copy Constructor
        Student student3 = new Student(student2);
        student3.DisplayDetails();
    }
}
```

### **Explanation:**

1. **Default Constructor**: 
   - `public Student()` initializes `StudentId` to `0` and `StudentName` to `"Anonymous"`.
   - `Student student1 = new Student();` uses this constructor.

2. **Parameterized Constructor**: 
   - `public Student(int id, string name)` allows setting specific values for `StudentId` and `StudentName`.
   - `Student student2 = new Student(123, "John Doe");` uses this constructor.

3. **Copy Constructor**: 
   - `public Student(Student other)` creates a new `Student` object by copying the attributes from another `Student` object.
   - `Student student3 = new Student(student2);` uses this constructor to copy values from `student2`.

4. **Static Constructor**: 
   - `static Student()` is called once before any static members are accessed or any objects are created.
   - It outputs "Static constructor called" to the console.

5. **DisplayDetails Method**: 
   - Prints the `StudentId` and `StudentName` of the `Student` object.

When running the program, you will see that the static constructor is called first, followed by the creation of objects using the default, parameterized, and copy constructors.

## Inheritance

Here's a summary and key points from the text on inheritance in C#:

### Summary
The session covers inheritance in object-oriented programming with a focus on C#. Inheritance allows one class to inherit fields and methods from another class, promoting code reuse and simplifying maintenance. The text explains various types of inheritance, provides a practical example, and highlights the role of the `base` keyword in method calls.

### Key Points

1. **Inheritance Concept**:
   - **Definition**: Inheritance is a relationship between classes where a subclass inherits fields and methods from a superclass.
   - **Purpose**: It enables code reuse by allowing a new class to use the properties and methods of an existing class and to extend or modify them.

2. **Types of Inheritance**:
   - **Single Inheritance**: A single subclass inherits from one superclass.
   - **Multi-level Inheritance**: A subclass inherits from another subclass, forming a chain.
   - **Hierarchical Inheritance**: Multiple subclasses inherit from a single superclass, but the subclasses do not inherit from each other.
   - **Hybrid Inheritance**: Combines different types of inheritance patterns. However, C# does not support multiple inheritance directly with classes (a class inheriting from more than one class).
   - **Multiple Inheritance (Interface-based)**: Achieved using interfaces in C#, where a class can implement multiple interfaces.

3. **Example**:
   - **Vehicle Example**: A `Vehicle` class can be the base class with common properties like speed and color. Specific vehicle types like `Bike`, `Car`, `Bus`, and `Truck` inherit from `Vehicle` and can have additional properties or methods. For example, `Bike` can be further categorized into `Scooter` and `Bicycle`.

4. **Implementation in C#**:
   - **Base and Derived Classes**: In C#, a derived class inherits from a base class. For example, `Marks` class inherits from `StudentInfo` class.
   - **Method Overriding and Base Keyword**: Derived classes can override methods from the base class. The `base` keyword allows calling methods from the base class within overridden methods.

5. **Practical Example**:
   - **StudentInfo and Marks Classes**: The `StudentInfo` class has properties and methods for student details. The `Marks` class inherits from `StudentInfo` and adds additional properties for marks. Method calls to `acceptDetails` and `displayDetails` in the `Marks` class can use the `base` keyword to invoke the base class methods if needed.

6. **Method Call Sequence**:
   - When a derived class method is called, it can chain to the base class method using `base.methodName()` to ensure both the base and derived class functionalities are executed.

7. **Concept Summary**:
   - Inheritance promotes code reuse and modularity by allowing classes to build on top of other classes. Understanding the types and implementation of inheritance is crucial for effective object-oriented programming in C#.

### Example

Here’s a simple example of inheritance in C# to illustrate the concepts discussed:

### Example: Vehicle and Car Classes

#### Base Class: Vehicle

```csharp
// Base class
public class Vehicle
{
    // Fields
    public string Color { get; set; }
    public int Speed { get; set; }

    // Constructor
    public Vehicle(string color, int speed)
    {
        Color = color;
        Speed = speed;
    }

    // Method
    public void DisplayInfo()
    {
        Console.WriteLine($"Color: {Color}, Speed: {Speed} km/h");
    }
}
```

#### Derived Class: Car

```csharp
// Derived class
public class Car : Vehicle
{
    // Additional field
    public int NumberOfDoors { get; set; }

    // Constructor
    public Car(string color, int speed, int numberOfDoors)
        : base(color, speed) // Call base class constructor
    {
        NumberOfDoors = numberOfDoors;
    }

    // Overridden method
    public new void DisplayInfo()
    {
        base.DisplayInfo(); // Call base class method
        Console.WriteLine($"Number of Doors: {NumberOfDoors}");
    }
}
```

#### Main Program

```csharp
using System;

class Program
{
    static void Main()
    {
        // Create an instance of Car
        Car myCar = new Car("Red", 120, 4);

        // Display information about the car
        myCar.DisplayInfo();
    }
}
```

### Explanation

1. **Base Class (Vehicle)**:
   - **Fields**: `Color` and `Speed` to store common properties.
   - **Constructor**: Initializes `Color` and `Speed`.
   - **Method**: `DisplayInfo` prints the properties of the vehicle.

2. **Derived Class (Car)**:
   - **Field**: `NumberOfDoors` specific to cars.
   - **Constructor**: Initializes `Color`, `Speed`, and `NumberOfDoors` using the base class constructor.
   - **Overridden Method**: `DisplayInfo` in `Car` calls the base class method and adds additional information about `NumberOfDoors`.

3. **Main Program**:
   - **Instantiation**: Creates an instance of `Car` and initializes it with specific values.
   - **Method Call**: `DisplayInfo` method of `Car` is called to print the properties, showing how the `Car` class inherits from `Vehicle` and extends its functionality.

This example demonstrates basic inheritance in C#, where `Car` inherits common properties and methods from `Vehicle` and adds its own.

## Graded Quiz

1. An access modifier in object-oriented programming is:

**A way to control the visibility of a class, method, or field.**

Access modifiers determine how and where the members of a class (such as fields, methods, and properties) can be accessed or modified. Common access modifiers include `public`, `private`, `protected`, and `internal` in C#.

1. A constructor in object-oriented programming is:

**A special method that is used to create an instance of a class and initialize its state.**

Constructors are called automatically when an object of a class is created, and they are used to set up the initial values of the object's fields or properties.

1. Inheritance in object-oriented programming is:

**The process of defining a new class based on an existing class.**

Inheritance allows a new class (subclass or derived class) to inherit properties and methods from an existing class (superclass or base class), enabling code reuse and creating a hierarchical relationship between classes.

1. A method in object-oriented programming is:

**A function that is associated with an object or class and can be called to perform a specific task.**

Methods define behaviors for objects and classes, allowing you to execute code and perform operations on the object's data.

1. A structure in object-oriented programming is:

**A type of user-defined data type that is similar to a class, but with the key difference that its members are public by default.**

Structures (`struct` in C#) are used to group related variables (fields) into a single entity. Unlike classes, structures are value types and typically used for small, lightweight objects.

1. The correct answer is:

**A constructor is used to create objects and allocate memory for them.**

Constructors are special methods that are automatically called when an object is created. They initialize the object’s state and allocate the necessary resources for the object to be used. Constructors do not destroy objects or modify existing ones; those tasks are handled by other methods and destructors or finalizers, if applicable.

1. The purpose of inheritance in object-oriented programming is:

**To create new classes by deriving from existing classes.**

Inheritance allows new classes (derived classes) to inherit properties and methods from existing classes (base classes), promoting code reuse and establishing a hierarchical relationship between classes.

1. The correct answer is:

**All of the above.**

In object-oriented programming, access modifiers include `private`, `public`, and `protected`. These modifiers control the visibility and accessibility of class members (such as fields, methods, and properties) and help enforce encapsulation by restricting access to certain parts of a class.

1. The correct answer is:

**A method is a function that is called on an object, while a function is not associated with any object.**

In object-oriented programming, a method is a function that is associated with an object or class and operates on the data contained within that object. A function, in contrast, is a more general concept that is not necessarily tied to an object or class and can exist independently in procedural programming.

1. The correct answer is:

**Private members can only be accessed by the same class, while protected members can be accessed by the same class and its subclasses.**

- **Private**: Members marked as `private` are accessible only within the class that defines them. They cannot be accessed from outside the class or by derived (subclass) classes.
- **Protected**: Members marked as `protected` are accessible within the class that defines them and by subclasses (derived classes). They are not accessible from outside the class hierarchy.

1. The correct answer is:

**A method that is used to create an object.**

A constructor is a special method that is automatically called when an object is created. It initializes the object's state and sets up its initial values. Constructors do not destroy or modify objects; those tasks are handled by other mechanisms or methods.

1. The correct answer is:

**A class that cannot be instantiated.**

An abstract class is a class that cannot be instantiated on its own and is typically used as a base class for other classes. It can contain abstract methods (which have no implementation and must be implemented by derived classes) as well as non-abstract methods and properties. The purpose of an abstract class is to provide a common interface and base functionality for derived classes.

1. The correct answer is:

**The ability of an object to take on many forms.**

Polymorphism in object-oriented programming refers to the ability of different objects to be treated as instances of the same class through a common interface. It allows objects to be accessed through references of their base class type, and the appropriate method implementation is determined at runtime. This concept enables objects of different classes to be treated as objects of a common superclass and supports method overriding and overloading.

1. The correct answer is:

**None of the above.**

Method overloading is the process of defining multiple methods with the same name but different parameter lists within the same class. This allows a class to have more than one method with the same name, as long as the methods differ in the number or type of their parameters.

1. The correct answer is:

**To control the visibility and accessibility of class members.**

Access modifiers determine how and where class members (such as fields, methods, and properties) can be accessed. They help enforce encapsulation by specifying whether members are accessible from outside the class or only within the class itself or its subclasses.

1. The correct answer is:

**An instance method can access non-static fields and methods of the class, while a static method cannot.**

- **Static Method**: Belongs to the class itself rather than to any specific object. It can be called without creating an instance of the class and can only access static fields and methods.

- **Instance Method**: Belongs to an instance of the class and can access both instance fields and static fields. It requires an object of the class to be called.