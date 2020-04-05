# Числа
Числовые типы данных.

## Целое число
* `byte` от 0 до 255 (байт)
* `sbyte` от -128 до +127
* `short` от -32 тыс до +32 тыс
* `ushort` от 0 тыс до 65 тыс
* `int` от -2 млрд 150 млн до 2 млрд 150 млн
* `uint` от 0 до 4 млрд 300 млн
* `long` триллионы (редко используется)
* `ulong` от 0 до триллионы (редко используется)

### int
32-х битное целое число от -2 147 483 648 до 2 147 483 647

    int mln = 1000000;

## Вещественное число (число с плавающей запятой)
Вещественное число (десятичное число) &ndash; число с плавающей запятой (в C# используется точка).

* `float` от -3.4 * 10 ^ 38 до 3.4 * 10 ^ 38, пример `110.5f`
* `double` от -4.9 * 10 ^ 308 до 4.9 * 10 ^ 308 (редко используется)

### float
Вешественное число.

    float fl = 4.5f;
    float fl2 = 1.0f/3.0f;

### double
Вещественное число с двойной точностью.

    double db = 4.5d;

## Свойства
У всех числовых типов есть свойства `MaxValue` и `MinValue`. У double еще имеются Epsilon, PositiveInfinity, NegativeInfinity.

    int x = int.MaxValue;
    int y = int.MinValue;
    double ze = double.Epsilon;
    double zp = double.PositiveInfinity;
    double zn = double.NegativeInfinity;

    Console.WriteLine("Max {0}. Min {1}", x, y);
    Console.WriteLine("Eps {0}. PI {1}. NI {2}", ze, zp, zn);