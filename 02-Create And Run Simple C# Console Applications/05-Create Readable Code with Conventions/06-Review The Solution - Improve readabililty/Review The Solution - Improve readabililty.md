# Review the solution to the improve code readability challenge activity

**`4 minutes`**

The following code is one possible solution for the challenge from the previous unit.

     ```
     /*
     This code reverses a message, counts the number of times 
     a particular character appears, then prints the results
     to the console window.
     */

     string originalMessage = "The quick brown fox jumps over the lazy dog.";

     char[] message = originalMessage.ToCharArray();
     Array.Reverse(message);

     int letterCount = 0;

     foreach (char letter in message)
     {
     if (letter == 'o')
     {
          letterCount++;
     }
     }

     string newMessage = new String(message);

     Console.WriteLine(newMessage);
     Console.WriteLine($"'o' appears {letterCount} times.");
     ```

If you identified the same issues and addressed them in a similar way, congratulations! Continue on to the knowledge check in the next unit.

❗**Important**

If you had trouble completing this challenge, maybe you should review the previous units before you continue on.