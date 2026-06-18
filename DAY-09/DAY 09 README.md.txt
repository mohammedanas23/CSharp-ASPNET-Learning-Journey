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


### Static : 

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Car car1 = new Car("Mustang");
            Car car2 = new Car("Corvette");
            Car car3 = new Car("Lambo");

            Console.WriteLine(Car.numberOfcars);

            Car.StartRace();

            Console.ReadKey();
            Console.Beep();
        }
    }
    class Car
    {
        string model;
        public static int numberOfcars;

        public Car(string model)
        {
            this.model = model;
            numberOfcars++;
        }

        public static void StartRace()
        {
            Console.WriteLine("The Race has begun!");
        }
        
    }

   
    
}



### Inheritance : 

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Car car = new Car();
            Bicycle bicycle = new Bicycle();
            Boat boat = new Boat();

            Console.WriteLine(car.speed);
            Console.WriteLine(car.wheels);
            car.go();

            Console.WriteLine(bicycle.speed);
            Console.WriteLine(bicycle.wheels);
            bicycle.go();

            Console.WriteLine(boat.speed);
            Console.WriteLine(boat.wheels);
            boat.go();

            Console.ReadKey();
            Console.Beep();
        }
    }
    class Vehical
    {
        public int speed = 0;

        public void go()
        {
            Console.WriteLine("This car is moving");
        }
    }
    class Car : Vehical
    {
        public int wheels = 4;

    }
    class Bicycle : Vehical
    {
        public int wheels = 2;
    }
    class Boat : Vehical
    {
        public int wheels = 0;
    }
   
    
}




