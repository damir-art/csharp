# Пример класса №0
Создадим класс который выведет на экран параметры компьютера.



    static void Main()
    {
        // Создание объекта н аоснове класса
        SysInfo MyComp = new SysInfo();

        // Вывод свойств объекта в консоли
        Console.WriteLine($"Версия операционной системы: {MyComp.win}");
        Console.WriteLine($"Имя компьютера: {MyComp.hostname}");
        Console.WriteLine($"Имя пользователя: {MyComp.username}");
        Console.WriteLine($"Количество процессоров: {MyComp.cpu}");
        Console.WriteLine($"Версия .NET: {MyComp.net}");

        Console.ReadKey();
    }

Все поля класса публичные, к ним можно обращаться за пределами класса:

    // Класс
    class SysInfo
    {
        // Свойства
        public string win;
        public string hostname;
        public string username;
        public string net;
        public string cpu;

        // Конструктор, совпадает с именем класса
        public SysInfo()
        {
            win      = Environment.OSVersion.ToString();
            hostname = Environment.MachineName.ToString();
            username = Environment.UserName.ToString();
            cpu      = Environment.ProcessorCount.ToString();
            net      = Environment.Version.ToString();
        }
    }

* Environment - класс обладающий информацией о системе, каждое его поле это объект который нужно преобразовать в `string`