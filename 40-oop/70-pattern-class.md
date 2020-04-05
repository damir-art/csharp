# Шаблон класса
Передача не только параметров в сам класс как у функций, но также и передача типа данных при создании объекта.

## Test.cs - класс с шаблоном
    using System;

    namespace CSharpProject
    {
        // Шаблонный класс
        class Test<T>
        {
            public T field;
        }

        // Можно передавать несколько типов данных
        class Test2<T, T2, T3>
        {
            public T field;
            public T2 field_2;
            public T3 field_3;

            // Можно реализовать конструктор
            public Test2(T field, T2 field_2, T3 field_3)
            {
                this.field = field;
                this.field_2 = field_2;
                this.field_3 = field_3;
                Console.WriteLine($"Свойство: {field}, Свойство_2: {field_2}, Свойство_3: {field_3} ");
            }
        }
    }

## Program.cs - главный файл

    using System;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                // Созание объекта шаблонного класса
                Test<int> IntObj = new Test<int>();
                IntObj.field = 400;

                Test<char> CharObj = new Test<char>();
                CharObj.field = 'M';

                // Созание объекта шаблонного класса, с передачей несколько типов
                Test2<byte, int, string> Obj = new Test2<byte, int, string>(100, 500, "Hello");
                
                // Obj.field = 254;
                // Obj.field_2 = 400;
                // Obj.field_3 = "Привет";

                Console.ReadKey();
            }
        }
    }
