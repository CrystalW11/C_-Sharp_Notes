# Exercise - Create and configure for iteration loops

**`14 minutes`**

On the surface, the for statement is another iteration statement that allows you to iterate through a code block and thereby change the flow of execution of your code. However, once we examine how each works, we can better identify the nuances of each iteration statement and when to use them.

### What is the `for` statement?

The `for` statement iterates through a code block a specific number of times. This level of control makes the `for` statement unique among the other iteration statements. The `foreach` statement iterates through a block of code once for each item in a sequence of data like an array or collection. The `while` statement iterates through a block of code until a condition is met.

Furthermore, the `for` statement gives you much more control over the process of iteration by exposing the conditions for iteration.

In this exercise, you'll use the `for` statement, learning how to control the iteration's pre-condition, completion condition, its iteration pattern and more. Also, you'll learn of common use cases for the for statement.

Okay, now let's prepare our coding environment and begin our examination of code samples that implement a `for` statement.

### Prepare your coding environment

This module includes hands-on activities that guide you through the process of building and running demonstration code. We encourage you to complete these activities using Visual Studio Code as your development environment. Using Visual Studio Code for these activities will help you to become more comfortable writing and running code in a developer environment that's used by professionals worldwide.

1. Open Visual Studio Code.

     You can use the Windows Start menu (or equivalent resource for another OS) to open Visual Studio Code.

2. On the Visual Studio Code **File** menu, select **Open Folder**.

3. In the **Open Folder** dialog, navigate to the Windows Desktop folder.

     If you have different folder location where you keep code projects, you can use that folder location instead. For this training, the important thing is to have a location that’s easy locate and remember.

4. In the **Open Folder** dialog, select **Select Folder**.

     If you see a security dialog asking if you trust the authors, select **Yes**.

5. On the Visual Studio Code **Terminal** menu, select **New Terminal**.

     Notice that a command prompt in the Terminal panel displays the folder path for the current folder. For example:

     ```
     C:\Users\someuser\Desktop>
     ```

     ❗**Note**

     If you are working on your own PC rather than in a sandbox or hosted environment and you have completed other Microsoft Learn modules in this C# series, you may have already created a project folder for code samples. If that's the case, you can skip over the next step, which is used to create a console app in the TestProject folder.

6. At the Terminal command prompt, to create a new console application in a specified folder, type **`dotnet new console -o ./CsharpProjects/TestProject`** and then press Enter.

     This .NET CLI command uses a .NET program template to create a new C# console application project in the specified folder location. The command creates the **CsharpProjects** and TestProject folders for us, and uses TestProject as the name of our `.csproj` file.

7. In the EXPLORER panel, expand the CsharpProjects folder.

     You should see the TestProject folder and two files, a C# program file named Program.cs and a C# project file named TestProject.csproj.

8. In the EXPLORER panel, to view your code file in the Editor panel, select **Program.cs**.

9. Delete the existing code lines.

     You'll be using this C# console project to create, build, and run code samples during this module.

10. Close the Terminal panel.

### Write a basic for statement

1. Ensure that you have Visual Studio Code open and Program.cs displayed in the Editor panel.

     ❗**Note**

     **Program.cs** should be empty. If if isn't, select and delete all code lines.

2. Type the following code into the Visual Studio Code Editor.

     ```
     for (int i = 0; i < 10; i++)
     {
     Console.WriteLine(i);
     }
     ```

     This code presents a simple `for` statement that loops through its code block 10 times, printing the current value of `i`.

3. On the Visual Studio Code **File** menu, select **Save**.

     The Program.cs file must be saved before building or running the code.

4. In the EXPLORER panel, to open a Terminal at your TestProject folder location, right-click **TestProject**, and then select **Open in Integrated Terminal**.

     A Terminal panel will open. The Terminal should include a command prompt showing that the Terminal is open to your TestProject folder location.

5. At the Terminal command prompt, to run your code, type **dotnet run** and then press Enter.

     ❗**Note**

     If you see a message saying "Couldn't find a project to run", ensure that the Terminal command prompt displays the expected TestProject folder location. For example: **`C:\Users\someuser\Desktop\csharpprojects\TestProject>`**

     You should see the following output.

     ```
     0
     1
     2
     3
     4
     5
     6
     7
     8
     9
     ```

6. Take a minute to identify the six parts of the `for` statement.

     The for statement includes the following six parts:

     The `for` keyword.

     a. A set of parentheses that defines the conditions of for iteration. The parentheses contain three distinct parts, separated by the end of statement operator, a semi-colon.
     
     b. The first part defines and initializes the iterator variable. In this example: `int i = 0`. This section is referred to as the initializer.
     
     c. The second part defines the completion condition. In this example:`i < 10`. In other words, the runtime will continue to iterate over the code in the code block below the `for` statement while `i` is less than `10`. 
     
     d. When i becomes equal to 10, the runtime stops executing the for statement's code block. The docs refer to this section as the **condition**.
     
     e. The third part defines the action to take after each iteration. In this case, after each iteration, `i++` will increment the value of `i` by 1. The docs refer to this section as the iterator.
     
     f. Finally, the code block. The code block contains the code that will be executed for each iteration. Notice that the value of `i` is referenced inside of the code block. The docs refer to this section as the **body**.

Given our rules for naming variables, you may wonder if `i` is a valid name for the variable that holds the current iteration. In this case, `i` is considered by most to be valid. Other popular choices are x and counter. The name j is also used in those situations when you have an outer `for` statement that uses `i`, and need to create an iteration variable for an inner for statement.