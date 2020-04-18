# String (строка)
Строка - последовательность 16-битных символов (Юникод).
* **string** - псевдоним типа `System.String`
* Строки в C# обрамляются двойными кавычками.
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

## Свойства
Свойства и методы класса `System.String`
* `Length` - длина строки

## Методы
### Поиск
* `IndexOf(), LastIndexOf` - поиск символа внутри строки
* `Contains(), StartsWith(), EndsWith()` - поиск подстроки внутри строки

### Манипуляция
Возвращает новую строку:
* `Substring()` - извлечь часть строки
* `Insert(), Remove()` - вставить, удалить символы в указанной позиции
* `PadLeft(), PadRight()` - добавить пробельные символы
* `Trim()` - удалить определенные символы с начала и с конца

* `Equals()` - сравнить две строки
* `Format()` - форматирование строки (статический метод)
* `Replace()` - заменить символы в строке, работает с копией
* `Split()` - разделение строки на подстроки
* `ToUpper(), ToLower()` - создать копию в верхнем и нижнем регистре
* `CompareTo()` - сравнить две строки (статический метод)

Со статическими методами нужно работать на уровне класса, а не объекта.

Рассмотрим работу на уровне объекта: 

    string name = "Damir";

    Console.WriteLine("{0}", name.Length); // 5
    Console.WriteLine("{0}", name.ToUpper()); // DAMIR
    Console.WriteLine("{0}", name.Contains("ir")); // True
    Console.WriteLine("{0}", name.Replace("amir", "enis")); // Denis

Рассмотрим работу на уровне класса:

## Конкатенация `+`

    string name = "Damir";
    string family = "Gabdrakhimov";
    Console.WriteLine(name + family);

## Интерполяция `$" {x} "`
Вставить переменную внутрь строки:

    string x = "Имя";
    Console.WriteLine($"Привет {x}");

## Примеры с методами

    // Сравнить две строки
    Console.WriteLine("B".CompareTo("A")); // 1
    Console.WriteLine("B".CompareTo("B")); // 0
    Console.WriteLine("B".CompareTo("C")); // -1

    // Возвратить индекс символа
    Console.WriteLine("Привет"[2]); // и
