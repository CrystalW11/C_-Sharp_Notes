# Create effective Code Comments

**`13 minutes`**

In this exercise, you'll add notes to your code and temporarily disable certain lines of code from compilation. Then you'll look at how the C# compiler understands whitespace and how to use whitespace to increase the readability of your code.

### What is a code comment?

A **code comment** is an instruction to the compiler to ignore everything after the code comment symbols in the current line.

```
// This is a code comment!
```

This may not seem useful at first, however it's useful in three situations:


- When you want to leave a note about the intent of a passage of code. It can be helpful to include code comments that describe the purpose or the thought process when you're writing a particularly challenging set of coding instructions. Your future self will thank you.

- When you want to temporarily remove code from your application to try a different approach, but you're not yet convinced your new idea will work. You can comment out the code, write the new code, and once you're convinced the new code will work the way you want it to, you can safely delete the old (commented code).

- Adding a message like TODO to remind you to look at a given passage of code later. While you should use this judiciously, it's a useful approach. You may be working on another feature when you read a line of code that sparks a concern. Rather than ignoring the new concern, you can mark it for investigation later.

❗**Note**

Code comments should be used to say what the code cannot. Often, developers update their code but forget to update the code comments. It's best to use comments for higher-level ideas and not to add comments about how an individual line of code works.

### Prepare your coding environment

This module includes exercises that guide you through the process of building and running sample code. You are encouraged to complete these activities using Visual Studio Code as your development environment. Using Visual Studio Code for these activities will help you to become more comfortable writing and running code in a developer environment that's used by professionals worldwide.


1. Open Visual Studio Code.

     You can use the Windows Start menu (or equivalent resource for another OS) to open Visual Studio Code.

2. On the Visual Studio Code **File** menu, select **Open Folder**.

3. In the **Open Folder** dialog, navigate to the Windows Desktop folder.

     If you have a different folder location where you keep code projects, you can use that folder location instead. For this training, the important thing is to have a location that’s easy to locate and remember.

4. In the **Open Folder** dialog, select **Select Folder**.

     If you see a security dialog asking if you trust the authors, select **Yes**.

5. On the Visual Studio Code **Terminal** menu, select **New Terminal**.

     Notice that a command prompt in the Terminal panel displays the folder path for the current folder. For example:
     
     ```
     C:\Users\someuser\Desktop>
     ```

❗ **Note**

If you are working on your own PC rather than in a sandbox or hosted environment and you have completed other Microsoft Learn modules in this C# series, you may have already created a project folder for code samples. If that's the case, you can skip over the next step, which is used to create a console app in the `TestProject` folder.

6. At the Terminal command prompt, to create a new console application in a specified folder, type `dotnet new console -o ./CsharpProjects/TestProject` and then press Enter.

     This .NET CLI command uses a .NET program template to create a new C# console application project in the specified folder location. The command creates the CsharpProjects and `TestProject` folders for you, and uses `TestProject` as the name of your `.csproj` file.

7. In the EXPLORER panel, expand the **CsharpProjects** folder.

     You should see the TestProject folder and two files, a C# program file named Program.cs and a C# project file named `TestProject.csproj`.

8. In the EXPLORER panel, to view your code file in the Editor panel, select **Program.cs**.

9. Delete the existing code lines.

     You'll be using this C# console project to create, build, and run code samples during this module.

10. Close the Terminal panel.