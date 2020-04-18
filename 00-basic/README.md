# Начало работы
Изучим основные работы с C#, программой Visual Studio и консолью.

## Код
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Hello
    {
        class Program
        {
            static void Main(string[] args)
            {
                Console.WriteLine("Hello, World!");
                Console.ReadKey();
            }
        }
    }

## Сборка проекта
* Включим панель вывода: `Вид > Вывод`
* Соберем проект: `Сборка > Построить Имя_проекта` (появится отчет компилятора и расположение .exe файла)

## Запуск проекта
* Кнопка `Пуск` на панели инструментов
* Программа сразу закроется

Чтобы увидеть строку `Hello, World!`, есть два варианта:
* Добавить в конце кода строку: `Console.ReadKey();`
* Открыть `.exe` файл через консоль

## Что есть что в коде
* `namespace` Hello - простарнство имён
* `class` Program - класс Program
* `static void` Main(string[] args) - метод Main
