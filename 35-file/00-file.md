# File &ndash; работа без потока

Создаём файл, записываем в него строку:

    // путь к файлу
    string file_name = @"D:\csharp\CSharpProject\text.txt";
    
    // Создаёт файл и записывает, далее очищает файл и записывает.
    File.WriteAllText(file_name, "Всем привет!");

Создаём файл, записываем в него несколько строк, выводим строки в консоли:

    // путь к файлу
    string file_name = @"D:\csharp\CSharpProject\text.txt";
    
    // Создаёт файл и записывает, далее очищает файл и записывает.
    File.WriteAllText(file_name, "Всем привет! \n Это C#");
    
    // Читаем данные из файла, выводим их в консоли
    foreach(string line in File.ReadAllLines(file_name))
    {
        Console.WriteLine($"Линия: {line}");
    }
    Console.ReadKey();
