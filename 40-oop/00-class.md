# Классы
## Создание класса

Создаём новый файл-класс:
* `Проект > Добавить класс > Элементы Visual C# > Код > Класс`, задать имя класс `Users`, нажать добавить.

Пример класса:

    // Библиотеки
    using System;

    // Пространство имён, класс принадлежит проекту CSharpProject
    namespace CSharpProject
    {
        // Класс
        public class Users
        {
            // Конструктор
            public Users()
            {
            }
        }
    }

## Создание свойств (переменные, поля)

    public class Users
    {
        // Свойства класса
        public string name;
        public string email;
        public string pass;
        byte age;
    }

По-умолчанию у свойств модификатр доступа `private`. Поэтому если нужен к ним доступ из вне прописываем `public`.

## Создание объекта
Объекты создаём не в файле-класса, а в основном файле где есть функция `Main()`, внутри функции `Main()`.

* Пишем название класса `Users`
* Придумываем имя объекту `john`
* Выделяем память `new Users()`

Пример создания объекта:

    Users john = new Users();

## Работа со свойством

    john.name = "Джон";
    john.email = "john@mail.ru";
    john.pass = "1234";
    john.age = 34;

    Console.WriteLine(john.name);

## Упрощаем создание объекта

    Users john = new Users
    {
        name = "Джон",
        email = "john@mail.ru",
        pass = "1234",
        age = 34
    };

## Создание метода

    public void SetAll(string _name, string _email, string _pass, byte _age)
    {
        name  = _name;
        email = _email;
        pass  = _pass;
        age   = _age;
    }

    public void PrintAll()
    {
        Console.WriteLine($"Имя: {name}\nЕ-маил: {email}\nПароль: {pass}\nВозраст: {age}\n");
    }
## Работа с методом

    john.SetAll("Джон", "john@mail.ru", "12345", 35);
    john.PrintAll();

## Свойство как объект другого класса

Другой класс `Admin.cs`:

    using System;

    namespace CSharpProject
    {
        public class Admin
        {
            string role = null;
        }
    }

Сам класс `Users.cs`:

    // свойство как объект, имя класса, имя объекта
    public Admin root = new Admin();

## Разное
* Класс - это тип переменной, содержащий в себе комбинацию переменных и функций.