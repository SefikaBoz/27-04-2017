# 27-04-2017
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class Program
    {
        static void Main(string[] args)
        {
            //BoxingAndUnBoxing.Boxing();
            BoxingAndUnBoxing.Box();
            BoxingAndUnBoxing.Boxin();


            //short a = 257;
            //string b = a.ToString();
            //Console.WriteLine(b);

            //int i = 258;
            //byte by = (byte)i;
            //Console.WriteLine("bv   :" + by);


            //UseToIs.Is();
            //  UseToIs.As();


            // Checked.Check();
            //Checked.UnCheck();
            // Checked.Transform();
            int i = 1;
            object o = i;

            char c = '\u0044';
            Console.WriteLine(" C : " + c);

            Console.WriteLine(o);

            int j = (int)o;
            Console.WriteLine(j);

            ///////////////////////////////////
            //operator overloading

            Point p1 = new Point(10, 2);
            Point p2 = new Point(4, 5);
            Point p3 = p1 + p2;
            Console.WriteLine("P 3 : " + p3);           

            Console.WriteLine(" p1 / p2 : "  + p1 / p2);
            Console.WriteLine(" p1 % p2 : " + p1 % p2);

            Console.WriteLine("p1 & p2" + p1 * p2);

            ///////////////////////////////////
            // ControlStructure.BasicControl1();

            ///////////////////////////////////
            //  ControlStructure.BControlChooseCoffee();
            // ControlStructure.BasicControlWithCalculate();

            // ControlStructure.ForControlEx();

            //ControlStructure.GeneralTest();
            ControlStructure.CalculateMaxAndMin();
            Console.ReadKey();
        }
    }
}
