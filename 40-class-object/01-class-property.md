# Свойства класса (переменные, поля)
Создание свойств класса:

    public class Users
    {
        // Свойства класса
        public string name;
        public string email;
        public string pass;
        byte age;
    }

По-умолчанию у свойств модификатр доступа `private`. Поэтому если нужен к ним доступ из вне прописываем `public`.