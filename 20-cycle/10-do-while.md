# do ... while
Проверяет условие после каждой итерации. Независмо от условия, сделает хотя бы одну итерацию.

    int i = 0;
    do
    {
        Console.WriteLine(i);
        i++;
    } while (i < 10);

    Console.ReadKey();