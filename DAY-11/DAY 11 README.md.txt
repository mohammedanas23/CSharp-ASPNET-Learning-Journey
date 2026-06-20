### Method Overriding = provides a new version of a method inherited from a parent class.
                        inherited methods must be abstract, virtual, or already overriden
                        used with ToString(); polymorphism


using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Dog dog = new Dog();
            Cat cat = new Cat();

            dog.Speak();
            cat.Speak();

            Console.ReadKey();
            Console.Beep();
            

        }
       
    }
    
    class Animal
    {
        public virtual void Speak()
        {
            Console.WriteLine("The animal goes *brrr*");
        }
    }
    class Dog : Animal
    {
        public override void Speak()
        {
            Console.WriteLine("The dog goes *woof*");
        }
    }
    class Cat : Animal
    {
        public override void Speak()
        {
            Console.WriteLine("The cat goes *meow*");
        }
    }
}

# Explanation : 

Think of Animal as the parent class.

The keyword virtual means:

"Any child class can replace this method with its own version if it wants."

So by default, every animal says:

The animal goes *brrr*

class Dog : Animal

The : means Dog inherits from Animal.

Dog automatically gets everything Animal has.

The keyword override means:

"I don't want to use the parent's Speak() method. I want my own version."

So when Dog speaks:

The dog goes *woof*

instead of:

The animal goes *brrr*

Same thing for Cat:

public override void Speak()
{
    Console.WriteLine("The cat goes *meow*");
}
Step 4: Create objects
Dog dog = new Dog();
Cat cat = new Cat();

You are creating a dog object and a cat object.

Step 5: Call the methods
dog.Speak();
cat.Speak();

C# checks:

Is there an overridden version in Dog? → Yes → Use it.
Is there an overridden version in Cat? → Yes → Use it.

Output:

The dog goes *woof*
The cat goes *meow*
Why use virtual and override?

Imagine a game with 100 animals.

Instead of making:

DogSpeak()
CatSpeak()
LionSpeak()
TigerSpeak()

You can just make:

Speak()

and let every animal decide how it speaks.

dog.Speak();    // woof
cat.Speak();    // meow
lion.Speak();   // roar

This is called Method Overriding, one of the main concepts of Polymorphism.

Simple formula
Parent class method = virtual
Child class method = override


### ToString(); Method : converts an object to its string representation so that it is suitable for display.


using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Car car = new Car("Chevy", "Corvette", 2022, "Yellow");

            Console.WriteLine(car.ToString());

            

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
        public override string ToString()
        {

            return "This is a " + make + " " + model + "," + year + " and the color is " + color; 
        }
    }

}

# Explanation : 

Car car = new Car("Chevy", "Corvette", 2022, "Yellow");

This calls the constructor:

public Car(string make, string model, int year, string color)

So the values become:

make  = Chevy
model = Corvette
year  = 2022
color = Yellow

Every class in C# automatically inherits from a base class called Object.

Object contains a method called:

ToString()

By default, if you write:

Console.WriteLine(car.ToString());

without overriding it, you would get something like:

Programpractice.Car

because C# only knows the object's class name.


public override string ToString()
{
    return "This is a " + make + " " + model + "," + year + " and the color is " + color;
}

The keyword override means:

"Don't use the default ToString() method. Use my custom version instead."

Now when ToString() is called, it returns:

This is a Chevy Corvette,2022 and the color is Yellow

Console.WriteLine(car.ToString());

First:

car.ToString()

returns:

This is a Chevy Corvette,2022 and the color is Yellow

Then:

Console.WriteLine(...)

prints it to the screen.

Output:

This is a Chevy Corvette,2022 and the color is Yellow

Console.WriteLine(car);

and C# will automatically call:

car.ToString();

behind the scenes.

So these are basically the same:

Console.WriteLine(car.ToString());
Console.WriteLine(car);



### Polymorphism : A Greek word that means to have 'many different forms'
                   Objects can be identified by more than one type 

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Polymorphism

            Car car = new Car();
            Bicycle bicycle = new Bicycle();
            Boat boat = new Boat();

            Vehical[] vehicals = { car, bicycle, boat };

            foreach(Vehical vehicle in vehicals)
            {
                vehicle.Go();
            }

            Console.ReadKey();
            Console.Beep();
        }
       
    }
    class Vehical
    {
        public virtual void Go()
        {

        }
    }
    class Car : Vehical
    {
        public override void Go()
        {
            Console.WriteLine("This car is moving!");
        }
    }
    class Bicycle : Vehical
    {
        public override void Go()
        {
            Console.WriteLine("This bicycle is moving!");
        }
    }
    class Boat : Vehical
    {
        public override void Go()
        {
            Console.WriteLine("This boat is moving!");
        }
    }
}

# Explanation : 

Many different objects can be treated as the same type, but each object does its own thing when a method is called.

class Vehical
{
    public virtual void Go()
    {

    }
}

Think of Vehical as the common parent.

You're basically saying:

Every vehicle can move, so every vehicle should have a Go() method.

But you don't specify how it moves.

class Car : Vehical
class Bicycle : Vehical
class Boat : Vehical

All three inherit from Vehical.

Each one creates its own version of Go():

public override void Go()
{
    Console.WriteLine("This car is moving!");
}
public override void Go()
{
    Console.WriteLine("This bicycle is moving!");
}
public override void Go()
{
    Console.WriteLine("This boat is moving!");
}

Car car = new Car();
Bicycle bicycle = new Bicycle();
Boat boat = new Boat();

Now you have three different vehicles.

Vehical[] vehicals = { car, bicycle, boat };

Normally you might think:

"How can a Vehicle array store a Car, Bicycle, and Boat?"

Because:

Car is a Vehicle
Bicycle is a Vehicle
Boat is a Vehicle

Since they all inherit from Vehical, C# allows it.

Think of it like:

Vehicle
 ├── Car
 ├── Bicycle
 └── Boat

 Loop through them
foreach(Vehical vehicle in vehicals)
{
    vehicle.Go();
}

First iteration:

vehicle = car;
vehicle.Go();

Output:

This car is moving!

Second iteration:

vehicle = bicycle;
vehicle.Go();

Output:

This bicycle is moving!

Third iteration:

vehicle = boat;
vehicle.Go();

Output:

This boat is moving!
Final output
This car is moving!
This bicycle is moving!
This boat is moving!


### Interface : defines a "contract" that all the classes inheriting should follow 
                  An interface declares "what a class should do"
                  An inheriting class defines "how it should do it"

                  Benifit = security + multiple inheritance + "plug and play"
                 

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Interface Method

            Rabbit rabbit = new Rabbit();
            Hawk hawk = new Hawk();
            Fish fish = new Fish();

            rabbit.flee();
            hawk.hunt();
            fish.flee();
            fish.hunt();



            Console.ReadKey();
            Console.Beep();
        }
        interface IPray
        {
            void flee();
        }
        interface IPraditor
        {
            void hunt();
        }
       
    }
    class Rabbit
    {
        public void flee()
        {
            Console.WriteLine("The rabbit escaped the praditor!");
        }
    }
    class Hawk
    {
       public void hunt()
        {
            Console.WriteLine("The hawk is searching for food!");
        }
    }
    class Fish
    {
       public void flee()
        {
            Console.WriteLine("The fish flew off the scene!");
        }
        public void hunt()
        {
            Console.WriteLine("The fish is hunting for smaller fish in the ocean!");
        }
    }
    
}

# Explanation : 

code creates interfaces:

interface IPray
{
    void flee();
}

interface IPraditor
{
    void hunt();
}

But your classes are not actually using them.

Normally it should look like:

class Rabbit : IPray
class Hawk : IPraditor
class Fish : IPray, IPraditor

Otherwise they're just normal methods and the interfaces aren't doing anything.

What's an Interface?

Think of an interface as a contract or rulebook.

For example:

interface IPray
{
    void flee();
}

This means:

"Anything that is prey must know how to flee."

And:

interface IPraditor
{
    void hunt();
}

means:

"Anything that is a predator must know how to hunt."

The interface only says what must exist, not how it works.

Rabbit
class Rabbit
{
    public void flee()
    {
        Console.WriteLine("The rabbit escaped the predator!");
    }
}

A rabbit is prey.

When danger comes:

rabbit.flee();

Output:

The rabbit escaped the predator!
Hawk
class Hawk
{
    public void hunt()
    {
        Console.WriteLine("The hawk is searching for food!");
    }
}

A hawk is a predator.

When it hunts:

hawk.hunt();

Output:

The hawk is searching for food!
Fish
class Fish
{
    public void flee()
    {
        Console.WriteLine("The fish flew off the scene!");
    }

    public void hunt()
    {
        Console.WriteLine("The fish is hunting for smaller fish in the ocean!");
    }
}

Fish can be both:

Prey to bigger fish → flee()
Predator to smaller fish → hunt()

So:

fish.flee();

Output:

The fish flew off the scene!

And:

fish.hunt();

Output:

The fish is hunting for smaller fish in the ocean!

Imagine nature has two job roles:

Prey

Rule:

If you're prey, you must know how to run away.

Method:

flee();
Predator

Rule:

If you're a predator, you must know how to hunt.

Method:

hunt();

Now:

Rabbit = only runs away
Hawk = only hunts
Fish = can do both

That's why Fish has both methods.

