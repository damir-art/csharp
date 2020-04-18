# Конструктор
Конструктор позволяет заполнить данными объект, сразу после его создания.

Конструктор - инициализирует объект при его создании. Конструктор почти как метод, за исключением того что он ничего не возвращает.

* Имя конструктора должно совпадать с именем класса
* Список параметров может быть пустым
* Модификатор доступа обычно `public`
* Свойства которые заполняются при создании объекта, должны быть `public`.
* Конструктор это метод класса.
* Всегда и везде рекомендуется использовать конструкторы, он создаётся автоматически при создании класса.

    static void Main()
    {
        // Создание объекта н аоснове класса
        Auto BMW = new Auto("БМВ", "328i", 1999, true);
        Auto VAZ = new Auto("Автоваз", "девятка", 1993, false);

        BMW.CarInfo();
        VAZ.CarInfo();

        Console.ReadKey();
    }

    // Класс
    class Auto
    {
        // Свойства
        public string brand;
        public string model;
        public short  year;
        public bool   automatic;

        // Конструктор
        public Auto(string _brand, string _model, short _year, bool _automatic)
        {
            brand     = _brand;
            model     = _model;
            year      = _year;
            automatic = _automatic;
        }

        // Деструктор
        ~Auto()
        {
            Console.WriteLine("Память освобождена!");
        }

        // Метод
        public void CarInfo()
        {
            Console.WriteLine($"Бренд: {brand}");
            Console.WriteLine($"Модель: {model}");
            Console.WriteLine($"Год: {year}");
            Console.WriteLine($"Коробка: {automatic} \n");
        }
    }