## Внешние переменные
* out
* ref

## out
Чтобы передать переменную из одной функции в другую нужно воспользоваться оператором `out`.

В примере, `out` говорит о том, что переменную нужно искать внутри той функции где происходит вызов функции.

    static void Main()
    {
        byte num = 7;
        maxEl(out num);
        Console.WriteLine(num); // 8
        Console.ReadKey();
    }
    public static void maxEl(out byte num)
    {
        num = 8;
    }

## ref
Передача по ссылке, меньше затрат памяти, более целесообразно для объектов, массивов и прочих ресурсозатратных сущностей.

    static void Main()
    {
        byte num = 7;
        maxEl(ref num);
        Console.WriteLine(num); // 9
        Console.ReadKey();
    }

    public static void maxEl(ref byte num)
    {
        num = 9;
    }