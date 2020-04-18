# Свойства класса (переменные, поля)
Свойство класса - модификатор доступа, тип данных, имя свойства.

    public class Users
    {
        // Свойства класса
        public string name;
        public string email;
        public string pass;
        byte age;
    }

По-умолчанию у свойств модификатр доступа `private`. Поэтому если нужен к ним доступ из вне прописываем `public`.