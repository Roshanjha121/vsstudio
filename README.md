# vsstudio

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int temp = 0;

            Console.WriteLine("Enter the number");
            string values = Console.ReadLine();
            int[] numbers = new int[values.Length];
            
            for(int i=0;i<numbers.Length;i++)
            {
                numbers[i] = int.Parse(values.Substring(i, 1));
            }


            for (int i = 0; i < numbers.Length; i++)

            {

                for (int j = i + 1; j < numbers.Length; j++)

                {

                    if (numbers[i] < numbers[j])

                    {

                        temp = numbers[j];
                        numbers[j] = numbers[i];
                        numbers[i] = temp;
                    }

                }
                //Console.WriteLine("The maximum number formed of given digit is:");
                Console.Write(numbers[i].ToString());
            }

            Console.ReadLine();
        }


    }
}

