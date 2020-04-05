# Игра: &laquo;Угадай число&raquo;

    byte rand = 8;
    byte userInput;
    do
    {
        Console.WriteLine("Введите число от 1 до 10: ");
        userInput = Convert.ToByte(Console.ReadLine());
    } while (userInput != rand);
    Console.WriteLine("Победа! Число угадано!");
    Console.ReadKey();
