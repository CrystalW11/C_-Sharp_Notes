# Implement foreach Statement

**`12 minutes`**

Suppose you work for a manufacturing company. The company needs you to complete an inventory of your warehouse to determine the number of products that are ready to ship. In addition to the total number of finished products, you need to report the number of finished products stored in each individual bin in your warehouse, along with a running total. This running total will be used to create an audit trail so you can double-check your work and identify "shrinkage".

### Looping through an array using `foreach`

The `foreach` statement provides a simple, clean way to iterate through the elements of an array. The `foreach` statement processes array elements in increasing index order, starting with index 0 and ending with index Length - 1. It uses a temporary variable to hold the value of the array element associated with the current iteration. Each iteration will run the code block that's located below the `foreach` declaration.

Here's a simple example:

```
string[] names = { "Rowena", "Robin", "Bao" };
foreach (string name in names)
{
    Console.WriteLine(name);
}
```

Below the `foreach` keyword, the code block that contains the `Console.WriteLine(name);` will execute once for each element of the `names` array. As the .NET runtime loops through each element of the array, the value stored in the current element of the `names` array is assigned to the temporary variable `name` for easy access inside of the code block.

If you ran the code, you would see the following result.

```
Rowena
Robin
Bao
```

Use the `foreach` statement to create a sum of all the items on hand in each bin of your warehouse.