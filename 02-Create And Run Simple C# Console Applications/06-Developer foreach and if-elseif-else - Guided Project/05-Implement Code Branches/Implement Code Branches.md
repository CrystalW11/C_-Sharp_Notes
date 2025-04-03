# Exercise - Implement code branches using selection statements

**`25 minutes`**

In this exercise, you'll develop the code that automatically assigns a student's letter grade based on their final numeric score and you'll update the application so that extra credit project scores are factored into the student's final grade. You will begin by writing an `if-elseif-else` construct that can be used to evaluate the student's numeric score and assign the letter grade. Next, you'll examine the application requirements related to extra credit work, and then work your way through the required code updates. The detailed tasks that you'll complete during this exercise are:

1. Develop an `if-elseif-else` construct that evaluates the student's score to assign a letter grade. The expression that's evaluated compares the student's numeric score with a range of scores taken from a grading chart provided by the teacher.

2. Integrate extra credit scores into each student's scores array, and then update the code that's used to calculate the student's numeric score. The `foreach` that's used to sum the student scores will be updated to include an `if` statement that branches the code. The exam scores will be applied to the sum in one branch, and the extra credit scores in the other branch.

❗**Important**

You need to have completed this module's previous Exercise, "Create arrays and foreach loops", before you begin this Exercise.

### Assign letter grades using an if-elseif-else construct

In this task, you'll develop an `if-elseif-else` structure that can be used to assign letter grades based on a calculated numeric score.

1. Ensure that you have the **Program.cs** file open in the Visual Studio Code Editor.

2. Create a blank code line below the line used to declare `studentScores` array.

3. To create a string variable that can be used to hold the student's letter grade, enter the following code:

     ```
     string currentStudentLetterGrade = "";
     ```

4. Scroll down to the bottom of the **Program.cs** file.

5. Add a blank code line below the line that assigns a calculated value to `currentStudentGrade`.

6. Take a minute to consider the grading chart that shows the letter grade corresponding to numeric scores.

     ```
     97 - 100   A+
     93 - 96    A
     90 - 92    A-
     87 - 89    B+
     83 - 86    B
     80 - 82    B-
     77 - 79    C+
     73 - 76    C
     70 - 72    C-
     67 - 69    D+
     63 - 66    D
     60 - 62    D-
     0  - 59    F
     ```

     Notice that the top row of scores, the values greater than or equal to 97, have a letter grade of "A+". In other words, if a student's final score is >= 97, they'll be assigned a letter grade of "A+".

7. To create an `if` statement that assigns `A+` to `currentStudentLetterGrade` when the student's score is greater than or equal to 97, enter the following code:

8. To create an `else if` statement that assigns `A` to `currentStudentLetterGrade` when the student's score is greater than or equal to 93, enter the following code:

     ```
     else if (currentStudentGrade >= 93)
     currentStudentLetterGrade = "A";
     ```

     The `else if` will not assign `A` to `currentStudentLetterGrade` when the student's score is greater than or equal to 97 because that expression returned true in the preceding if.

     You can extend this `else if` pattern as you move down the rows of the letter grade chart. When you reach the end of the chart, you can use a final `else` to catch any currentStudentGrade that is below 60.

9. Create the `else if` statements that assign letter grades to `currentStudentLetterGrade` for the score ranges between 60 and 92.

     Once you've completed this step, you should have an if statement structure that matches the following code:

     ```
     if (currentStudentGrade >= 97)
          currentStudentLetterGrade = "A+";

     else if (currentStudentGrade >= 93)
          currentStudentLetterGrade = "A";

     else if (currentStudentGrade >= 90)
          currentStudentLetterGrade = "A-";

     else if (currentStudentGrade >= 87)
          currentStudentLetterGrade = "B+";

     else if (currentStudentGrade >= 83)
          currentStudentLetterGrade = "B";

     else if (currentStudentGrade >= 80)
          currentStudentLetterGrade = "B-";

     else if (currentStudentGrade >= 77)
          currentStudentLetterGrade = "C+";

     else if (currentStudentGrade >= 73)
          currentStudentLetterGrade = "C";

     else if (currentStudentGrade >= 70)
          currentStudentLetterGrade = "C-";

     else if (currentStudentGrade >= 67)
          currentStudentLetterGrade = "D+";

     else if (currentStudentGrade >= 63)
          currentStudentLetterGrade = "D";

     else if (currentStudentGrade >= 60)
          currentStudentLetterGrade = "D-";
     ```

     Your final step is to add the `else` that addresses any remaining scores.

10. To create the else that applies to scores below 60, enter the following code:

     ```
     else
          currentStudentLetterGrade = "F";
     ```

11. Take a minute to review your application code.

     Your **Program.cs** code should match the following code:

     ```
     // initialize variables - graded assignments
     int currentAssignments = 5;

     int[] sophiaScores = new int[] { 90, 86, 87, 98, 100 };
     int[] andrewScores = new int[] { 92, 89, 81, 96, 90 };
     int[] emmaScores = new int[] { 90, 85, 87, 98, 68 };
     int[] loganScores = new int[] { 90, 95, 87, 88, 96 };

     // Student names
     string[] studentNames = new string[] { "Sophia", "Andrew", "Emma", "Logan" };

     int[] studentScores = new int[10];

     string currentStudentLetterGrade = "";

     // Display the Report Header
     Console.WriteLine("Student\t\tGrade\n");

     foreach (string name in studentNames)
     {
     string currentStudent = name;

     if (currentStudent == "Sophia")
          // assign Sophia's scores to the studentScores array 
          studentScores = sophiaScores;

     else if (currentStudent == "Andrew")
          // assign Andrew's scores to the studentScores array 
          studentScores = andrewScores;

     else if (currentStudent == "Emma")
          // assign Emma's scores to the studentScores array 
          studentScores = emmaScores;

     else if (currentStudent == "Logan")
          // assign Logan's scores to the studentScores array 
          studentScores = loganScores;

     // initialize/reset the sum of scored assignments
     int sumAssignmentScores = 0;

     // initialize/reset the calculated average of exam + extra credit scores
     decimal currentStudentGrade = 0;

     foreach (int score in studentScores)
     {
          // add the exam score to the sum
          sumAssignmentScores += score;
     }

     currentStudentGrade = (decimal)(sumAssignmentScores) / currentAssignments;

     if (currentStudentGrade >= 97)
          currentStudentLetterGrade = "A+";

     else if (currentStudentGrade >= 93)
          currentStudentLetterGrade = "A";

     else if (currentStudentGrade >= 90)
          currentStudentLetterGrade = "A-";

     else if (currentStudentGrade >= 87)
          currentStudentLetterGrade = "B+";

     else if (currentStudentGrade >= 83)
          currentStudentLetterGrade = "B";

     else if (currentStudentGrade >= 80)
          currentStudentLetterGrade = "B-";

     else if (currentStudentGrade >= 77)
          currentStudentLetterGrade = "C+";

     else if (currentStudentGrade >= 73)
          currentStudentLetterGrade = "C";

     else if (currentStudentGrade >= 70)
          currentStudentLetterGrade = "C-";

     else if (currentStudentGrade >= 67)
          currentStudentLetterGrade = "D+";

     else if (currentStudentGrade >= 63)
          currentStudentLetterGrade = "D";

     else if (currentStudentGrade >= 60)
          currentStudentLetterGrade = "D-";

     else
          currentStudentLetterGrade = "F";

     Console.WriteLine($"{name}\t\t{currentStudentGrade}\t?");
     }

     Console.WriteLine("Press the Enter key to continue");
     Console.ReadLine();
     ```

     Notice that your application is organized in a very logical top-to-bottom manner:

     a. You initialize variables and create the arrays that serve as the data source for the application. You have arrays that supply student scores as well as an array that supplies the student names. You also have a student-agnostic array named `studentScores` that you can use to hold the scores of any student when it comes time to calculate the grades.

     b. You have a `Console.WriteLine()` statement that writes the column labels for your grading report to the console.

     c. You have an outer `foreach` loop that iterates through the `studentNames` array, providing you with a code block that repeats for each student.

     d. You continue to organize your code using a top-to-bottom approach inside the code block of the outer foreach loop:

     - **i**. You have an `if` statement to evaluate the name of the current student, for example `if (currentStudent == "Sophia")`. When the expression evaluates as true, you assign the student's scores array to your student-agnostic array, for example: studentScores = sophiaScores;
     
     - **ii**. You declare the two variables that're required in order to calculate student grades. The first variable, sumAssignmentScores, is used to calculate the sum of assignment scores. The second variable, currentStudentGrade, is used to calculate final numeric grade. You initialize the variables with a value of 0.
     
     - **iii**. You have a foreach loop that iterates through studentScores to calculate the value of sumAssignmentScores.

     - **iv**. You calculate currentStudentGrade by dividing sumAssignmentScores by the number of assignments in the grade book. The number of graded assignments is held in a variable named currentAssignments.

     - **v**. You have an if-elseif-else construct that assigns letter grades based on the value of currentStudentGrade.

     - **vi**. You have a Console.WriteLine() statement that writes student names and grades to the console in order to complete the grading report.

12. Locate the `Console.WriteLine()` statement that writes student names and grades to the console.