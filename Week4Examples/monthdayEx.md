```csharp
using System;
using static System.Console;
class CheckMonth2
{
   static void Main()
   {
      int month;
      int day;
      bool isMonthOK = false;
      bool isDayOK = false;
      Write("Enter birth month >> ");
      month = Convert.ToInt32(ReadLine());
      Write("Enter birth day >> ");
      day = Convert.ToInt32(Console.ReadLine());
      switch(month)
      {
         case 1:
         case 3:
         case 5:
         case 7:
         case 8:
         case 10:
         case 12:
         {
             if(day >= 1 && day <= 31)
             {
                isMonthOK = true;
                isDayOK = true;
             }
             else
                isDayOK = false;
             break;
         }
         case 4:
         case 6:
         case 9:
         case 11:
         {
             if(day >= 1 && day <= 30)
             {
                isMonthOK = true;
                isDayOK = true;
             }
             else
                isDayOK = false;
             break;
         }
         case 2:
         {
             if(day >= 1 && day < 29)
             {
                isMonthOK = true;
                isDayOK = true;
             }
             else
                isDayOK = false;
             break;
         }
         default:
         {
            isMonthOK = false;
            break;
         }
       }
       if(isMonthOK && isDayOK)
            WriteLine("{0}/{1} is a valid birthday", month, day);
         else
            WriteLine("Invalid date");
    }
}


```
