# Classes and Interface

Here are the key points from the text about classes and interfaces:

### Abstract Class:
- **Abstract classes** allow the creation of classes with incomplete members that need to be implemented in derived classes.
- Declared using the `abstract` keyword before the class definition.
- **Abstract classes** can contain:
  - Member variables.
  - Non-abstract methods or properties.
  - Non-public methods and properties (including abstract ones).
  - Constants, static methods, and static members.
  - Constructors.

### Interface:
- **Interfaces** are data structures that define member signatures without providing actual implementations.
- Useful for defining contracts between members of different types with different implementations.
- Interfaces can define:
  - Methods.
  - Properties.
  - Indexers.
- Interface members are implicitly public.
- Interfaces can be implemented implicitly or explicitly.
- **Interfaces** cannot have:
  - Member variables.
  - Constants, static methods, or static members.
  - Constructors.
  - Non-public methods or properties.

### Interface vs. Abstract Class:
- **Abstract classes** can have member variables and non-abstract methods or properties, while interfaces cannot.
- A class or abstract class can inherit from only one class or abstract class, but can implement multiple interfaces.
- An interface can only extend other interfaces.
- Abstract classes allow more flexibility with constructors, access modifiers, and static members compared to interfaces.