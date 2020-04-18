# Пример работы с this
Пример итогового класса `Users` с конструктором. Задействовано три файла: главный входной файл `Program.cs`, класс Users `Users.cs`, класс `Admin.cs`.

## Admin.cs &ndash; класс Admin

    using System;

    namespace CSharpProject
    {
        public class Admin
        {
            public string role = null;
        }
    }

## Users.cs &ndash; класс Users

    using System;

    namespace CSharpProject
    {
        public class Users
        {
            // Свойства класса
            private string name;
            private string email;
            private string pass;
            private byte   age;
            // свойство как объект, имя класса, имя объекта
            private Admin root = new Admin();

            // Конструктор
            public Users(string name, string email, string pass, byte age)
            {
                // Присваиваем значения свойствам
                this.name = name;
                this.email = email;
                this.pass = pass;
                this.age = age;

                // Обращаемся к методу класса, тут this не обязателен
                this.PrintAll();
            }

            // Перегрузка конструктора, для создания роли
            public Users(string _name, string _email, string _pass, byte _age, string role)
            {
                name = _name;
                email = _email;
                pass = _pass;
                age = _age;
                root.role = role;

                // Обращаемся к методу класса
                PrintAll();
            }

            // Перегрузка конструктора, конструктор без параметров
            public Users()
            {

            }

            // Методы класса
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

            public void SetAdmin(string role)
            {
                root.role = role;
            }

            // Метод класса для работы с приватным свойством
            public string GetAdminRole()
            {
                return root.role;
            }
        }
    }

## Program.cs &ndash; главный входной файл

    using System;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                Users john = new Users("Джон", "john@mail.ru", "123", 27);

                Users admin = new Users("Админ", "admin@mail.ru", "12345", 33, "admin");

                Console.WriteLine(admin.GetAdminRole());
                
                Console.ReadKey();
            }
        }
    }
