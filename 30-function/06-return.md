# Возврат функции `return`
**return** - возврат значения от функции.

Используя `return`, вместо `void` нужно записывать тип данных возвращаемого значения.

Создаём функцию которая возвращает сумму переданных параметров.

    static void Main()
    {
        int x = 3;
        int y = 4;
        int res = Sum(x, y);
        Console.WriteLine(res);
        Console.ReadKey();
    }

    public static int Sum(int a, int b)
    {
        int res = a + b;
        return res;
    }

Сокращаем:

    static void Main()
    {
        Console.WriteLine(sum(3, 4));
        Console.ReadKey();
    }
    
    public static int sum(int a, int b)
    {
        return a + b;
    }
