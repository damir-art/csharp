# Класс
## Создание класса

Создаём новый файл-класс:
* `Проект > Добавить класс > Элементы Visual C# > Код > Класс`, задать имя класса `Users`, нажать добавить.

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