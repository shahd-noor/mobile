# mobile
using System;

using System.Collections.Generic;

using System.Linq;

using System.Text;

using System.Threading.Tasks;



namespace FirstProject

{

    internal class Program

    {

        //C1

        class Purush_BiggestNumber

        {

            public static void BiggestNumber()

            {

                int count = 0;

                Console.WriteLine("Enter Total Number of Integers\n");

                count = int.Parse(Console.ReadLine());



                int[] numbers = new int[count];



                Console.WriteLine("Enter the numbers"); // Input 44, 55, 111, 2 Output = "111"

                for (int temp = 0; temp < count; temp++)

                {

                    Console.WriteLine("value " + temp + ": ");

                    numbers[temp] = int.Parse(Console.ReadLine());

                }

                int largest = numbers[0];

                for (int big = 1; big < numbers.Length; big++)

                {

                    if (largest < numbers[big])

                    {

                        largest = numbers[big];

                    }

                }

                Console.WriteLine("Largest: " + largest);

                Console.ReadKey();

            }

        }





        //c2

        class ReverseExample

        {

            public static void Reverse()

            {

                int n, reverse = 0, rem;

                Console.Write("Enter a number: ");

                n = int.Parse(Console.ReadLine());

                while (n != 0)

                {

                    rem = n % 10;

                    reverse = reverse * 10 + rem;

                    n /= 10;

                }

                Console.Write("Reversed Number: " + reverse + "\n");

            }

        }

        //C3

        class DigitAnalyzer

        {

            public static void GetLargestDigit()

            {

                int n, r, ld = 0;

                Console.Write("Enter a number:");

                n = Convert.ToInt32(Console.ReadLine());



                while (n > 0)

                {

                    r = n % 10;

                    if (ld < r)

                    {

                        ld = r;

                    }

                    n = n / 10;

                }

                Console.WriteLine("Largest digit:" + ld);

            }

        }



        //C4

        class FindNumber

        {

            public static void FindInteger()

            {



                string str;

                Console.Write("Enter a string: ");

                str = Convert.ToString(Console.ReadLine());



                string emptystring = string.Empty;

                int number = 0;

                for (int i = 0; i < str.Length; i++)

                {

                    if (Char.IsDigit(str[i]))

                        emptystring += str[i];

                    else if (emptystring.Length != 0)

                        break;

                }



                if (emptystring.Length > 0)

                    number = int.Parse(emptystring);



                Console.WriteLine("First Number:" + number);

                Console.ReadLine();



            }

        }





        static void Main(string[] args)

        {





            Console.WriteLine("Operation 1");

            Console.WriteLine("Operation 2");

            Console.WriteLine("Operation 3");

            Console.WriteLine("Operation 4");





            while (true)



            {

                Console.WriteLine("Enter a choice:");

                int num = Convert.ToInt32(Console.ReadLine());



                switch (num)

                {

                    case 1:

                        Purush_BiggestNumber.BiggestNumber();

                        break;

                    case 2:

                        ReverseExample.Reverse();

                        break;

                    case 3:

                        DigitAnalyzer.GetLargestDigit();

                        break;

                    case 4:

                        FindNumber.FindInteger();

                        break;

                    default:

                        break;

                }

            }

        }

    }

}
