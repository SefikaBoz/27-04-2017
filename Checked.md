# 27-04-2017
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class Checked
    {
        public static void Check()
        {
            int intValue = 1258;
            byte byteValue;
            //Console.WriteLine("Byte değerini giriniz :");
            //intValue = Convert.ToByte(Console.ReadLine());

            checked
            {
                byteValue = (byte)intValue;
            }
            Console.WriteLine(byteValue);
        }

        public static void UnCheck()
        {
            int inVal = 258;
            int intA = 300;
            byte b, c;
            checked
            {
                b = (byte)intA;
                unchecked
                {
                    c = (byte)inVal;
                    Console.WriteLine(c);
                }
            }
        }

        public static void Transform()
        {
            char ch = 's';
            string str = ch.ToString();
            Console.WriteLine(str);
            Type t = typeof(Person);
            
            Console.WriteLine(t.ToString());
            Console.WriteLine(t.GetType());
            Console.WriteLine(ch.GetType());
        }
    }
}
