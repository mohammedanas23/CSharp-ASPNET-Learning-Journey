### execptions+:

using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* exception = error that occurs during execution.
             * 
             * try     = try some code that is considered "dangerious".
             * catch   = catches and handles exceptions when they occur.
             * finally = always executes regardless if exception is caught or not.
             */

            double x;
            double y;
            double result;

            try
            {
                Console.WriteLine("Enter your first number: ");
                x = Convert.ToInt32(Console.ReadLine());

                Console.WriteLine("Enter your second number: ");
                y = Convert.ToInt32(Console.ReadLine());

                result = x / y;

                Console.WriteLine("result " + result);

            }
            catch (FormatException e)
            {
                Console.WriteLine("ENTER ONLY NUMBERS PLEASE");
            }
            catch (DivideByZeroException)
            {
                Console.WriteLine("You can't divide a number by zero!!!");
            }
            catch(Exception e)
            {
                Console.WriteLine("Something went wrong");
            }
            finally
            {
                Console.WriteLine("Thanks visit again!");
            }


            
            
            Console.ReadKey();
            Console.Beep();
        }
        
      
           
          
            
          
    }
}


### Conditional Statements :
using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* Conditional statements = used on conditional assignment if a condition is true / false
             * 
             * (condition) ? x : y */

            double temperature = 20;
            string message;

            if (temperature >= 15)
            {
                message = "It's warm outside!!!";
            }
            else
            {
                message = "It's cold outside!!!";
            }
            Console.WriteLine(message);


            
            
            Console.ReadKey();
            Console.Beep();
        }
        
      
           
          
            
          
    }
}

# Explanation : 
                this is one way to write the code but in conditional statements we usually dont write it that way, we just give a certain condition and then
                we execute the line 

                using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* Conditional statements = used on conditional assignment if a condition is true / false
             * 
             * (condition) ? x : y */

            double temperature = 02;

            Console.WriteLine((temperature >= 15) ? "It's warm outside" : "It's cold outside ");

            
            
            Console.ReadKey();
            Console.Beep();
        }
        
      
           
          
            
          
    }
}

this is how we use the conditional statement.


### String Interpolation: 

using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* string interpolation = allows us to insert variables into a string literal
             *                        precede a string literal with a $ sign
             *                        {} are placeholders 
             *                        */

            string Firstname = "Mohammed";
            string Lastname = "Anas";
            int age = 21;

            Console.WriteLine($"Hello {Firstname} {Lastname}. ");
            Console.WriteLine($"You are {age,1} years old ");
           

            
            
            Console.ReadKey();
            Console.Beep();
        }
        
      
           
          
            
          
    }
}


### Object in C# : 

using System.ComponentModel.Design;
using System.Numerics;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /* objects = an instanse of a class 
             *           A class can be used as a blue print to create Objects (OOP)
             *           Objects can have fields and methods (characteristics and actions)
             *           */

            Human human1 = new Human();

            human1.name = "Roman";
            human1.age = 95;

            human1.eat();
            human1.sleep();

            
            
            Console.ReadKey();
            Console.Beep();
        }
    }
    class Human
    {
        public String name;
        public int age;

        public void eat()
        {
            Console.WriteLine(name + "is eating");
        }
        public void sleep()
        {
            Console.WriteLine(name + "is sleeping");
        }
    }
}
