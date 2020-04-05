# Считаем количество слов в тексте

    Console.WriteLine("Введите текст:");
    string txt = Console.ReadLine();
    Console.WriteLine("Вы ввели: {0}", txt);

    string[] txtArr;
    txtArr = txt.Split(' ');

    Console.WriteLine("Количество слов: {0}", txtArr.Length);

    Console.ReadKey();