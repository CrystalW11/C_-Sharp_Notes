# Exercise - Implement a switch statement

**`11 minutes`**

A `switch` statement is a C# selection statement that provides an alternative to an `if-elseif-else` branching construct. The switch statement provides advantages over an `if-elseif-else` construct when evaluating a single value against a list of known matching values.

Consider the following scenario:


- You're working on an application related to food nutrition. A section of the code deals with fruits.

- Your code includes a variable named `fruit` that's used to hold the name of different types of fruit.

- You have a list of the 20 fruits that your application is focused on.

- You want to branch your code based on the value assigned to `fruit`.

In this scenario, you can use a `switch` statement to create a separate branch for each type of fruit.

### How does a switch statement work?

The `switch` statement chooses one section of code to execute from a list of possible ***switch sections***. The selected switch section is chosen based on a pattern match with the statement's match expression.

Consider the following code sample that shows the basic structure of `switch` statement:

```
switch (fruit)
{
    case "apple":
        Console.WriteLine($"App will display information for apple.");
        break;

    case "banana":
        Console.WriteLine($"App will display information for banana.");
        break;

    case "cherry":
        Console.WriteLine($"App will display information for cherry.");
        break;
}
```

The match expression (which may also be referred to as the switch expression) is the value following the `switch` keyword, in this case `(fruit)`. Each switch section is defined by a case pattern. Case patterns are constructed using the keyword `case` followed by a value. The first case pattern in this example is: `case "apple":`. Case patterns are Boolean expressions that evaluate to either `true` or `false`. Each switch section includes a small number of code lines that will be executed if the case pattern is a match for the match expression. In this example, if `fruit` is assigned a value of "apple", the first case pattern will evaluate as `true` and that switch section will be executed.

A switch statement must include at least one switch section, but will normally contain three or more switch sections.

The switch is best used when:


- You have a single value (variable or expression) that you want to match against many possible values.

- For any given match, you need to execute a couple of lines of code at most.

❗**Note**

This first example of a `switch` statement is purposefully simple and your examination of the syntax was brief. You will be examining additional features of the `switch` statement when you work through some more advanced scenarios in the sections below.

It's time to prepare your coding environment and begin developing your own `switch` statements.

### Prepare your coding environment