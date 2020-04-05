# enum (перечисления)
Благодаря перечислениям мы можем записать некие названия, а затем эти названия использовать как полноценный тип данных.

В проекте можно будет использовать только те типы данных, которые записанны в enum.

Файл для создания перечисления в VS не нашел, просто создавай файл класса.

## Lights.cs - enum
    using System;

    namespace CSharpProject
    {
        // enum (перечисление), записываем названия свветильников
        public enum Lights
        {
            Bra, HallLight, BigLight, SmallLight
        }
    }

## ILights.cs - интерфейс
    using System;

    namespace CSharpProject
    {
        interface ILights
        {
            float Brightness { get; set; }
            bool IsOn { get; set; }

            // enum
            Lights type { get; set; }

            void TurnOnOff(bool IsOn);
            bool IsLightOn();
        }
    }

## BraLights.cs - класс
    using System;

    namespace CSharpProject
    {
        // Класс наследник двух интерфейсов
        class BraLights : ILights, ILightProblems
        {
            public float Brightness { get; set; }
            public bool IsOn { get; set; }

            // enum
            public Lights type { get; set; }

            public void ElectricError()
            {
                Console.WriteLine("Возникла ошибка!"); ;
            }

            public bool IsLightOn()
            {
                return this.IsOn;
            }

            public void TurnOnOff(bool IsOn)
            {
                this.IsOn = IsOn;
            }
        }
    }

## Program.cs - входной файл
    using System;

    namespace CSharpProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                BraLights bra = new BraLights();
                bra.TurnOnOff(false);
                Console.WriteLine(bra.IsLightOn());
                bra.ElectricError();

                // enum
                bra.type = Lights.Bra;

                switch(bra.type)
                {
                    case Lights.BigLight:
                        Console.WriteLine("Big Light");
                        break;
                    case Lights.Bra:
                        Console.WriteLine("Bra Light");
                        break;
                }

                Console.ReadKey();
            }
        }
    }
