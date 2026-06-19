### Array of Objects :
                        An array of objects is just a collection of objects stored inside a single array so that I can manage multiple objects without creating separate variables for each one.


using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Car[] garage = { new Car("Mustang"), new Car("Lambo"), new Car("Corvette") };

            foreach (Car car in garage)
            {
                Console.WriteLine(car.model);
            }

            Console.ReadKey();
            Console.Beep();
        }
    }
    
    class Car 
    {
        public string model;

            public Car(string model)
        {
            this.model = model;
        }
    }

    
}


### Explanation :

For example, instead of:

Car car1 = new Car("Mustang");
Car car2 = new Car("Lambo");
Car car3 = new Car("Corvette");

I can do:

Car[] garage =
{
    new Car("Mustang"),
    new Car("Lambo"),
    new Car("Corvette")
};


This means:

Go through every car inside the garage one by one and print its model.

Iteration 1:

car = garage[0]
car.model = Mustang

Prints:

Mustang

Iteration 2:

car = garage[1]
car.model = Lambo

Prints:

Lambo

Iteration 3:

car = garage[2]
car.model = Corvette

Prints:

Corvette 


------------------------------------------ 

Passing Objects as Arguments :

This program demonstrates how an object can be passed to a method and modified.


using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Car car1 = new Car("Mustang", "Red");

            Changecolor(car1, "silver");

            Console.WriteLine(car1.model + " " + car1.color);

            Console.ReadKey();
            Console.Beep();
        }
        public static void Changecolor(Car car, string color)
        {
            car.color = color;
        }
    }
    
    class Car 
    {
        public string model;
        public string color;

            public Car(string model, string color)
        {
            this.model = model;
            this.color = color;
        }
    }

    
}

A Car object is created with:

Model = Mustang
Color = Red

The car1 object and the new color "silver" are sent to the Changecolor() method.

public static void Changecolor(Car car, string color)
{
    car.color = color;
}

The method receives the same Car object and changes its color field to "silver".

Console.WriteLine(car1.model + " " + car1.color);

Output:

Mustang silver

Because the object was modified inside the method, the changes are reflected in car1.

