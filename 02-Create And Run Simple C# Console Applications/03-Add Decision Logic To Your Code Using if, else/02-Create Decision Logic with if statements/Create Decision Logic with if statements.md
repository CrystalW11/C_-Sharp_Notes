# Create Decision Logic with if statements

**`19 minutes`**

Most applications include a large number of execution paths. For example, an application could implement different execution paths based on which menu option a user selects. Developers refer to the code that implements different execution paths as ***code branches***.

The most widely used code branching statement is the if statement. The if statement relies on a Boolean expression that is enclosed in a set of parentheses. If the expression is true, the code after the if statement is executed. If not, the .NET runtime ignores the code and doesn't execute it.

In this exercise, you'll practice writing if statements by creating a game. First you'll define the rules of the game, then you'll implement them in code.

You'll use the Random.Next() method to simulate rolling three six-sided dice. You'll evaluate the rolled values to calculate the score. If the score is greater than an arbitrary total, then you'll display a winning message to the user. If the score is below the cutoff, you'll display a losing message to the user.