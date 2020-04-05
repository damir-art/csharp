# Создание и вызов функции
## Создание функции
Функции создают внутри класса и вне другой функции.

    public static void print()
    {
        Console.WriteLine("Hello World!");
    }

Описание функции:
* `public` - функция доступна отовсюду.
* `static` - функция не принадлежит каким-либо объектам, а принадлежит классу.
* `void` - функция ничего не возвращает.
* `print` - пользовательское имя функции.

## Вызов функции
Вызов происходит внути функции `Main()`:

    static void Main(string[] args)
    {
        print();
        Console.ReadKey();
    }
    public static void print()
    {
        Console.WriteLine("Hello World!");
    }

## Шаблон функции
Шаблон функции с аргументами, параметрами и return.

    static void Main()
    {
        Console.WriteLine(Sum(3, 4));
        Console.ReadKey();
    }
    
    public static int Sum(params int[] numbers)
    {
        int um = 0;
        foreach(int el in numbers) {
            sum += el;
        }
        return sum;
    }
