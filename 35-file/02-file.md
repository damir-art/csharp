# StreamWriter &ndash; поток данных
Рекомендуемый и наиболее удобный способ работы с файлами.

    string file_name = @"D:\csharp\CSharpProject\data.txt";
    string words = "Hello world! \n";

    // создаём объект sw, открываем файл
    StreamWriter sw = File.CreateText(file_name);

    // записываем данные в файл
    sw.Write(words);
    sw.WriteLine("Добавили текстом, на конце стоит Enter.");

    // закрываем файл
    sw.Close();

    // создаём объект sr, открываем файл
    StreamReader sr = File.OpenText(file_name);

    // выводим данные в консоль
    Console.WriteLine(sr.ReadToEnd());

    // закрываем файл
    sr.Close();

    Console.ReadKey();