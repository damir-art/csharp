# Операторы is и as
Операторы is и as позволяют работать с типами данных для конкретных объектов.

## is

`is` - проверяет, является ли объект созданным от какого либо класса.

Условие проверяет, является ли obj с типом данных Admin, т.е является ли объект созданным от класса Admin:

    if(obj is Admin) {
        obj.favBook.printBook();
    }

## as

`as` - позволяет привести объект в определённый тип данных и скопировать его в другой объект, если копирование не сработает то в объект запишется `null`.

    Admin newObj = obj as Admin;

## Program.cs

    using System;
    using System.Collections.Generic;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                // создём объект на основе структуры
                Book bookName = new Book(300, "Автор", "Книга", 2019);
                Book bookName2 = new Book(350, "Автор2", "Книга2", 2019);

                // создаём объект на основе класса UersStruct
                UsersStruct john = new UsersStruct(25, "Джон", true, bookName);

                // Наследуемся от UsersStruct, конструктор используем Admin
                UsersStruct admin = new Admin(27, "Питер", true, bookName2, "Администратор");

                // Помещаем объекты john и admin в массив
                List<UsersStruct> people = new List<UsersStruct>();
                people.Add(john);
                people.Add(admin);

                // Выводим объекты
                foreach (UsersStruct obj in people)
                {
                    // as
                    Admin newObj = obj as Admin;

                    // is - является ли obj с типом данных Admin
                    if(newObj is Admin)
                        newObj.favBook.printBook();
                }

                Console.ReadKey();
            }
        }
    }
