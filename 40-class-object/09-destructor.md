# Деструктор
Деструктор - метод вызываемый при удалении объекта.

При создании объекта используется оператор `new`, который выделяет память для объекта.

* Память нужно освобождать от неиспользуемых объектов.
* В `C++` освобождение памяти осуществляется в ручную, через оператор `delete`.
* В `C#`, `PHP` и др. сборка мусора (освобождение) памяти осуществляется автоматически.
* Используйте деструкторы без модификатора доступа.

Синтаксис определения деструктора такой же как и у констурктора, перед именем конструктора нужно поставить тильду `~`:

    // Деструктор
    ~Auto()
    {
        Console.WriteLine("Память освобождена!");
    }

В деструкторе можно использовать параметры.

Обычно деструкторы не нужны, поскольку освобождение памяти происходит автоматически. Но можно освободить ресурсы явно, например закрыть используемые файлы и сетевые соединения.