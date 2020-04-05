# Руководство C# (C sharp)
Добрый день, вы находитесь в репозитории Гитхаба https://github.com/damir-art/csharp, данный репозиторий является черновиком руководства по C# размещенного по адресу https://csharp.su

C# (C Sharp, си шарп) - язык программирования. С помощью данного языка можно создавать программы для компьютера, в том числе и игры.

Чтобы начать программировать на C# нужно установить редактор (IDE) `Visual Studio Community`, благодаря ей мы сможем писать код для програм и запускать их.

## Установка Visual Studio Community

Visual Studio `Community` - бесплатная версия программы Visual Studio.

* Качаем `Visual Studio Community`: https://visualstudio.microsoft.com/ru/vs/
* Официальное руководство по установке (если вдруг что-то пойдет не так): https://docs.microsoft.com/ru-ru/visualstudio/install/install-visual-studio
* Рабочие нагрузки, выбираем: `Разработка классических приложений .NET`
* Сведения об установке, оставляем как есть
* После скачиваия и установки нажать на кнопку `Запустить`

## Создание проекта в Visual Studio Community
* `Файл > Создать > Проект > Консольное приложение NET Framework` жмём кнопку `Далее`
* Имя проекта (Hello) > Расположение > Поместить решение и проект в одном каталоге (Да) > Создать

Получим следующий код:

    // using - подключение библиотек 
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    // namespace - пространство имён, общее хранилище для классов
    namespace Hello
    {
        // класс Program
        class Program
        {
            // Функция Main обязательна в любой программе
            static void Main(string[] args)
            {
            }
        }
    }

## Запуск проекта
* Пуск - зелёная стрелка над редактором
* или `Отладка > Начать отладку (F5)`

## О языке
* Все данные: переменные и функции должны находиться внутри классов
* // - комментарий
* `.cs` - си шарп, файлы языка
* Объектно-ориентированный

## Ссылки
* https://docs.microsoft.com/ru-ru/dotnet/csharp/ - оф документация
* https://metanit.com/sharp/ - учебник