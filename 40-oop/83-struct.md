# Структуры
Структуры - это небольшие классы. В структурах описываются маленькие объекты.

В структурах можно записывать свойства, методы и конструкторы.

## UsersStruct.cs - обычный класс со структурой

    using System;

    namespace CSharpProject
    {
        // Обычный класс в котором будет находится структура
        public class UsersStruct
        {
            private int    age;
            private string name;
            private bool   hasCar;
            
            // из favBook создаём структуру
            public Book favBook { get; private set; }

            public UsersStruct(int age, string name, bool hasCar, Book favBook)
            {
                this.age     = age;
                this.name    = name;
                this.hasCar  = hasCar;
                this.favBook = favBook;
            }
        }
    }

## Book.cs - структура

    using System;

    namespace CSharpProject
    {
        public struct Book
        {
            private short pages;
            private string avtor, name;
            private short date;
            public Book(short pages, string avtor, string name, short date)
            {
                this.pages = pages;
                this.avtor = avtor;
                this.name  = name;
                this.date  = date;
            }
            public void printBook()
            {
                Console.WriteLine($"Количество страниц: {pages}, Автор книги: {avtor}, Название книги: {name},  Дата публикации: {date}");
            }
        }
    }

## Program.cs - главный файл

    using System;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                // создём объект на основе структуры
                Book bookName = new Book(300, "Автор", "Книга", 2019);
                
                // создаём объект на основе класса UersStruct
                UsersStruct john = new UsersStruct(25, "Джон", true, bookName);

                john.favBook.printBook();

                Console.ReadKey();
            }
        }
    }
