### Constructure : A special method is a class with the same name as the class name anf can be used to assign arguments to fields when creating an objects 


using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Car car1 = new Car("Ford", "Mustang", 2022, "Yellow");

            car1.Drive();

            Console.ReadKey();
            Console.Beep();
        }
    }
    class Car
    {
        string make;
        string model;
        int year;
        string color;

        public Car(string make, string model, int year, string color)
        {
            this.make = make;
            this.model = model;
            this.year = year;
            this.color = color;
        }
        public void Drive()
        {
            Console.WriteLine("You drive the " + make + " " + model + " " + year + " " + color + " color" );
        }
    }

   
    
}
