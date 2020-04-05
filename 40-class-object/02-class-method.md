# Метод класса (функция)
Создание методов класса:

    public void SetAll(string _name, string _email, string _pass, byte _age)
    {
        name  = _name;
        email = _email;
        pass  = _pass;
        age   = _age;
    }

    public void PrintAll()
    {
        Console.WriteLine($"Имя: {name}\nЕ-маил: {email}\nПароль: {pass}\nВозраст: {age}\n");
    }