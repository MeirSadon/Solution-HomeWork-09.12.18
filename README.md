using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HomeWork_09._12
{
    class Program
    {
        static void Main(string[] args)
        {
            ////=============================Question 1.
            //int x = 12; int y = 5;
            //bool result = ItsWitModule(x, y); Console.Write(result ? "No Module" : "With Module");

            ////=============================Question 2.
            //int x = 5;
            //int y = 3;
            //AddAndMultiply(ref x, ref y);
            //Console.WriteLine($"x is {x} and y is {y}");

            ////=============================Question 3.
            //int x;
            //int y;
            //Declare(out x, out y);
            //Console.WriteLine($"x is {x} and y is {y}");

            ////=============================Question 4.
            //int result = (Power(2,4,6,8));
            //Console.WriteLine(result);

            ////=============================Question 5.
            //int result = MultiplyWithDefaultValue(5,3);
            //Console.Write(result);

            ////=============================Question 6.
            //int result = MultiplyWithDefaultValue(y:5,z:3);
            //Console.Write(result);

            ////=============================Question 7.
            //int[] arr = new int[] { 3, -1, 5, 8, -5, -10, -20,4,-22,55,-113,123 };
            //PosAndNig(arr);

            Console.ReadKey();

        }
        private static bool ItsWitModule(int x, int y)
        {
            if (x % y == 0)
                return true;
            else
                return false;
        }
        private static void AddAndMultiply(ref int a,ref  int b)
        {
            a += 1;
            b *= 2;
        }
        private static void Declare(out int x, out int y)
        {
            x = 5;
            y = 10;
        }
        private static int Power(params int[] numbers)
        {
            int sum = numbers[1];
            for (int i = 0; i < numbers.Length; i++)
            {
                sum = sum * numbers[i];
            }
            return sum;
        }
        private static int MultiplyWithDefaultValue(int x = 3, int y = 1, int z = 2)
        {
            int result = x * y * z;
            return result;
        }
        private static void PosAndNig(int[] arr)
        {
            int lengthOfPositive = 0;
            int lengthOfnegative = 0;
            for (int i = 0; i < arr.Length; i++)
            {
                if (arr[i] < 0)
                    lengthOfnegative += 1;
                else
                    lengthOfPositive += 1;
            }
            int[] positiveArray = new int[lengthOfPositive];
            int[] negativeArray = new int[lengthOfnegative];
            int positionPositive = 0;
            int positionNegative = 0;
            for (int i = 0; i < arr.Length; i++)
            {
                if (arr[i] < 0)
                {
                    negativeArray[positionNegative] = arr[i];
                    positionNegative++;
                }
                if (arr[i] > 0)
                {
                    positiveArray[positionPositive] = arr[i];
                    positionPositive++;
                }
                        
            }
            for (int i = 0; i < positiveArray.Length; i++)
            {
                Console.Write($"{positiveArray[i]},");
            }
            Console.WriteLine();
            for (int i = 0; i < negativeArray.Length; i++)
            {
                Console.Write($"{negativeArray[i]},");
            }
        }
    }
}
