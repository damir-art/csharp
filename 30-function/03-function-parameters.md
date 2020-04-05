# Аргументы и параметры
При вызове функции в неё можно добавлять аргументы:

    static void Main(string[] args)
    {
        print("БМВ", 150);
        print("БМВ", 100);

        // Можно передавать переменные
        string ford = "Форд";
        print(ford, 100);
        Console.ReadKey();
    }

    public static void print(string car, byte power)
    {
        Console.WriteLine("Автомобиль: " + car);
        Console.WriteLine("Мощность: " + power + "\n");
    }

* параметры - при объявлении
* аргументы - при вызове

## Параметры по-умолчанию
Можно добавлять парамтеры по-умолчанию:
    
    static void Main()
    {
        Print("БМВ");
        Console.ReadKey();
    }

    public static void Print(string car, byte power = 120)
    {
        Console.WriteLine("Автомобиль: {0}, Мощность: {1}", car, power);
    }
