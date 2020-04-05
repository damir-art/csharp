# Пример работы с accessor
Пример итогового класса `Users` с конструктором. Задействовано три файла: главный входной файл `Program.cs`, класс Users `Users.cs`, класс `Admin.cs`.

## Admin.cs &ndash; класс Admin

    using System;

    namespace CSharpProject
    {
        public class Admin
        {
            public static string role = null;
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
            
            private byte age;
            // аксессор, не метод
            public byte Age
            {
                // Получить, return обязателен
                get
                {
                    age++;
                    return age;
                }
                // Установить
                set
                {
                    //  value - значение переменной
                    if (value < 10)
                    {
                        this.age = 1;
                    }
                    else
                    {
                        this.age = value;
                    }
                }
            }

            // статическая переменная
            public static int count = 0;

            // Конструктор
            public Users(string name, string email, string pass, byte age)
            {
                // Присваиваем значения свойствам
                this.name = name;
                this.email = email;
                this.pass = pass;
                // Обрабатываем аксессором
                Age = age;

                // Обращаемся к методу класса, тут this не обязателен
                this.PrintAll();

                // Вычисляем сколько объкетов имеется у класса
                count++;
            }

            // Перегрузка конструктора, для создания роли
            public Users(string _name, string _email, string _pass, byte _age, string role)
            {
                name = _name;
                email = _email;
                pass = _pass;
                Age = _age;
                Admin.role = role;

                // Обращаемся к методу класса
                PrintAll();

                count++;
            }

            // Перегрузка конструктора, конструктор без параметров
            public Users()
            {
                count++;
            }

            // Методы класса
            public void SetAll(string _name, string _email, string _pass, byte _age)
            {
                name  = _name;
                email = _email;
                pass  = _pass;
                Age   = _age;
            }

            public void PrintAll()
            {
                Console.WriteLine($"Имя: {name}\nЕ-маил: {email}\nПароль: {pass}\nВозраст: {Age}\n");
            }

            public void SetAdmin(string role)
            {
                Admin.role = role;
            }

            // Метод класса для работы с приватным свойством
            public string GetAdminRole()
            {
                return Admin.role;
            }

            // Статический метод
            public static void Print()
            {
                Console.WriteLine($"У класса {count} объекта(ов)");
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
                Users john = new Users("Джон", "john@mail.ru", "123", 25);
                Users admin = new Users("Админ", "admin@mail.ru", "12345", 33, "admin");
                Users bob = new Users();

                // Обращение к статическому свойству
                Console.WriteLine(Users.count);
                // Обращение к статическому методу
                Users.Print();

                // Получить переменную аксессор
                Console.WriteLine(john.Age);
                Console.WriteLine(admin.Age);

                Console.ReadKey();
            }
        }
    }
