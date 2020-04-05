# FileStream &ndash; поток данных
Для работы с файлами, лучще использовать потоки данных (асинхронная работа с файлами, параллельно с другими процессами).

## Создание файла и запись в файл

    string file_name = @"D:\csharp\CSharpProject\text.txt";
    string words = "Hello world!";
    
    // FileStream - создание потока
    // fs - объект
    FileStream fs = File.Open(file_name, FileMode.Create);
    
    // разбиваем строку на байты
    byte[] writeStrByte = Encoding.Default.GetBytes(words);
    
    // записываем байты в файл
    fs.Write(writeStrByte, 0, writeStrByte.Length);

## Вывод информации из файла в консоль

    // с какой позиции считываем данные
    fs.Position = 0;
    byte[] readStrByte = new byte[writeStrByte.Length];
    
    // считываем данные в цикле побайтово
    for(int i = 0; i < writeStrByte.Length; i++)
    {
        readStrByte[i] = (byte)fs.ReadByte();
    }
    
    // переводит байты в строку
    Console.WriteLine(Encoding.Default.GetString(readStrByte));

    // Закрытие потока
    fs.Close();
