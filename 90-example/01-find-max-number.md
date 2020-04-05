# Поиск максимального элемента в массиве

    static void Main(string[] args)
    {
        int[] num = { 4, 5, 7, 9, 14, 0 };
        Console.WriteLine(maxEl(num));
        Console.ReadKey();
    }
    public static int maxEl(int[] num)
    {
        int max = num[0];
        foreach(int el in num)
        {
            if(el > max)
            {
                max = el;
            }
        }
        return max;
    }
