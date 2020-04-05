# Пример работы с абстрактными классами

    Humans.cs  - абстрактный класс
    People.cs  - класс наследник
    UFO.cs     - класс наследник
    Program.cs - главный входной файл

# Humans.cs

    using System;

    namespace CSharpProject
    {
        // Описание общих характеристик для всех живых существ
        abstract class Humans
        {
            public virtual void SayHello()
            {
                Console.WriteLine("None");
            }

            public abstract void Talk();
            public abstract void Walk();
        }
    }

# People.cs

    using System;

    namespace CSharpProject
    {
        // Класс описывающий людей, класс наследник Humans
        class People : Humans
        {
            public override void SayHello()
            {
                // base.SayHello();
                Console.WriteLine("Люди передают привет.");
            }
            public override void Talk()
            {
                Console.WriteLine("Люди говорят.");
            }

            public override void Walk()
            {
                Console.WriteLine("Люди ходят.");
            }
        }
    }

# UFO.cs

    using System;

    namespace CSharpProject
    {
        // Класс описывающий инопланетян, класс наследник Humans
        class UFO : Humans
        {
            //public override void SayHello()
            //{
                // base.SayHello();
                // Console.WriteLine("Инопланетне передают привет.");
            //}
            public override void Talk()
            {
                Console.WriteLine("Инопланетяне говорят.");
            }

            public override void Walk()
            {
                Console.WriteLine("Инопланетяне ходят.");
            }
        }
    }

# Program.cs

    using System;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                Humans john = new People();
                Humans galaxy = new UFO();

                john.SayHello();
                john.Talk();
                john.Walk();

                Console.WriteLine();

                galaxy.SayHello();
                galaxy.Talk();
                galaxy.Walk();

                Console.ReadKey();
            }
        }
    }
