# static
**static** позволяет обращаться к свойству или методу, без создания объекта.

Статические свойства или методы принадлежат непосредственно классу, а не объекту.

К статическим свойствам или методам нельзя добавить `this` или обратиться через объект.

Например: `Класс.Метод()` или `Console.WriteLine()`.

## Статические свойства

    public static string car;
    public static int count = 0;

При создании объекта все свойства обнуляются, а статические переменные сохраняют своё значение. Поэтому например можно подсчитать количество созданных объектов, поместив статическую переменную в конструктор.

## Статические методы

    public static void Print()
    {
        Console.WriteLine($"У класса {count} объекта(ов)");
    }

## Рефакторинг и статический метод
Было:

    static void Main()
    {
        int x = 12 * 10;
        int y = 12 * 12;
        Console.WriteLine(x); // 120
        Console.WriteLine(y); // 144
        Console.ReadKey();
    }

Стало:

    static void Main()
    {
        Console.WriteLine(FeetToInches(10)); // 120
        Console.WriteLine(FeetToInches(12)); // 144
        Console.ReadKey();
    }

    // В 1 футе 12 дюймов
    static int FeetToInches(int feet)
    {
        int inches = 12 * feet;
        return inches;
    }