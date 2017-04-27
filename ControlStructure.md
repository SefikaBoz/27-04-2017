# 27-04-2017

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class ControlStructure
    {
        public static void BasicControl1()
        {
            string str = "chosen";

            switch (str)
            {
                case ("chosen"):
                    Console.WriteLine("choooseeee...:)");
                    break;

                case ("choose"):
                    Console.WriteLine(" a = 1");
                    break;
                case "choosed":
                    Console.WriteLine(" a = 1");
                    break;

                default:
                    Console.WriteLine(" Default operation..");
                    break;
            }
        }

        public static void BasicControlWithCalculate()
        {

            string operation;
            int num1, num2;

            Console.WriteLine("First num : ");
            num1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Second num : ");
            num2 = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Adding --> a");
            Console.WriteLine("Devide --> d");
            Console.WriteLine("Select to operation..");
            operation = Console.ReadLine();


            switch (operation)
            {
                case "a":
                    Console.WriteLine("Total : " + (num1 + num2));
                    break;

                case "d":

                    switch (num2)
                    {
                        case 0:
                            Console.WriteLine();
                            break;
                        default:
                            float result = (float)num1 / (float)num2;
                            Console.WriteLine("Total : " + result);
                            break;
                    }
                    break;

                default:
                    Console.WriteLine("İşlem seçmediniz..");
                    break;
            }

        }
        public static void BControlChooseCoffee()
        {
            Console.WriteLine("Choose coffee size.. \n 1 : small 2 : medium 3 :large");
            Console.WriteLine("");
            string str = Console.ReadLine();
            int totalbalance = 0;

            switch (str)
            {
                case "1":
                case "small":
                    totalbalance += 1;
                    Console.WriteLine("Total balance :" + totalbalance + "USD");
                    totalbalance = 1;
                    break;
                case "2":
                case "medium":
                    totalbalance += 2;
                    Console.WriteLine("Total balance :" + totalbalance + "USD");
                    break;
                case "3":
                case "large":
                    totalbalance += 3;
                    Console.WriteLine("Total balance :" + totalbalance + "USD");
                    break;

                default:
                    Console.WriteLine("Invalid selection..\nPlease select 1, 2 or 3 ");
                    break;
            }
        }
        public static void ForControlEx()
        {
            char ch;
            for (ch = Convert.ToChar(Console.ReadLine()); ch != 'q'; ch = Convert.ToChar(Console.ReadLine()))
            {
                Console.WriteLine(ch);

            }
           // int k = 0;
            //for (;;)
            //{
            //    Console.WriteLine("endless loop");
            //    k++;

            //}
        }
        public static void GeneralTest()
        {
            int count = 0;
            int total = 0;
            for (int i = 1; i <= 100; i++)
            {
                if ((i % 5 == 0) && (i % 7 != 0))
                {
                    total += i;
                    Console.WriteLine(".num = " + i + "bolunur." );
                    count++;
                }
            }
            Console.WriteLine("Total is : " + total);
            Console.WriteLine("Total number : " + count);
        }
        public static void CalculateMaxAndMin()
        {
            int num, max = 0, min = 100;
            Console.WriteLine("0 ile 100 arası 10 sayi girin..");
            for (int i = 0; i < 10; )
            {
                num = Convert.ToInt32(Console.ReadLine());
                if(num<0 || num>100)
                {
                    Console.WriteLine("Yanlis deger ! ");
                }
                else
                {
                    if (num > max)
                    {
                        max = num;
                    }
                    else if (num<min)
                    {
                        min = num;

                    }
                    i++;
                }
            }
            Console.WriteLine("En yuksek num :" + max);
            Console.WriteLine("En dusuk num :" + min);
        }
    }
}
