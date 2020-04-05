# List List
Ступенчатый двумерный список.

    List<List<string>> stList;
    stList = new List<List<string>>();

    // Создать два списка List b добавить их в stList
    stList.Add(new List<string>());
    stList.Add(new List<string>());

    // Добавить элементы в первый список
    stList[0].Add("BMW");
    stList[0].Add("Green");

    // Создать третий список и сразу добавить элементы
    stList.Add(new List<string>( new string[] { "Ford", "Silver" } ));

    string str = "";
    foreach (List<string> stL in stList)
    {
        foreach (string el in stL)
        {
            if (el != null)
            {
                str += " | " + el;
            } else
            {
                str += " | ";
            }
        }
        str += " | \n";
    }

    Console.WriteLine(str);
    Console.ReadKey();