# Массивы и циклы
Перебираем массив в цикле.

    string[] cars = new string[]
    {
        "Ford", "BMW", "Opel", "Mazda", "Audi"
    };
    for(byte i = 0; i < cars.Length; i++)
    {
        Console.WriteLine(cars[i]);
    }
    Console.ReadKey();

При переборе массива в цикле, работаем с элементами.

    string res = "";
    string[] cars = new string[]
    {
        "Ford", "BMW", "Opel", "Mazda", "Audi"
    };
    for(byte i = 0; i < cars.Length; i++)
    {
        res = cars[i] + ": авто";
        Console.WriteLine(res);
    }
    Console.ReadKey();

## Перебор многомерного массива
Сначала перебираем первый массив, потом внутренние массивы-элементы.

    int[,] digits =
    {
        { 12, 7, 4},
        { 12, 7, 4},
        { 12, 7, 4},
        { 12, 7, 4}
    };
    // цикл для гланого массива
    for (byte i = 0; i < 4; i++)
    {
        // цикл для внутренних элементов-массивов
        for (byte j = 0; j < 3; j++)
        {
            Console.Write(digits[i, j] + " ");
        }
        Console.WriteLine("");
    }
    Console.ReadKey();
