# Делегаты
Делегаты - это специальные конструкции, которые указывают на функцию, которую необходимо выполнить.

* Делегаты записывают вне других функций.

Пример:

    using System;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            // Создаём делегат
            delegate void Message();
            delegate int Math(int x, int y);
            static void Main(string[] args)
            {
                // Создание переменной (объекта) на основе делегата
                Message Msg;

                // DateTime - класс для работы с временем и датой
                if(DateTime.Now.Hour < 12)
                {
                    // присваиваем делегату, имя функции
                    Msg = GoodMorning;
                }
                else
                {
                    Msg = GoodDay;
                }

                Msg();

                Math operation = Add;
                Console.WriteLine(operation(3, 5));

                operation = Mult;
                Console.WriteLine(operation(3, 5));

                Console.ReadKey();
            }

            private static int Mult(int x, int y)
            {
                return x * y;
            }

            private static int Add(int x, int y)
            {
                return x + y;
            }

            private static void GoodMorning()
            {
                Console.WriteLine("Доброе утро!");
            }
            private static void GoodDay()
            {
                Console.WriteLine("Добрый день!");
            }
        }
    }

