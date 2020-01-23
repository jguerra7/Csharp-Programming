```csharp
/* Tempconversion app
 * This program converts degrees in Celsius to degrees in Fahrenheit.
 * It displays the original temperature and  the formatted
 * converted value.
 */
using System;
using static System.Console;

namespace Tempconversion
{
    class Program
    {
        static void Main()
        {
            double celsius = 32;
            double fahrenheit;

            fahrenheit = (9.0 / 5.0 * celsius) + 32.0;

            WriteLine("\tTemperature Conversion Console APP");
            WriteLine("\n Degrees Celsius: {0,8}", celsius);
            WriteLine("Degrees Fahrenheit:{0,7:f1}", fahrenheit);
            ReadKey();

        }
    }
}
```
