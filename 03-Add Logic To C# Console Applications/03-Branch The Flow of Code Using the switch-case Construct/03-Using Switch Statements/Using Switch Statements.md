# Exercise - Complete a challenge activity using switch statements

**`9 minutes`**

Code challenges will reinforce what you've learned, and help you gain some confidence before continuing on.

### Convert to switch statements challenge

In this challenge, you'll rewrite an `if-elseif-else` construct as a `switch` statement. This challenge should help you see the strengths/weaknesses of the `switch` statement when compared to an `if-elseif-else` construct. Good luck.

### Code challenge: rewrite if-elseif-else using a switch statement

You'll start with code that uses an `if-elseif-else` construct to evaluate the components of a product SKU. The SKU (Stock Keeping Unit) is formatted using three coded values: `<product #>-<2-letter color code>-<size code>`. For example, a SKU value of `01-MN-L` corresponds to (sweat shirt)-(maroon)-(large), and the code outputs a description that appears as "Product: Large Maroon Sweat shirt".

Your challenge is to convert the `if` statement code to a `switch` statement that achieves the same result as the initial code.

1. Ensure that you have an empty Program.cs file open in Visual Studio Code.

     If necessary, open Visual Studio Code, and then complete the following steps to prepare a Program.cs file in the Editor:

     a. On the **File** menu, select **Open Folder**.

     b. Use the Open Folder dialog to navigate to, and then open, the CsharpProjects folder.

     c. In the Visual Studio Code EXPLORER panel, select **Program.cs**.

     d. On the Visual Studio Code Selection menu, select **Select All**, and then press the Delete key.

2. Enter the following code into the Visual Studio Code Editor:

     ```
     // SKU = Stock Keeping Unit. 
     // SKU value format: <product #>-<2-letter color code>-<size code>
     string sku = "01-MN-L";

     string[] product = sku.Split('-');

     string type = "";
     string color = "";
     string size = "";

     if (product[0] == "01")
     {
     type = "Sweat shirt";
     } else if (product[0] == "02")
     {
     type = "T-Shirt";
     } else if (product[0] == "03")
     {
     type = "Sweat pants";
     }
     else
     {
     type = "Other";
     }

     if (product[1] == "BL")
     {
     color = "Black";
     } else if (product[1] == "MN")
     {
     color = "Maroon";
     } else
     {
     color = "White";
     }

     if (product[2] == "S")
     {
     size = "Small";
     } else if (product[2] == "M")
     {
     size = "Medium";
     } else if (product[2] == "L")
     {
     size = "Large";
     } else
     {
     size = "One Size Fits All";
     }

     Console.WriteLine($"Product: {size} {color} {type}");
     ```

3. Update the code to use a `switch` statement in place of the `if-elseif-else` construct.

4. Verify that your output hasn't changed.

     No matter how you do it, your code should produce the following output:

     ```
     Product: Large Maroon Sweat shirt
     ```

Whether you get stuck and need to peek at the solution or you finish successfully, continue on to view a solution to this challenge.