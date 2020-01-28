Write a program that shows the formatted retail price of shirts when there is a 15% markdown. Test the program by performing a compile- time initialization with an item labeled “Open Collar Running Shirt,” which has a wholesale price of $41.00. How much savings is expected with the markdown? Display appropriately labeled retail and mark- down values for the shirt. Once you get that running, go back into your source code, add lines of code that will reassign the memory location’s values for a Razorback T-Shirt, which has a retail price of $36.00. Add additional lines of code, which will display the new item’s information along with the previous item. What happens if the markdown goes to 20% or 10%?

```csharp
/* MarkDownApp.cs
 * This application computes the retail price of items 
 * when there is a 15% sale. The original price, sale
 * price and savings are displayed. 
 */

using System;
using static System.Console;

namespace MarkDownApp
{
    class MarkDownApp
    {
        static void Main( )
        {
            const double MARK_DOWN = 0.15;
            string itemName = "Open Collar Running Shirt";
            double retailPrice = 41.00,
                   newPrice,
                   savingsExpected;

            newPrice = retailPrice - (retailPrice * MARK_DOWN);
            savingsExpected = retailPrice - newPrice;

            WriteLine("{0,14}\n", "Markup App");
            WriteLine("Item: {0}", itemName);
            WriteLine("Retail Price: {0,11:c}", retailPrice);
            WriteLine("Sales Price: {0,12:c}", newPrice);
            WriteLine("Savings Expected: {0,7:c}", savingsExpected);

            //Second item....same code as above with new values
            itemName = "Razorback T-Shirt";
            retailPrice = 36.00;

            newPrice = retailPrice - (retailPrice * MARK_DOWN);
            savingsExpected = retailPrice - newPrice;

            WriteLine("{0,14}\n", "Markup App");
            WriteLine("Item: {0}", itemName);
            WriteLine("Retail Price: {0,11:c}", retailPrice);
            WriteLine("Sales Price: {0,12:c}", newPrice);
            WriteLine("Savings Expected: {0,7:c}", savingsExpected);
            ReadKey();
        }
    }
}
```
