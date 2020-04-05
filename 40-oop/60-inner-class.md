# Вложенные (внутренние) классы
Вложенные классы, это классы находящиеся внутри других классов.

Вложенные классы используют для расширения функционала тех классов в которых находятся.

Во внутренних классах тоже могут содержатся свойства, методы, конструкторы.

Главный файл:

    // Создание объекта на основе класса Car
    Car bmw = new Car(110.5f);
    Console.WriteLine($"Скорость: {bmw.GetSpeed()} км/ч");

    // Создание объекта на основе вложенного класса Car
    Car.Engine bmwEngine = new Car.Engine();
    bmwEngine.StartEngine(true);
    Console.WriteLine($"Двигатель включен? {bmwEngine.GetIsStart()}");

Класс и вложенный класс:

    using System;

    namespace CSharpProject
    {
        class Car
        {
            protected float speed;
            public Car(float speed)
            {
                this.speed = speed;
            }
            public float GetSpeed()
            {
                return this.speed;
            }
            // Вложеннй класс отвечающий только за двигатель
            public class Engine
            {
                // По-умолчани, значение у булевой переменной равно false
                private bool isStart;
                public void StartEngine(bool isStart)
                {
                    this.isStart = isStart;
                }
                public bool GetIsStart()
                {
                    return this.isStart;
                }
            }
        }
    }
