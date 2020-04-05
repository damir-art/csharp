# Меняем элементы массива
Меняем местами элементы массивов, используем ссылки `ref`.

    static void Main(string[] args)
    {
        int[] arr1 = { 1, 2, 3 };
        int[] arr2 = { 10, 20, 30 };

        foreach(int el in arr1)
            Console.Write("{0} ", el);
        Console.WriteLine("");
        foreach (int el in arr2)
            Console.Write("{0} ", el);

        Console.WriteLine("");
        Console.WriteLine("");
        changeArrays(ref arr1, ref arr2);
        foreach (int el in arr1)
            Console.Write("{0} ", el);
        Console.WriteLine("");
        foreach (int el in arr2)
            Console.Write("{0} ", el);

        Console.ReadKey();
    }
    
    public static void changeArrays(ref int[] a, ref int[] b)
    {
        // создаём временный массив
        int[] temp = new int[a.Length];

        a.CopyTo(temp, 0);
        Array.Clear(a, 0, a.Length);
        b.CopyTo(a, 0);
        Array.Clear(b, 0, b.Length);
        temp.CopyTo(b, 0);
    }