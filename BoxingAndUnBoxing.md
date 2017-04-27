# 27-04-2017

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class BoxingAndUnBoxing
    {
        public static void Boxing() {
            int i = 123;
            object o1 = i;
            //Console.WriteLine(o1);

            string str = "test";
            object o2 = (object)str;
            //Console.WriteLine(o2);

            byte b = 67;
            object o3 = (object)b;
            //Console.WriteLine(o3);

            //unboxig

            int j = (int)o1;
            string str2 = (string)o2;
            string str3 = o2.ToString();

            byte b1 = (byte)o3;
            //Console.WriteLine(j);
            //Console.WriteLine(str2);
            //Console.WriteLine(str3);

            int d = 456778;
            object obje = (object)d;
            Console.WriteLine(obje);
            Console.WriteLine(d.GetType());

            int k = (int)obje;
            Console.WriteLine(k);

            int z = 123;
            object p = z;
            z = 456;
            

            Console.WriteLine("z : " + z);
            Console.WriteLine("p : " + p);

        }     
        public static void Box()
        {
            string s = "Antalya";
            object obj = s;
            Console.WriteLine(obj);
            s = "İstanbul";
            Console.WriteLine(obj);
            Console.WriteLine(s);
        }
        public static void Boxin()
        {//calisir
            int x = 10;
            double y;
            object o = x;
            y = (int)o;
            Console.WriteLine(y);

        }
        public static void Boxi()
        {
            int x = 45;
            object o = x;
          //  x = o;

        }

    }
}
