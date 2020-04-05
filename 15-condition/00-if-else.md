# Условный инструктор if
При работе с условным инструктором `if` используют операторы сравнения и логические.

    short num;
    Console.WriteLine("Введите число от -32 000 до 32 000: ");
    num = Convert.ToInt16(Console.ReadLine());

    if (num > 10)
    {
        Console.WriteLine(num + " больше 10");
    } else if (num < 10)
    {
        Console.WriteLine(num + " меньше 10");
    } else
    {
        Console.WriteLine(num + " равно 10");
    }

    Console.ReadKey();

Одна строка кода, фигурные скобки можно опустить:

    if (num > 10)
        Console.WriteLine(num + " больше 10");

Пример с логическим оператором:

    if (num > 10 && num < 50)
    {
        Console.WriteLine(num + " больше 10 и меньше 50");
    }

Пример с вложенным if:

    if (num > 10) {
        Console.WriteLine(num + " больше 10");
    } else {
        if (num == 10) {
            Console.WriteLine(num + " равно 10");
        } else {
            Console.WriteLine(num + " меньше 10");
        }
    }

Пример с одной строкой:

    if(a < b) break;