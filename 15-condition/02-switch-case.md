# switch case
* Заменяет несколько `if else`.
* Проверяет только на равенство.
* Выполняет сравнение только с одной переменной.
* Сравнивает переменную только со значением (литералом).

Пример:

    // можно использовать числовой или строковый тип данных
    string name = "User";

    switch (name)
    {
        case "Bob":
            Console.WriteLine("name == Bob");
            break;
        case "Mickle":
            Console.WriteLine("name == Mickle");
            break;
        case "User":
            Console.WriteLine("name == User");
            break;
        default:
            Console.WriteLine("По-умолчанию");
            break;
    }

    Console.ReadKey();

* `name` - переменная используется для сравнения.
* `case` - литерал сравниваемый с переменной.
* Каждый `case` и `default` должен оканчиваться `break`.
* `default` - код выполняемый по умолчанию, если не будет совпадений.
