# 27-04-2017
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Demo3
{
    class Point
    {
        public int X { get; set; }
        public int Y { get; set; }
        public string A { get; set; }
        public string B { get; set; }


        public Point(int x, int y)
        {
            X = x;
            Y = y;
        }
       
        public static Point operator +(Point p1, Point p2)
        {
            return new Point(p1.X + p2.X, p1.Y + p2.Y);
        }

        public static Point operator /(Point p1, Point p2)
        {
            return new Point(p1.X / p2.X, p1.Y / p2.Y);
        }
        public static Point operator %( Point p1, Point p2)
        {
            return new Point(p1.X - p2.X , p1.Y + p2.Y);
        }
        public static Point operator * (Point p1,Point p2)
        {
            return new Point(p1.X * p2.Y , p2.X / p2.Y);
        }
        
        
    }
}
