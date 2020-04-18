# DirectoryInfo
DirectoryInfo - работа с каталогами.

    DirectoryInfo d = new DirectoryInfo(@"d:\cat");
    d.Create();

Получаем информацию о текущем каталоге:

    DirectoryInfo d = new DirectoryInfo(@"d:\cat");
    // d.Create();

    Console.WriteLine("FullName: {0}", d.FullName);
    Console.WriteLine("Name: {0}", d.Name);
    Console.WriteLine("Parent: {0}", d.Parent);
    Console.WriteLine("CreationTime: {0}", d.CreationTime);
    Console.WriteLine("Attributes: {0}", d.Attributes);
    Console.WriteLine("Root: {0}", d.Root);

    Console.ReadKey();