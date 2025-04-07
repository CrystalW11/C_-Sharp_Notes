# Review the solution to the conditional operator challenge activity

**`3 minutes`**

The following code is one possible solution for the challenge from the previous unit.

```
Random coin = new Random();
int flip = coin.Next(0, 2);
Console.WriteLine((flip == 0) ? "heads" : "tails");
```

This code is merely ***"one possible solution."*** You could have eliminated the temporary variable `flip` by calling the `Next()` inside of the Boolean expression like so:

```
Random coin = new Random();
Console.WriteLine((coin.Next(0, 2) == 0) ? "heads" : "tails");
```

However, this code is packed densely and it might be more difficult to understand what the code is doing.

If you were successful, congratulations! Continue on to the second challenge in the next unit.

❗**Important**

If you had trouble completing this challenge, maybe you should review the previous units before you continue on.

