# String (строка)
* Строки в C# обрамляются двойными кавычками.
* Последовательность 16-битных символов (Юникод).
* В других яхыках программирования строки являются массивами символов
* В C# строка это объект

## Создание строки

Пример:

    string name = "Damir";
    string family = "Gabdrakhimov";

Получаем первый символ строки:

    string name = "Damir";
    string family = "Gabdrakhimov";
    char d = name[0];
    Console.WriteLine("Имя: {0}, Фамилия: {1}", name, family);
    Console.WriteLine("Первый символ имени: {0}", d); // D
    Console.ReadKey(); // Наживаем любую клавишу, консоль закроется

* Теоретически строка может хранить до 2 млрд символов.

## Свойства и методы
Свойства и методы класса `System.String`
* `Length` - длина строки
* `Compare()` - сравнить две строки (статический метод)
* `Contains()` - есть ли подстрока
* `Equals()` - сравнить две строки
* `Format()` - форматирование строки (статический метод)
* `Insert()` - вставить строку внутрь другой
* `PadLeft(), PadRight()` - дополнить строку слева, справа
* `Remove()` - удалить символы из строки
* `Replace()` - заменить символы в строке, работает с копией
* `Split()` - разделение строки на подстроки
* `Trim()` - удалить определенные символы с начала и с конца
* `ToUpper(), ToLower()` - создать копию в верхнем и нижнем регистре

Со статическими методами нужно работать на уровне класса, а не объекта.

Рассмотрим работу на уровне объекта: 

    string name = "Damir";

    Console.WriteLine("{0}", name.Length); // 5
    Console.WriteLine("{0}", name.ToUpper()); // DAMIR
    Console.WriteLine("{0}", name.Contains("ir")); // True
    Console.WriteLine("{0}", name.Replace("amir", "enis")); // Denis

Рассмотрим работу на уровне класса:

## Конкатенация

    string name = "Damir";
    string family = "Gabdrakhimov";
    Console.WriteLine(name + family);