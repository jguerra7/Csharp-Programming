## Example 1

Write a program that computes the average of five exam scores. 
  Declare and perform a compile-time initialization with the five exam values. 
  Declare integer memory locations for the exam values. Use an integer constant to define the number of scores.
  Print all scores. The average value should be formatted with two digits to the right of the decimal. 
  Rerun the application with different values. Be sure to desk check your results.

```csharp
/* GradingApp.cs 
 * This program computes and displays the average of a 
 * set of test scores. 
 */

using System;
using static System.Console;

namespace GradingApp
{
    class GradingApp
    {
        static void Main( )
        {
            const int NUMBER_SCORES = 5;

            int scoreOne = 77,
                scoreTwo = 93,
                scoreThree = 82,
                scoreFour = 98,
                scoreFive = 74,
                sumOfScores = 0;
            double average;


            sumOfScores = scoreOne + scoreTwo + scoreThree + scoreFour + scoreFive;
            average = (double)sumOfScores / NUMBER_SCORES;

            WriteLine("  Grading App\n");
            WriteLine("Score #1:{0,4:f0}\n" +
                      "Score #2:{1,4:f0}\n" +
                      "Score #3:{2,4:f0}\n" +
                      "Score #4:{3,4:f0}\n" +
                      "Score #5:{4,4:f0}\n",
                      scoreOne, scoreTwo, scoreThree, scoreFour, scoreFive);
            WriteLine("\nAverage: {0,7:f2}", average);
            ReadKey();
        }
    }
}
```
