Write a program that prints the number of quarters, dimes, nickels, and pennies that a customer should get back as change. Declare and ini- tialize all memory locations as integers. On output, show the original change amount as a monetary amount, with two positions to the right of the decimal. Run your program once by performing a compile-time initialization using 92 cents for the value to be converted. Go into your source code and change the 92 to 27. Rerun the application. Be sure to desk check your solutions.


```csharp

using System;
using static System.Console;

namespace CalculateChangeCoins
{
    class CalculateChangeCoins
    {
        static void Main( )
        {
            const int AMOUNT_DUE = 92;
            int leftOverChange,
                quartersDue,
                dimesDue,
                nickelsDue,
                penniesDue;

            leftOverChange = AMOUNT_DUE;
            quartersDue = leftOverChange / 25;
            leftOverChange = leftOverChange % 25;
            dimesDue = leftOverChange / 10;
            leftOverChange = leftOverChange % 10;
            nickelsDue = leftOverChange / 5;
            penniesDue = leftOverChange % 5;

            WriteLine("\tChanger App");

            WriteLine("Change Amount: {0,4:f2}" +
                      "\n\nQuarters: {1,2:f0}" +
                      "\nDimes: {2,5:f0}\nNickels {3,4:f0}" +
                      "\nPennies: {4,3:f0}",
                      ((double)AMOUNT_DUE / 100), quartersDue, dimesDue,
                      nickelsDue, penniesDue);
            ReadKey();
        }
    }
}

```
