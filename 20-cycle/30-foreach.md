# foreach
Цикл для итерации по элементам объектов или коллекций (список, массив, строка). Вся мощь раскрывается при работе с интерфейсами.

Пример со строкой:

    string str = "Hello";
    foreach (char chr in str)
    {
        Console.WriteLine(chr);
    }

    Console.ReadKey();

Пример с массивом чисел:

    int[] digits = { 0, 1, 2, 3, 4, 5 };
    foreach (int i in digits)
        Console.WriteLine(i);

PS: циклы `foreach` работают немного медленнее чем остальные циклы.