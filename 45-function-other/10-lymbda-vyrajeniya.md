# Лямбда выражения
Лямбда выражения - это функции которые можно записать в одну строку.

    using System;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            delegate float SquareNumber(float number);
            static void Main(string[] args)
            {
                // лямбда выражение
                SquareNumber square = el => el * el;
                Console.WriteLine("8 в квадрате = " + square(8));
                Console.ReadKey();
            }
        }
    }
 