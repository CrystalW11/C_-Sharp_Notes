# Exercise - Complete a challenge activity to differentiate between do and while iteration statements

**`14 minutes`**

Code challenges will reinforce what you've learned and help you gain some confidence before continuing on.

### Examine the difference between do and while statement iterations

As you have seen, C# supports four types of iteration statements: `for`, `foreach`, `do-while`, and `while`. Microsoft's language reference documentation describes these statements as follows:


- The `for` statement: executes its body while a specified Boolean expression (the 'condition') evaluates to true.

- The `foreach` statement: enumerates the elements of a collection and executes its body for each element of the collection.

- The `do-while` statement: conditionally executes its body one or more times.

- The `while` statement: conditionally executes its body zero or more times.

The `for` and `foreach` iterations seem to be clearly differentiated from each other and from the `do-while` and `while` iterations. The definitions for the `do-while` and `while` statements, however, appear to be quite similar. Knowing when to choose between a `do-while` and a `while` seems more arbitrary, and can even be a bit confusing. Some challenge projects may help to make the differences clear.

In this challenge, you'll be presented with conditions for three separate coding projects. Each project will require you to implement an iteration code block using either a `do-while` or a `while` statement. You'll need to evaluate the specified conditions in order to choose between the `do-while` and `while` statements. You can switch after you start if your first choice isn't working out as well as you had hoped.

    ❗**Note

    The conditions for your coding project can be used to help you select between the `do-while` and `while` statements. What you know, or don't know, about the Boolean expression that will be evaluated can sometimes help you to select between the `do-while` and `while` statements. In this challenge exercise, the project conditions include information that will be used to construct the Boolean expression.

### Manage user input during this challenge

When using a `Console.ReadLine()` statement to obtain user input, it's common practice to use a nullable type string (designated `string`?) for the input variable and then evaluate the value entered by the user. The following code sample uses a nullable type string to capture user input. The iteration continues while the user-supplied value is null:

```
string? readResult;
Console.WriteLine("Enter a string:");
do
{
    readResult = Console.ReadLine();
} while (readResult == null);
```

The Boolean expression evaluated by the while statement can be used to ensure user input meets a specified requirement. For example, if a prompt asks the user to enter a string that includes at least three characters, the following code could be used:

```
string? readResult;
bool validEntry = false;
Console.WriteLine("Enter a string containing at least three characters:");
do
{
    readResult = Console.ReadLine();
    if (readResult != null)
    {
        if (readResult.Length >= 3)
        {
            validEntry = true;
        }
        else
        {
            Console.WriteLine("Your input is invalid, please try again.");
        }
    }
} while (validEntry == false);
```

If you want to use `Console.ReadLine()` input for numeric values, you need to convert the string value to a numeric type.

The `int.TryParse()` method can be used to convert a string value to an integer. The method uses two parameters, a string that will be evaluated and the name of an integer variable that will be assigned a value. The method returns a Boolean value. The following code sample demonstrates using the `int.TryParse()` method:

```
// capture user input in a string variable named readResult

int numericValue = 0;
bool validNumber = false;

validNumber = int.TryParse(readResult, out numericValue);
```

If the string value assigned to `readResult`represents a valid integer, the value will be assigned to the integer variable named `numericValue`, and `true` will be assigned to the Boolean variable named `validNumber`. If the value assigned to `readResult` doesn't represent a valid integer, `validNumber` will be assigned a value of `false`. For example, if `readResult` is equal to "7", the value `7` will be assigned to `numericValue`.

### Code project 1 - write code that validates integer input

