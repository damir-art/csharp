# LINQ
## Методы расширения LINQ

### Where
Выбираем определённые данные.

    using System;
    using System.Linq;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                List<short> numbers = new List<short>()
                {
                    7, 6, 1, 4, 9, 5, 30, 117
                };

                // Получаем из массива значения, которые кратны трём и записываем в массив
                // var list = numbers.Where(x => x % 3 == 0).ToList();
                var list = numbers.Where(x => (x > 5) && (x < 13)).ToList();
                foreach(var el in list)
                {
                    Console.WriteLine(el);
                }
                
                Console.ReadKey();
            }
        }
    }

### Select
Выбираем определённые данные и производим с ними манипуляции.

    using System;
    using System.Linq;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            // delegate float SquareNumber(float number);
            static void Main(string[] args)
            {
                // SquareNumber square = el => el * el;

                List<int> numbers = new List<int>();

                // Заполняем массив числами по-порядку, от одного и до сколько чисел брать
                numbers.AddRange(Enumerable.Range(1, 10));
                
                // Получаем квадрат для всех элементов массива
                var squares = numbers.Select(x => x * x);

                foreach (var elem in numbers)
                {
                    Console.WriteLine(elem);
                }

                Console.WriteLine();

                foreach (var elem in squares)
                {
                    Console.WriteLine(elem);
                }
                Console.ReadKey();
            }
        }
    }

### Aggregate
Позволяет функция позволяет работать с элементами массива (сразу с двумя элементами).

    using System;
    using System.Linq;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                List<int> numbers = new List<int>();

                numbers.AddRange(Enumerable.Range(1, 10));

                // посчитаем сумму элементов массива
                int sum = numbers.Aggregate((x, y) => x + y);
                Console.WriteLine($"Сумма элементов {sum}");
                Console.ReadKey();
            }
        }
    }

### Zip
Позволяет работать с несколькими числами одновременно, но при этом эти числа берутся из двух разных массивов.

    using System;
    using System.Linq;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                List<int> numbers = new List<int>();
                numbers.AddRange(Enumerable.Range(0, 9));
                List<int> digits = new List<int>();
                digits.AddRange(Enumerable.Range(10, 19));

                // элемент из numbers умножаем на элемент из digits
                var GroupAndMult = numbers.Zip(digits, (x, y) => x * y);

                foreach(var el in GroupAndMult)
                {
                    Console.WriteLine(el);
                }
                Console.ReadKey();
            }
        }
    }

### Distinct
Очищает массив от повторяющихся элементов.

    using System;
    using System.Linq;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                List<string> words = new List<string> { "hello", "world", "hello", "people" };
                string result = string.Join(", ", words.Distinct());
                Console.WriteLine(result);
                Console.ReadKey();
            }
        }
    }
