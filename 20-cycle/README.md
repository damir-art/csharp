# Циклы

* while
* do ... while
* for
* foreach

Циклы `for` и `foreach` наиболее частоиспользуемые. 

`i`, `j`, `k` имена переменных обычно используемых для счетчиков.

## Проход циклом по строке
    string str = "Hello";
    foreach (char chr in str)
    {
        Console.WriteLine(chr);
    }

    Console.ReadKey();