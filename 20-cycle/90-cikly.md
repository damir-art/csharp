# Циклы
* for
* while
* do while
* операторы циклов: 
* foreach

Цикл позволяет выполнить код несколько раз. Циклы удобны для перебора элементов в массиве.

## for
    for(byte i = 0; i < 10; i++)
    {
        Console.WriteLine("Итерация: " + i);
    }
    Console.ReadKey();

При одной строке кода, фигурные скобки можно опустить:

    for(byte i = 0; i < 10; i++)
        Console.WriteLine("Итерация: " + i);
    Console.ReadKey();

## while
    byte i = 0;
    while(i < 10)
    {
        Console.WriteLine("Итерация: " + i);
        i++;
    }
    Console.ReadKey();

## do while
    byte i = 0;
    do
    {
        Console.WriteLine("Итерация: " + i);
        i++;
    } while (i < 10);
    Console.ReadKey();

## Операторы циклов
### break
Прерывает цикл.

    for (byte i = 1; i <= 20; i++)
    {
        if (i == 16)
        {
            break;
        }
        Console.WriteLine("Итерация: " + i);
    }
    Console.ReadKey();

### continue
Прерывает итерацию.

    for (byte i = 1; i <= 20; i++)
    {
        if (i % 2 == 0)
        {
            continue;
        }
        Console.WriteLine("Итерация: " + i);
    }
    Console.ReadKey();

## foreach
Цикл для работы с массивами.

    string[] cars = new string[]
    {
        "Ford", "BMW", "Opel", "Mazda", "Audi"
    };
    foreach (string el in cars)
    {
        Console.WriteLine(el + ": авто");
    }
    Console.ReadKey();

Динамический массив:

    List<string> cars = new List<string>() { "Ford", "BMW", "Opel", "Mazda", "Audi" };
    foreach (string el in cars)
    {
        Console.WriteLine(el + ": авто");
    }
    Console.ReadKey();
