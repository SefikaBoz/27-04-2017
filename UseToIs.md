# 27-04-2017

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class UseToIs
    {
        public static void Is()
        {
            string str = "June";
            object object1 = new object();
            object object2 = str;
            Console.WriteLine("object2" + object2 is string ? "is": "is not");


            //object value = true;
            //Person person = (Person)value;

            object value = true;
            Person person = null;
            Person p = new Person();
            if (value is Person)
            {
                person = (Person)value;
                Console.WriteLine(person);
            }
            else if(p is Person)
                Console.WriteLine("p is person ");

            else  
                Console.WriteLine("else ");
        }


        public static void As()
        {
            // yapılan cast hatalı ise null doner

            Person p = new Person {
                Name = "July",
                Surname = "Smith"



            };
            object obj = p as Person;
            if (obj != null)
            {
                Console.WriteLine("Successful");
            }
            else
                Console.WriteLine("Unsuccessful");

            Student std = obj as Student; 
            if(obj != null)
            {
                Console.WriteLine("Successful transform");
            }
            else
                Console.WriteLine("UnSuccessful transform");
        }
       
        public static void ToAs()
        {
            Person p = new Person();
            object o = (object)p;
            Person per = o as Person;

            int a = 50;

            object oo = a;
            int j = (int)oo;
            Console.WriteLine("j :   "+j);
        }
    }
}
