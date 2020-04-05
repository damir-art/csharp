# Main() функция

**Main()** - статическая функция принадлежащая к классу. Точка входа любого приложения.

* Всё что написано в функции `Main()` сработает при старте программы.
* Функция `Main()` является основной функцией, без неё программа работать не будет.
* Функция `Main()` в проекте существует в единственном экземплре, в других классах и файлах проекта её не создают.
* В классе где находится функция `Main()` обычно не создают переменные или свойства.

## Console.WriteLine()
Работаем с `Console.WriteLine()`:

    Console.WriteLine("Привет");
    Console.WriteLine("Автомобиль: " + peremennaya);
    
    // Более правильная запись работы с аргументами функций
    Console.WriteLine("Аргумент 1: {0}, Аргумент 2: {1}", arg1, arg2);

## Примеры работы с консолью
Шаблон `№1` для начала работы с консолью:

    string name = "Damir";
    string family = "Gabdrakhimov";
    Console.WriteLine("Имя: {0}, Фамилия: {1}", name, family);
    Console.ReadKey(); // без этой строки, консоль сразу закроется, чтобы закрыть консоль, нажмите `Enter`

Далее в руководстве подробно будет описана каждая строка данного кода.

Шаблон `№2` для ввода данных в консоль, преобразования данных и их вывода в консоль.

    Console.WriteLine("Введите своё имя: ");
    string name = Console.ReadLine();

    Console.WriteLine("Введите свою фамилию: ");
    string family = Console.ReadLine();

    Console.WriteLine("Введите свой возраст: ");
    byte age = Convert.ToByte(Console.ReadLine());

    Console.WriteLine(
        "Имя: " + name + "\n" +
        "Фамилия: " + family + "\n" +
        "Возраст: " + age
    );

    // Console.WriteLine("Имя: {0}, Фамилия: {1}, Возраст: {2}", name, family, age);

    // Console.WriteLine("Имя: {0} \nФамилия: {1} \nВозраст: {2}", name, family, age);
   
    // Console.WriteLine($"Имя: {name}, Фамилия: {family}, Возраст: {age}");

    Console.ReadKey();

## Разное
`$` позволяет выводить переменные и элементы массивов внутри финурных скобок:

    Console.WriteLine($"Ключ: {el.Key}, Значение: {el.Value}");