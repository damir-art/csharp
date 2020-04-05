# Объект
## Создание объекта

Объекты создаём не в файле-класса, а в основном файле где есть функция `Main()`, внутри функции `Main()`.

* Пишем название класса `Users`
* Придумываем имя объекту `john`
* Выделяем память `new Users()`

Пример создания объекта:

    Users john = new Users();

## Упрощаем создание объекта

    Users john = new Users
    {
        name = "Джон",
        email = "john@mail.ru",
        pass = "1234",
        age = 34
    };