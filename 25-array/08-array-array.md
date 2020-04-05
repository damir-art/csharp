# Массив массивов
Массив массивов (ступенчатый массив). Такой же как и многомерный, но может иметь вложенные массивы **разной длины**.

Пример ступенчатого массива:

    |A|B|C|D|
    |E|F|G|
    |H|I|
    |J| | |K|

Пример кода:

    // Объявляем двумерный ступенчатый массив
    string[][] jArray;

    // [4] - инициализирум массив с 4-мя элементами
    // [] - элементы это массивы которые могут иметь разную длину
    jArray = new string[4][];

    // Первый элемент ступенчатого массива - это строковый массив состоящий из 4-х элементов
    jArray[0] = new string[4];
    jArray[0][0] = "A";
    jArray[0][1] = "B";
    jArray[0][2] = "C";
    jArray[0][3] = "D";

    // Инициализации массива в одной строке, размер можно не указывать
    jArray[1] = new string[] { "E", "F", "G" };
    jArray[2] = new string[] { "H", "I" };

    // Заполняем третий элемент массивом, второй и третий элементы оставляем пустыми
    jArray[3] = new string[4];
    jArray[3][0] = "J";
    jArray[3][3] = "K";

Ступенчатый массив в отличии от многомерного, считает элементы первого уровня:

    Console.WriteLine("Длина массива: " + jArray.Length); // 4
    Console.WriteLine("Длина элемента с индексом [1]: " + jArray[1].Length + "\n"); // 3

    Console.WriteLine("Вывод массива:\n");
    string str = "";
    foreach(string[] sArray in jArray)
    {
        foreach(string sTemp in sArray)
        {
            if(sTemp != null)
            {
                str += "|" + sTemp;
            } else
            {
                str += "|_";
            }
        }
        str += "|\n";
    }
    Console.WriteLine( str );
    Console.ReadKey();

## Используем цикл `for`
    for (int i = 0; i < jArray.Length; i++)
    {
        for (int j = 0; j < jArray[i].Length; j++)
        {
            if (jArray[i][j] != null)
            {
                str += " | " + jArray[i][j];
            }
            else
            {
                str += " |  ";
            }
        }
        str += " |\n";
    }