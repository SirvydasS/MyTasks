# Task1============
using System;

namespace paysera
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            int[] x = new int[] {1, 3, 2, 6, 0, 3, 4, 2, 1, 3};
            int[] y = new int[] {5, 0, 2, 2, 4, 2, 3, 1, 5, 2};
            int points = 0;

            for(int i=0; i<; i++)
            {
                if(x[i]>y[i])
                {
                    points = points + 3;
                }
                else if(x[i] < y[i])
                {
                    points = points + 0;
                }
                else
                {
                    points = points + 1;
                }
            }
            Console.WriteLine("Points: " + points);
        }
    }
}

#Task2============
using System;

namespace paysera2
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            string[] array = new string[] { "XOOXO", "XOOXO", "OOOXO", "XXOXO", "OXOOO" };

            int per = 0;
            for (int i = 0; i < array.Length; i++)
            {
                for (int j = 0; j < array[i].Length; j++)
                {
                    if (array[i][j] == 'X')
                    {
                        if (j - 1 < 0 || array[i][j - 1] != 'X')
                        {
                            per++;
                        }
                        if (j + 1 >= array[i].Length || array[i][j + 1] != 'X')
                        {
                            per++;
                        }
                        if (i - 1 < 0 || array[i - 1][j] != 'X')
                        {
                            per++;
                        }
                        if (i + 1 >= array.Length || array[i + 1][j] != 'X')
                        {
                            per++;
                        }
                    }
                }
            }
            Console.WriteLine(per);
        }
    }
}
using System;

namespace paysera3
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            int n;
            Console.WriteLine("Iveskite metus: ");
            n = int.Parse(Console.ReadLine());
            Console.WriteLine(Cows(n));
        }
        public static int Cows(int years)
        {
            int y = years - 3;
            int cows = 1;
            for (int i = 0; i <= y; i++)
            {
                cows += Cows(y - i);
            }
            return cows;
        }

    }

}
#Task3============
