namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            do
            {
                // calculator program;

                double num1 = 0;
                double num2 = 0;
                double result = 0;

                Console.WriteLine("--------------------");
                Console.WriteLine("Calculator Program");
                Console.WriteLine("--------------------");

                Console.Write("Enter your first number: ");
                num1 = Convert.ToDouble(Console.ReadLine());

                Console.Write("Enter your second number: ");
                num2 = Convert.ToDouble(Console.ReadLine());

                Console.WriteLine("\t+, Add");
                Console.WriteLine("\t-, Subtract");
                Console.WriteLine("\t*, Multiply");
                Console.WriteLine("\t/, Divide");
                Console.Write("Enter an option");

                switch (Console.ReadLine())
                {
                    case "+":
                        result = num1 + num2;
                        Console.WriteLine($"Your result {num1} + {num2} = " + result);
                        break;

                    case "-":
                        result = num1 - num2;
                        Console.WriteLine($"Your result {num1} - {num2} = " + result);
                        break;

                    case "*":
                        result = num1 * num2;
                        Console.WriteLine($"Your result {num1} * {num2} = " + result);
                        break;

                    case "/":
                        result = num1 / num2;
                        Console.WriteLine($"Your result {num1} / {num2} = " + result);
                        break;
                }
                Console.WriteLine("Would you like to continue? (Y = yes); (N = no): ");
            } while (Console.ReadLine().ToUpper() == "Y");


            Console.WriteLine("ThankYou!!!");
            Console.ReadKey();
        }    
    }
}

### Array in C#:
namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // array = a variable that can store multiple values. fixed values 

            string[] cars = new string[3];

            //string[] cars = { "BMW", "Mustang", "Corvette" };

            cars[0] = "Tesla";
            cars[1] = "Mustang";
            cars[2] = "Corvette";

            Console.WriteLine(cars[0]);
            Console.WriteLine(cars[1]);
            Console.WriteLine(cars[2]);
          
            Console.ReadKey();
        }    
    }
}

# EXPLANATION : 
                Arrays

When we are making a program, sometimes we need to store multiple values of the same type. Imagine I have three car names:

"BMW"
"Mustang"
"Corvette"

One way would be to create three separate variables, but that would become messy if we had 10, 20, or even 100 car names.

That is where arrays come in.

An array is a collection that allows us to store multiple values of the same data type under one variable name.

For example:

string[] cars = { "BMW", "Mustang", "Corvette" };

Here:

string[] means we are creating an array of strings.
cars is the name of the array.
Inside the curly braces are the values stored in the array.

Each value gets its own position, called an index.

cars[0] = "BMW"
cars[1] = "Mustang"
cars[2] = "Corvette"

Notice that arrays start counting from 0, not 1.

So if I want to display only the first car, I can do:

Console.WriteLine(cars[0]);

And if I want the second or third car:

Console.WriteLine(cars[1]);
Console.WriteLine(cars[2]);

Another way to create an array is by deciding beforehand how many values it can store:

string[] cars = new string[3];

This creates an array that can store exactly 3 strings.

Then we can add values later:

cars[0] = "Tesla";
cars[1] = "Mustang";
cars[2] = "Corvette";

So in simple words, an array is just a way to keep multiple related values together under one variable name.


### FOREACH LOOP : 

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // froeach loop = a simpler way to iterate over an array, but it is less fixed.

            string[] cars = { "BMW", "Mustang", "Corvette" };

            foreach(string car in cars)
            {
                Console.WriteLine(car);
            }
          
            Console.ReadKey();
        }    
    }
}

# EXPLANATION :
                Foreach Loop

Now let's say we have this array:

string[] cars = { "BMW", "Mustang", "Corvette" };

If we want to display every car, we could do this:

Console.WriteLine(cars[0]);
Console.WriteLine(cars[1]);
Console.WriteLine(cars[2]);

This works, but imagine having 100 cars in the array. Writing 100 Console.WriteLine() statements would be a nightmare.

This is where the foreach loop helps us.

foreach(string car in cars)
{
    Console.WriteLine(car);
}

Let's break it down.

foreach(string car in cars)

This means:

Go through every value inside the cars array one by one. Whenever you find a value, temporarily store it in a variable called car.

So the program does this behind the scenes:

car = "BMW"
Console.WriteLine(car);

car = "Mustang"
Console.WriteLine(car);

car = "Corvette"
Console.WriteLine(car);

The output becomes:

BMW
Mustang
Corvette

The best thing about foreach is that it doesn't care whether the array has 3 values or 300 values. It will automatically go through all of them.

So in simple words:

A foreach loop is an easy way to go through every item in an array and perform an action on each item without having to access every index manually.


### METHOD IN C#:

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // method = performs a section of code whenever it is called "invoked".
            //          benifits = let's us use the code w/o writing it multiple times.

            string name = "Anas";
            int age = 22;

            happybirthdaysong(name, age);
            happybirthdaysong(name, age);
            happybirthdaysong(name, age);

            Console.ReadKey();
        }
            static void happybirthdaysong(string name, int age)
            {
                Console.WriteLine("Happy birthday to you");
                Console.WriteLine("Happy birthday to you");
                Console.WriteLine("Happy birthday to you " + name);
                Console.WriteLine("You are " + age + "years old");
                Console.WriteLine("Happy birthday to you");

            }
          
            
          
    }
}

# EXPLANATION : 
                Methods

When we are writing a program, sometimes we find ourselves writing the same code over and over again.

For example, imagine we want to sing a birthday song three times.

Without methods, we might write:

Console.WriteLine("Happy birthday to you");
Console.WriteLine("Happy birthday to you");
Console.WriteLine("Happy birthday to you Anas");
Console.WriteLine("You are 22 years old");
Console.WriteLine("Happy birthday to you");

and then copy the same five lines again and again.

That works, but it makes the code longer and harder to manage.

This is where methods help us.

A method is a block of code that performs a specific task whenever it is called (invoked).

Instead of writing the same code multiple times, we write it once inside a method and call it whenever we need it.

Creating Variables

First, we create two variables:

string name = "Anas";
int age = 22;

These variables store the person's name and age.

Calling the Method

Next, we call the method:

happybirthdaysong(name, age);
happybirthdaysong(name, age);
happybirthdaysong(name, age);

Every time the program sees one of these lines, it jumps to the method, runs the code inside it, and then comes back.

Since we called it three times, the birthday song will be sung three times.

Creating the Method

Here is the method:

static void happybirthdaysong(string name, int age)
{
    Console.WriteLine("Happy birthday to you");
    Console.WriteLine("Happy birthday to you");
    Console.WriteLine("Happy birthday to you " + name);
    Console.WriteLine("You are " + age + " years old");
    Console.WriteLine("Happy birthday to you");
}

Let's break it down.

static void happybirthdaysong
static allows the method to be called from Main.
void means the method does not return any value.
happybirthdaysong is the name of the method.
Parameters

Inside the parentheses:

(string name, int age)

These are called parameters.

Parameters are placeholders that receive values when the method is called.

When we write:

happybirthdaysong(name, age);

the values are passed into the method.

So:

name = "Anas"
age = 22

inside the method.

What Happens During Execution?

When the program reaches:

happybirthdaysong(name, age);

it temporarily jumps to:

static void happybirthdaysong(string name, int age)

and runs:

Console.WriteLine("Happy birthday to you");
Console.WriteLine("Happy birthday to you");
Console.WriteLine("Happy birthday to you Anas");
Console.WriteLine("You are 22 years old");
Console.WriteLine("Happy birthday to you");

Then it returns back to Main and continues executing the next line.

Since the method is called three times, the whole birthday song is printed three times.

Simple Definition

A method is a reusable block of code that performs a specific task whenever it is called. It helps reduce repetition, keeps the code cleaner, and makes programs easier to manage.

One small thing: in your code,

"You are " + age + "years old"

will print:

You are 22years old

because there is no space before "years".

It would be better as:

"You are " + age + " years old"

which prints:

You are 22 years old


### RETURN STATEMENTS IN C#


using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // return = returns data back to the place where a method is invoked 

            double x;
            double y;
            double result;

            Console.WriteLine("Enter your first number: ");
            x = Convert.ToDouble(Console.ReadLine());

            Console.WriteLine("Enter your second number: ");
            y = Convert.ToDouble(Console.ReadLine());

            result = Multiply(x, y);

            Console.WriteLine(result);

            Console.ReadKey();
            Console.Beep();
        }
        static double Multiply(double x, double y)
        {
            double z = x * y;
            return z;

        }
           
          
            
          
    }
}

# EXPLANATION: 
                Return

When we learned methods, we created methods that performed a task.

For example:

happybirthdaysong(name, age);

The method would run some code and print the birthday song.

After finishing, it would simply return control back to Main().

But what if we want the method to calculate something and give us the answer back?

That is where return comes in.

A return statement sends data from a method back to the place where the method was called.

Getting Input

First, the program asks the user for two numbers.

Console.WriteLine("Enter your first number: ");
x = Convert.ToDouble(Console.ReadLine());

Console.WriteLine("Enter your second number: ");
y = Convert.ToDouble(Console.ReadLine());

Suppose the user enters:

5
10

Now:

x = 5
y = 10
Calling the Method

Next, we call:

result = Multiply(x, y);

At this point the program says:

"Go to the Multiply() method, give it the values of x and y, and bring me back the answer."

So the program temporarily jumps to:

static double Multiply(double x, double y)
Inside the Method

Inside the method:

double z = x * y;

Since:

x = 5
y = 10

the calculation becomes:

z = 5 * 10
z = 50
Return Statement

Now we reach:

return z;

This means:

"Take the value stored in z and send it back to wherever this method was called."

So:

return 50;

is effectively what happens.

The method finishes its work and sends 50 back to:

result = Multiply(x, y);

which becomes:

result = 50;
Displaying the Result

Now:

Console.WriteLine(result);

prints:

50

to the console.

Why double Instead of void?

Earlier you learned:

static void happybirthdaysong(...)

void means:

This method performs a task but does not give any value back.

In this program:

static double Multiply(double x, double y)

double means:

This method must return a value of type double.

That's why:

return z;

is required.

Without it, the program would give an error.


### PARAMS KEYWORD IN C#

using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* prams keyword = a method that takes variable number of arguments.
             *                 the parameter type must be a single - dimensional array
             *                 */

            double total = Checkout(30, 22.35, 569);

            Console.WriteLine(total);
            
            Console.ReadKey();
            Console.Beep();
        }
        static double Checkout(params double[] prices)
        {
            double total = 0;
            
            foreach(double price in prices)
            {
                total += price;
            }
            return total;
            

        }
      
           
          
            
          
    }
}
