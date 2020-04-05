# List - динамические массивы
* Создание массива List
* Добавление элемента в List
* Удаление элемента из List
* Сортировка в List

**List** *(список)* - размер не фиксирован (динамический массив), немного более медлителен чем фиксированный массив. 

List - наиболее частоиспользуемая коллекция (особенно в разработке прототипов игр). Для доступа к элементам используются `[ ]`, имеет дополнительные методы.

Для работы с динамическими массивами нужно подключисть библиотеку `using System.Collections.Generic;` благодаря ей мы можем создавать объекты класса `List`.

Класс `List` отвечает за динамические массивы.

## Создание массива
    List<string> sList; // Объявление переменной которая может хранить список List
    sList = new List<string>(); // Инициализация списка
    sList.Add("BMW"); // Добавление элемента в список

Сокращенная запись, объявление и инициализация в одной строке:

    // List<тип данных>, имя массива, выделение памяти
    List<string> cars = new List<string>();

    Console.ReadKey();

## Добавляем элементы
Добавляем элементы сразу:

    List<string> cars = new List<string>() { "Ford", "BMW", "Opel", "Mazda", "Audi" };

### Проход циклом и сортировка
    List<string> cars = new List<string>() { "Ford", "BMW", "Opel", "Mazda", "Audi" };

    string str = "";
    foreach (string el in cars)
    {
        str += el + ", ";
    }
    Console.WriteLine(str);

    cars.Sort();

    string str2 = "";
    foreach (string el in cars)
    {
        str2 += el + ", ";
    }
    Console.WriteLine(str2);

    Console.ReadKey();

### Add()
Добавляем элемент в конец массива `.Add()`:

    cars.Add("Ford");
    cars.Add("Chevrolet");

### AddRange()
Добавляем элемент`ы` в конец массива `.AddRange()`:

    cars.AddRange(new string[] { "Ferrari", "Porsche", "Toyota" });

### Insert()
Добавляем элемент на определённый индекс через `.Insert()`, последующие сдвигаются:

    Console.WriteLine(cars[1]); // BMW
    cars.Insert(1, "Nissan");
    Console.WriteLine(cars[1]); // Nissan

## Удаляем элементы
### .Remove(значение)
Удаляем из массива элемент по его значению:

    Console.WriteLine(cars[0]); // Ford
    cars.Remove("Ford");
    Console.WriteLine(cars[0]); // Nissan

### .RemoveAt(индекс)
Удаляем из массива элемент по его индексу:

    Console.WriteLine(cars[0]); // Nissan
    cars.RemoveAt(0);
    Console.WriteLine(cars[0]); // BMW

## Sort() - сортировка
    List<string> cars = new List<string>() { "Ford", "BMW", "Opel", "Mazda", "Audi" };

    Console.WriteLine(cars[0]); // Ford
    cars.Sort();
    Console.WriteLine(cars[0]); // Audi

## Методы List
* `new List<T>()` - объявляет новую коллекцию List с элементами типа `T`
* `Add(X)` - добавляет элемент X типа T в конец List
* `Clear()` - удаляет все элементы их List
* `Contains(X)` - возвращает true, если элемент  (типа Т) имеется в List
* `Count` - свойство, возвращающее количество элементов в List
* `IndexOf(X)` - возвращает числовой индекс элемента X в List, при отсутствии, возвращает `-1`
* `Insert(индекс, значение)` - вставить значение в индекс
* `Remove(X)` - удаляет элемент X из List
* `RemoveAt(#)` - удаляет из List объект с индексом #

## Разное
* List имеет **динамическую** длину.
* List, как и другие скписки не могут иметь пустые элементы.
* List - обобщенная строго типизированная коллекция.
* `sList.ToArray()` - преобразование списка `List` в простой массив `Array`. 