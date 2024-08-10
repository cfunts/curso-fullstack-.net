# .NET Core Architecture and .NET CLI

## Introduction to .NET CLI

Here are the key notes from the text:

1. **.NET Core CLI Overview**:
   - .NET Core CLI is a cross-platform tool for creating, restoring packages, building, and publishing .NET applications.
   - It supports third-party package installations and is used internally by Visual Studio for these tasks.

2. **Commands and Functionality**:
   - .NET Core CLI commands can be used to create, build, and run .NET Core projects.
   - It manages dependencies, including adding, removing, or updating third-party dependencies using the .NET NuGet package manager.
   - The CLI is integrated into build and deployment pipelines due to its command-line interface.

3. **Installation and Verification**:
   - The .NET Core CLI is automatically installed with the .NET Core SDK, so no separate installation is required.
   - The installation can be verified by checking the .NET SDK version or by running the `.NET` command, which should display usage and help options.

4. **Command Structure**:
   - All .NET Core CLI commands start with the `dotnet` driver.
   - After `dotnet`, a command is specified to perform a specific action, followed by arguments and options (e.g., project type, project name).
   - This structure allows users to generate and modify .NET projects efficiently.

5. **Advanced Commands**:
   - The text hints at more advanced commands and project modification commands available in .NET Core CLI.
   - There is anticipation for further exploration of these topics in future sessions.

6. **Conclusion**:
   - The session ends with a note of excitement for the next session, where more advanced topics will be covered. 

These notes capture the essential points of the text regarding .NET Core CLI commands and their usage.

## .NET CLI Commands

Here are the key notes from the text about .NET Core CLI commands:

1. **Introduction to .NET Core CLI Commands**:
   - The session discusses various .NET Core CLI commands.
   - The `dotnet-help` command lists all available commands.

2. **Key Commands**:
   - **`dotnet new`**: Initializes a new .NET project.
   - **`dotnet build`**: Builds the project, checking for warnings and errors.
   - **`dotnet run`**: Executes the project.
   - **`dotnet migrate`**: Migrates projects based on `project.json` to newer formats.
   - **`dotnet sln`**: Modifies solution files.

3. **Advanced Commands**:
   - **NuGet**: Manages third-party packages.
   - **MS Build** and **VS Test**: Other advanced commands for build and testing purposes.

4. **Project Creation Example**:
   - The example involves generating a new web project in the D drive's Snippets folder using the `dotnet new web` command.
   - The project is then built using the `dotnet build` command, followed by running it with the `dotnet run` command.
   - The output is a basic "Hello World" displayed in a browser.

5. **Conclusion**:
   - The session aims to clarify the usage of .NET Core CLI commands and concludes with an encouragement to stay tuned for the next session.

## The .NET Core Platform

Here are the key notes from the text about the .NET Core platform:

1. **.NET Core Platform Overview**:
   - The .NET Core platform is composed of several key components:
     - **CLI Tools**: Command-line tools for building and managing .NET Core applications.
     - **Roslyn**: The language compiler for C#, F#, and Visual Basic.
     - **CoreFX**: A set of frameworks and libraries common to all supported programming languages.
     - **Core CLR**: A Just-In-Time (JIT) based Common Language Runtime (CLR) that handles memory management, execution of managed and unmanaged code, and security/authentication.

2. **Language Compilers**:
   - .NET Core supports multiple programming languages, including C#, F#, and Visual Basic, through the Roslyn compiler.
   - C# programs or .NET Core applications are compiled into Intermediate Language (IL) code, which is then executed by the .NET runtime environment provided by the Core CLR.
   - The **Roslyn** compiler is specifically used for C# and Visual Basic, while F# has its own compiler called **FSC**.

3. **Core CLR**:
   - Core CLR is the runtime used in .NET Core applications, responsible for compiling and executing these applications.
   - It converts code into a low-level or intermediate language before compiling it into the final executable format.
   - Core CLR provides several important features:
     - **Garbage Collection**: Automatically manages memory allocation and deallocation.
     - **Just-In-Time Compilation**: Compiles code at runtime to improve performance.
     - **Memory Management**: Efficiently handles memory use.
     - **Exception Handling**: Manages runtime errors.
     - **Authentication and Authorization**: Ensures secure access to applications.

4. **Advantages of Core CLR**:
   - It is lightweight and modular compared to the full .NET Framework, making applications robust, scalable, and fast.
   - Optimized for modern hardware and execution environments.
   - Consumes fewer resources than the traditional .NET Framework.

5. **CoreFX Libraries**:
   - CoreFX provides a wide range of libraries for .NET Core applications, supporting various functionalities like file I/O, networking, collections, and generics.
   - The modular nature of CoreFX allows developers to select only the libraries they need for their applications.

6. **Summary**:
   - The .NET Core architecture is explained as a robust, flexible, and optimized framework for modern application development, providing support for multiple programming languages and a modular approach to using libraries.

The session concludes with a brief goodbye, encouraging viewers to stay tuned for future discussions.

## Demo: Building a basic .NET Core console application

Here are the key notes from the text:

1. **Objective**: The session focuses on building a basic .NET Core console application using .NET CLI commands.

2. **Steps to Create a Console Application**:
   - Navigate to the desired repository where you want to generate the project.
   - Use the command `.net new list` to check available commands and options for creating a console application.
   - Use the short name `console` to create a console application with the command `.net new console`.
   - Specify the application name using `-n <name>` or `--name=<name>`.

3. **Project Location**:
   - The project will be generated in the current repository unless specified otherwise using the `-o` option to set an output folder.

4. **Building and Running the Application**:
   - Navigate into the project folder.
   - Use `.net build` to build the application, generating a build folder and checking for any warnings or errors.
   - Run the application using the command `.net run`, which will execute the program and print "Hello World."

5. **Using Visual Studio Code**:
   - You can open the project in Visual Studio Code by using the command `code .` to open the current repository.
   - The default file `Program.cs` contains the code that uses `Console.WriteLine` to print "Hello World."

6. **Conclusion**: The session provides a step-by-step guide to developing a simple console application in .NET Core, with a reminder to build and run the project using the appropriate commands.

These notes summarize the process of creating, building, and running a basic .NET Core console application using CLI commands.

### Example 

Sure! Here’s an example of creating a basic .NET Core console application using CLI commands:

### Steps and Example Commands

1. **Open Command Line Interface (CLI)**:
   Open your terminal or command prompt.

2. **Navigate to Desired Directory**:
   Change to the directory where you want to create your project.
   ```sh
   cd D:\Drive\snippet
   ```

3. **Check Available Templates**:
   List available templates to confirm the command for creating a console application.
   ```sh
   dotnet new list
   ```
   Look for the `console` template.

4. **Create a New Console Application**:
   Use the `.NET CLI` command to create a new console application.
   ```sh
   dotnet new console -n MyConsoleApp
   ```
   - `-n MyConsoleApp` specifies the name of the application. 

5. **Navigate to the Project Folder**:
   Change to the newly created project directory.
   ```sh
   cd MyConsoleApp
   ```

6. **Build the Project**:
   Compile the project and generate a build folder.
   ```sh
   dotnet build
   ```

7. **Run the Application**:
   Execute the application to see the output.
   ```sh
   dotnet run
   ```
   This will output:
   ```
   Hello, World!
   ```

8. **Open in Visual Studio Code (Optional)**:
   Open the project in Visual Studio Code.
   ```sh
   code .
   ```

### Example `Program.cs`

The `Program.cs` file should look like this by default:
```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, World!");
    }
}
```

This example demonstrates creating, building, and running a simple .NET Core console application from the command line.

## Read more about .Net Core Architecture

Here are the key points from the text "Introduction to .NET CLI":

1. **.NET CLI Overview**:
   - The .NET command-line interface (CLI) is a cross-platform toolchain used for developing, building, running, and publishing .NET applications.

2. **Installation**:
   - The .NET Core CLI comes with the .NET Core SDK.

3. **Command Structure**:
   - The general structure of a .NET CLI command is: `dotnet <command> <argument> <option>`.
   - The `dotnet` driver initiates command execution.
   - Commands (verbs) specify the action to be performed.
   - Commands can be followed by arguments and options.

4. **.NET Framework**:
   - It includes the Common Language Runtime (CLR), which is the execution engine for .NET Framework.
   - CLR provides services like memory management, type safety, exception handling, garbage collection, security, and thread management.

5. **Compilation and Execution**:
   - Programs for .NET Framework are compiled into Common Intermediate Language (CIL) code, not directly into machine code.
   - During execution, a just-in-time (JIT) compiler converts CIL code into machine code specific to the architecture.

Feel free to ask if you need more details on any of these points!