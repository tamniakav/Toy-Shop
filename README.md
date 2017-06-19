using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_Two
{
    class Program
    {
        static void Main(string[] args)
        {
            double tripPrice = double.Parse(Console.ReadLine());
            int puzzle = int.Parse(Console.ReadLine());
            int doll = int.Parse(Console.ReadLine());
            int bears = int.Parse(Console.ReadLine());
            int minions = int.Parse(Console.ReadLine());
            int trucks = int.Parse(Console.ReadLine());

            double puzzlePrice = puzzle * 2.60;
            double dollPrice = doll * 3;
            double bearsPrice = bears * 4.10;
            double minionsPrice = minions * 8.20;
            double trucksPrice = trucks * 2;

            double total = puzzlePrice + dollPrice + bearsPrice + minionsPrice + trucksPrice;
            int toys = puzzle + doll + bears + minions + trucks;

            if (toys >= 50)
            {
                total = total * 0.75;
            }

            total = total * 0.90;

            double left = Math.Abs(total - tripPrice);
           
            Console.WriteLine(total >= tripPrice ? $"Yes! {left:f2} lv left." : $"Not enough money! {left:f2} lv needed.");
        }
    }
}
