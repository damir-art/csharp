# Исключения
## Конструкция try catch finally
Исключение это возможность управлять сообщением ошибки.

Рассмотрим пример исключения. Нужно ввести число от 0 до 255, если ввести например 256 то появится "исключение".

    Console.Write("Введите число от 0 до 255: ");

    byte number = Convert.ToByte(Console.ReadLine());

    Console.WriteLine($"Вы ввели число: {number}");

    Console.ReadKey();

Вводим код исключения в пример:

    Console.Write("Введите число от 0 до 255: ");
    
    try
    {
        byte number = Convert.ToByte(Console.ReadLine());
        Console.WriteLine($"Вы ввели число: {number}");
    } 
    catch(OverflowException)
    {
        Console.WriteLine("Вам нужно ввести число от 0 до 255!");
    }

    Console.ReadKey();

* try - код где может произойти ошибка
* catch - имя ошибки и код вывода надписи

Блоков catch может быть сколько угодно:

    try
    {
        byte number = Convert.ToByte(Console.ReadLine());
        Console.WriteLine($"Вы ввели число: {number}");
    } 
    catch(OverflowException)
    {
        Console.WriteLine("Вам нужно ввести число от 0 до 255!");
    }
    catch(FormatException)
    {
        Console.WriteLine("Вам нужно ввести число, а не строку!");
    }

## finally
`finally` всегда сработает, вне зависимости от того имеется ли исключение или нет. Блок записывают после всех `catch`.

    ...
    catch(FormatException)
    {
        Console.WriteLine("Вам нужно ввести число, а не строку!");
    }
    finally
    {
        Console.WriteLine("Работа программы завершилась!");
    }
    ...
