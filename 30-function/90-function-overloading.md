# Перегрузка функций
Перегрузка функций это возможность использовать несколько функций с одним и тем же именем. Какая функция отработает, зависит от переданных ей параметров.

Перегрузка создаётся при использовании разного количества параметров и/или использования разного типа данных у параметров.

    static void Main()
    {
        Console.WriteLine(Sum(3, 4));     // 7
        Console.WriteLine(Sum(300, 400)); // 700
        Console.WriteLine(Sum(3, 4, 5));  // 12
        Console.ReadKey();
    }

    public static int Sum(byte a, byte b)
    {
        return a + b;
    }
    
    public static int Sum(short a, short b)
    {
        return a + b;
    }
    
    public static int Sum(int a, int b, int c)
    {
        return a + b + c;
    }
