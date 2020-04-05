# Неограниченное число параметров
**params** - оператор позволяющий функции принимать неограниченное число параметров как в виде обычных переменных так и ввиде массива.

**params** - используется при передаче заранее не известного количества параметров.

    static void Main()
    {
        SumArg(1, 2, 3, 4);       // 10
        SumArg(2, 3, 5, 16, 100); // 126
        Console.ReadKey();
    }
    
    public static void SumArg(params int[] numbers)
    {
        int sum = 0;
        foreach(int el in numbers) {
            sum += el;
        }
        Console.WriteLine("Сумма всех элементов равна {0}", sum);
    }