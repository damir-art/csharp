# Пример работы с наследованием
Пример итогового класса `Users` с конструктором. Задействовано три файла: главный входной файл `Program.cs`, класс Users `Users.cs`, класс `Admin.cs`.

## Admin.cs &ndash; класс Admin

    using System;

    namespace CSharpProject
    {
        public class Admin : Users
        {
            private string role;

            // Получаем данные при создании объекта
            // base - Передаем данные в конструктор родительского класса
            public Admin(string name, string email, string pass, byte age, string role)
                : base(name, email, pass, age)
            {
                this.role = role;
                // this.name = "Админ2";
            }
            public void GetRole()
            {
                Console.WriteLine($"{role}");
            }

            // new - Метод переписывает такой же метод в родительском классе
            public new void PrintAll()
            {
                Console.WriteLine($"Имя: {name}\nЕ-маил: {email}\nПароль: {pass}\nВозраст: {Age}\nРоль: {role}\n");
            }
        }
    }

## Users.cs &ndash; класс Users

    using System;

    namespace CSharpProject
    {
        public class Users
        {
            // Свойства класса
            protected string name;
            protected string email;
            protected string pass;
            
            private byte age;
            // аксессор, не метод
            public byte Age
            {
                // Получить, return обязателен
                get {
                    age++;
                    return age;
                }
                // Установить
                set {
                    //  value - значение переменной
                    if (value < 10)
                        this.age = 1;
                    else
                        this.age = value;
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
                // this.PrintAll();

                // Вычисляем сколько объкетов имеется у класса
                count++;
            }

            // Перегрузка конструктора, конструктор без параметров
            public Users()
            {
                Console.WriteLine("Обратились к конструктору без параметров!\n");
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
                john.PrintAll();
                Users bob = new Users();

                // Объект admin от класса наследника Admin
                Admin admin = new Admin("Администратор", "admin@mail.ru", "123", 23, "root");

                // Доступ к методам родительского класса
                // admin.SetAll("Администратор", "admin@mail.ru", "123", 23);
                admin.PrintAll();

                Users.Print();

                Console.ReadKey();
            }
        }
    }
