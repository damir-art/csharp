# ArrayList
**ArrayList** *(коллекция)* - массив куда мы можем записать элементы разных типов данных.

Подключаем `using System.Collections;`

    ArrayList arrL = new ArrayList();
    arr.Add(15);      // число
    arr.Add("Hello"); // строка
    arr.Add('q');     // символ

    Console.WriteLine(arrL.Count); // длина массива

    foreach(object el in arrL)
    {
        Console.WriteLine(el);
    }
    Console.ReadKey();