# Introduction to .NET Core and its features

Here are the important notes about the provided text discussing .NET Core:

1. **Introduction to .NET Core**:
   - .NET Core is an open-source, cross-platform framework that works on Windows, macOS, and Linux.
   - It is a subset of the larger .NET Framework, introduced by Microsoft in 2016 as a successor to the .NET Framework.

2. **Key Features**:
   - **Cross-Platform**: Allows developers to create applications that can be used on multiple platforms.
   - **High Performance**: Designed to be fast, flexible, lightweight, and modular, leading to modern application development.
   - **Cloud-Ready**: Optimized to work well in cloud environments.
   - **Modern Development Tools**: Supports modern tools and techniques, such as asynchronous programming and the use of editors like Visual Studio Code (VS Code).
   - **Open-Source**: .NET Core is fully open-source, providing transparency and flexibility to developers.
   - **Modular Architecture**: Facilitates the development of web applications with a modular design.
   - **Multilingual Support**: Supports multiple languages and frameworks, making it versatile for various development needs.
   - **CLI Tools**: Provides a consistent command-line interface (CLI) for development and deployment.

3. **Use Cases**:
   - Developers can build applications for Android, iOS, Linux, Mac, and Windows using .NET Core.
   - Particularly useful for building large enterprise-based web applications with frameworks like ASP.NET Core.

4. **Conclusion**:
   - The text concludes with enthusiasm for teaching more about .NET Core and its practical implementation in future videos.

This summary covers the essential aspects of .NET Core as described in the text.

## Setting up a development environment with VS code

Here are the key points from the text about setting up a development environment using Visual Studio and VS Code:

1. **Checking Dotnet Installation**:
   - Use the command `dotnet --version` to check if Dotnet SDK is installed and to view its version. If Dotnet is not recognized, it means it's not installed.

2. **Listing Dotnet Commands**:
   - Use `dotnet new list` to view available project templates and commands.

3. **Generating a Project**:
   - To create a new console application: `dotnet new console -n CoreConsoleProject`. It's recommended to avoid generating projects in the C drive; use a different drive like D. (Usar en una carpeta de proyectos)

4. **Opening and Running Projects in VS Code**:
   - Navigate to the project directory and open it with VS Code using the command `code .`.
   - To build the project: `dotnet build`. This generates a bin folder with build outputs.
   - To run the project: `dotnet run`.

5. **Setting Up in Visual Studio 2022**:
   - Create a new project by selecting a console application template compatible with .NET Core (e.g., .NET 6.0).
   - Visual Studio provides various features for development and deployment, such as dependencies and other folders.

6. **Running the Application**:
   - In Visual Studio 2022, you can run the application directly to see the output.

The text provides a basic overview of setting up a development environment, including generating and running console applications in both VS Code and Visual Studio 2022.

## Further reading on .Net Core

### Introduction to .NET Core and its features

.NET (pronounced as "dot net"; formerly named .NET Core) is a free and open-source, managed computer software framework for Windows, Linux, and macOS operating systems.

.NET fully supports C# and F# (and C++/CLI as of 3.1; only enabled on Windows) and supports Visual Basic .NET

Read more

### .NET Core Version History

NET Core 1.0 was released on June 27, 2016,[13] along with Microsoft Visual Studio 2015 Update 3, which enables .NET Core development.

.NET Core 2.0 was released on August 14, 2017, along with Visual Studio 2017 15.3, ASP.NET Core 2.0, and Entity Framework Core 2.0

To know more about version history, refer to the link given below.


### Difference Between .NET Framework and .NET Core

.NET is cross platform and runs on Linux, macOS, and Windows, whereas .NET framework runs only on Windows. .NET is open source and accepts contribution from community, whereas .NET framework source code is available but restrict direct contribution.


### Setting up a development environment with Visual Studio and/or VS Code

.NET
 provides a fast and modular platform for creating many different types of applications that run on Windows, Linux, and macOS. Use Visual Studio Code with the C# and F# extensions to get a powerful editing experience with C# IntelliSense

, F# IntelliSense (smart code completion), and debugging.

Read more
