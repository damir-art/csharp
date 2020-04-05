# Dictionary
**Dictionary** *(словарь)* хранит данные как пары ключ-значение. Словари объявляются с двумя типами, тип для ключа и тип для значения.

Словарь - это ассоциативный массив, массив с пользовательскими ключами. В словарях нет индексов. Динамический массив.

## Создание словаря
Для работы со словарями необходимо подключить библиотеку `using System.Collections.Generic;`

    // <тип данных для ключа, тип данных для значения>
    Dictionary<string, string> domainCountry;
    domainCountry = new Dictionary<string, string>();
    
    // или Dictionary<string, string> domainCountry = new Dictionary<string, string>();

    domainCountry.Add("ru", "Россия");
    domainCountry.Add("us", "США");
    domainCountry.Add("de", "Германия");
    domainCountry.Add("cn", "Китай");
    domainCountry.Add("gb", "Англия");

    foreach(KeyValuePair<string, string> el in domainCountry)
    {
        Console.WriteLine($"Доменная зона: {el.Key}, страна: {el.Value};");
    }
    Console.ReadKey();

* `new Dictionary<Tkey, Tvalue>()` - объявление словаря
* `Add(Tkey, Tvalue)` - добавление элемента в словарь
* `Clear()` - удалить все элементы
* `ContainsKey(Tkey)` - true, если данный ключ существует
* `ContainsValue(Tvalue)` - true, если данное значение существует
* `Count` - возврат количества пар
* `Remove(Tkey)` - удалить значение по ключу
* `TryGetValue (TKey key, out TValue value)` - извлечь значение, связанное с указанным ключом.

Пример с TryGetValue:

    // Помещаем в переменную, значение из словаря, по ключу
    // rus - пользовательское название переменной
    domainCountry.TryGetValue("ru", out string rus);

    Console.WriteLine(rus); // Россия

## Создание словаря и его инициализация
Сразу создаём и инициализируем словарь.

    Dictionary<string, string> domainCountry;
    domainCountry = new Dictionary<string, string>() {
        { "ru", "Россия" },
        { "us", "США" },
        { "de", "Германия" },
        { "cn", "Китай" },
        { "gb", "Англия" }
    };

    foreach (KeyValuePair<string, string> el in domainCountry)
    {
        Console.WriteLine($"Доменная зона: {el.Key}, страна: {el.Value};");
    }
    Console.ReadKey();

## Свойства Dictionary
* `dIS[0]` - доступ к элементу по его индексу
* `dIS[0].Count` - текущее количество элементов

## Методы Dictionary
* `dIS.Add(12, "Hello")` - добавить элемент в словарь
* `dIS[12] = "Hello"` - добавить/изменить элемент в словаре
* `dIS.Clear()` - очистить словарь, сделать его пустым
* `dIS.ContainsKey(1)` - вернет true, если ключ 1 имеется в словаре, выполняется очень быстро
* `dIS.ContainsValue("A lot!")` - вернет true, если значение "A lot!" имеется в словаре, выполняется медленно
* `dIS.Remove(10)` - удалит элемент с ключом 10

## Разное
* Главное преимущество словарей - постоянное время доступа к элементам, скорость доступа кэлементам не зависит от их количества в словаре.
* Словари работают с библиотекой `System.Collections.Generic;`