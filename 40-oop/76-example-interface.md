# Пример работы с интерфейсом

## Program.cs

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

            Console.ReadKey();
        }
    }
}

## ILights.cs

    using System;

    namespace CSharpProject
    {
        interface ILights
        {
            float Brightness { get; set; }
            bool IsOn { get; set; }

            void TurnOnOff(bool IsOn);
            bool IsLightOn();
        }
    }

## ILightProblems.cs

    using System;

    namespace CSharpProject
    {
        interface ILightProblems
        {
            void ElectricError();
        }
    }

## BraLights.cs

    using System;

    namespace CSharpProject
    {
        // Класс наследник двух интерфейсов
        class BraLights : ILights, ILightProblems
        {
            public float Brightness { get; set; }
            public bool IsOn { get; set; }

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
