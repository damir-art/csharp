# Одномерный массив
Массив - самый простой и быстрый тип коллекций в C#. Не требует импорта библиотек (using). Встроен в язык.

Массив - это набор элементов данных, одного типа.

* Массивы имеют **фиксированную** длину, которая определяется при инициализации.
* Массивы не являются отдельным типов данных.
* Массивы могут быть простыми, многомерными и ступенчатыми.

## Создание массива
Создаём пустой массив с заранее заданным размером (количества элементов):

    // тип массива, имя массива
    byte[] digits;
    // имя массива, размер массива
    digits = new byte[5];

    // сокращенная запись
    byte[] digits = new byte[5];
    
    Console.WriteLine(digits[0]);

    // инициализируем элементы
    digits[0] = 12;
    digits[1] = 1;
    digits[2] = 10;
    digits[3] = 6;
    digits[4] = 7;

Если элементы не инициализированы, то у числовых элементов значения равны `0`, а у строковых `null`.
    
### Создаём элементы сразу
Объявление, инициализация, заполнение. При таком способе нет необходимости указывать явно количество элементов.

С количеством элементов:

    string[] cars = new string[5]
    {
        "Ford", "BMW", "Opel", "Mazda", "Audi"
    };

    Console.WriteLine(cars[1]); // BMW

Без количества элементов:

    string[] cars = new string[]
    {
        "Ford", "BMW", "Opel", "Mazda", "Audi"
    };

    Console.WriteLine(cars[1]); // BMW

Сокращённая запись массива:

    string[] cars = { "Ford", "BMW", "Opel", "Mazda", "Audi" };
    Console.WriteLine(cars[2]); // Opel

## Свойства массива
* `sA[2]` - доступ к элементу массива
* `sA[2] = "AA"` - присваивание значения элементу по его индексу
* `sA.Length` - длина массива

## Статические методы массива
Статические методы являются частью класса `System.Array` (определены в библиотеке `System.Collections`). Достаточно `using System;`.

* `System.Array.IndexOf(cars, "BMW")` - вернуть индекс элемента со значением `C` в массиве `sA`
* `System.Array.Resize(ref sA, 6)` - изменить размер массива. Не работает с многомерными массивами.
* `Array.Clear(cars, 0, cars.Length)` - очистить массив: имя массива, с какого индекса очищать, длина массива. Очищает в значения по умолчанию: `0`, `null`.

Пример где мы увеличиваем существующий массив добавляем значение последнему элементу и сравниваем с `null` предпоследний пустой элемент.

    string[] cars = { "Ford", "BMW", "Opel", "Mazda", "Audi" };
    Console.WriteLine(cars.Length);
    System.Array.Resize(ref cars, 7);
    Console.WriteLine(cars.Length);
    cars[6] = "Автоваз";
    if (cars[5] == null)
    {
        Console.WriteLine("cars[5] = null");
    }
    Console.WriteLine(cars[6]);
    Console.ReadKey();

## Проход циклом по массиву
Массивы удобны для работы с циклами. Выведем все названия авто, хранящиеся в массиве с помощью цикла.

### for
    string[] cars = { "Ford", "BMW", "Opel", "Mazda", "Audi" };

    string str = "";
    for (int i = 0; i < cars.Length; i++)
    {
        str += cars[i] + " ";
    }
    Console.WriteLine(str);

### foreach
    string[] cars = { "Ford", "BMW", "Opel", "Mazda", "Audi" };

    string str = "";
    foreach (string car in cars )
    {
        str += car + " ";
    }
    Console.WriteLine(str);
    Console.ReadKey();

## Копирование массива
    string[] cars = {"Ford", "BMW", "Opel", "Mazda", "Audi"};
    int ln = cars.Length;

    // Записываем количество элементов
    string[] copyCars = new string[ln];

    // Какой массив копируем, куда копируем, с какого индекса
    cars.CopyTo(copyCars, 0);
    copyCars[0] = "Джип";

    string str = "";
    foreach (string car in copyCars)
    {
        str += car + " ";
    }
    Console.WriteLine(str);
    Console.ReadKey();

## Преобразование массивов в списки
Массивы `Array` можно преобразовать в списки `List`.

    // Создать (копию) список carsL из массива cars
    List<string> carsL = new List<string>(cars)

Тоже самое:

    List<string> carsL = new List<string>(string[] { "Ford", "BMW", "Opel", "Mazda", "Audi" })

## Разное
Массивы могут иметь пустые элементы в середине:

    sArray[0] = "These";
    sArray[1] = "are";
    sArray[3] = "some";
    sArray[6] = "words";
