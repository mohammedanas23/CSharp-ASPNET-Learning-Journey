#  C# / ASP.NET Core Learning Journey

##  Goal
Complete C#, ASP.NET Core, APIs, HTML, CSS, and JavaScript in 8 weeks.

##  Things to learn.
- C#
- .NET
- ASP.NET Core
- REST APIs
- HTML
- CSS
- JavaScript
- SQL Server

---


---

##  Day 01 - C# Basics

### Topics Covered
- What is C#?
- What is .NET?
- Setting up development environment
- First Console Application

### Notes

#### What is .NET?

.NET is a software development platform created by Microsoft. It is a technology or a platform that is used to create multiple types of applications using .NET frameworks and programming languages.

# Types of applications that we can create using .NET 

# Desktop Applications : 
                        Console applications, Windows form applications, WPF (Windows Presentation Foundation)

# Web Applications : 
                    ASP.NET CLASSIC, ASP.NET MVC, ASP.NET CORE MVC

# Mobile Applications :
                        MUI (Multipurprose Application UI) used in every mobile like Android and IOS to create there mobile applications.

# Cloud Applications : 
                        Microsoft Windows Azure... In this cloud applications we can use cloud services like (MWA) Microsoft Windows Azure to create applications, we dont need any other high end device to create the applications... we can just create them using the GPUs of (MWA).

---                         


---

                        
#### What is C#?:
                C# is a programming language developed by Microsoft that runs on the .NET platform. It is Object Oriented Programming Language (OOP) that is most compatible with programming languages under .NET framwork. It provides better security, reusebility of code and easy syntax structure and excellent tooling.



### My first Code in C# 

namespace Projectpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, World!!!");
        }
    }
}

# Explanation: the above code is defined like this 

first the '''namespace''' this says in which project i am working on or on which file i am working on.

2nd the '''internal class Program''' this means that this is a class that can only be accessed using this project only and it is a blue print for creating projects 

3rd '''static void Main(string[] args)''' this is the main line of code i9n our entire code because it will make the code run if i dont write this line of code, it will not work and will give me an error.

4th '''Console.WriteLine ("Hello, World!!!")''' this is the default line to create or print the cofde.


### NOW I WILL SHOW YOU MY 2ND CODE THAT I CREATED IN C# 

namespace Projectpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int a = 10, b = 20, c;
            c = a + b;
            Console.WriteLine(c);
        }    
    }
}

# Explanation:
In this code what I did is that, I took two alphabets and assigned them two integers like 'a = 10' and 'b = 20' and left the 'c' as it is cuz it will have its use in the next line of code 

now i assigned 'c = a + b' i am adding the values that a and b was assigned to c 

now i just have to execute it and i the answer '30' 

---
---
---

### DAY 2 

namespace Projectpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int a = 10, b = 20, c;
            c = a + b;
            Console.WriteLine(c);

            int a = 10, b = 20, c;
            c = a - b;
            Console.WriteLine(c);

            int a = 10, b = 20, c;
            c = a * b;
            Console.WriteLine(c);

            int a = 10, b = 20, c;
            c = a / b;
            Console.WriteLine(c);
        }    
    }
}

# EXPLANATION:
In this code i just defined four different types of calculations like addition, substraction, multiplication, division. But there is a problem in this code each of them have the same exact same number and they all give the answers at the same time there is no freedom of calculation in this code like for example, if i want to add 15 + 15 then i have to delete the multiplication and division and substraction code and just write the addition code in C#... thats a problem.

----------

# 
namespace Projectpractice
{
    internal class Program
    {
        int a = 10, b = 20, c;
        
        void add()
        {
         c = a + b;
         Console.WriteLine(c);
        }

        void sub()
        {
         c = a - b;
         Console.WriteLine(c);
        }

        void mult()
        {
         c = a * b;
         Console.WriteLine(c);    
        }

        void div()
        {
         c = a / b;
         Console.WriteLine(c);
        } 

        static void Main(string[] args)
        {
            Program obj = new Program();
            obj.add();
            obj.sub();
            obj.mul();
            obj.div();


        }    
    }
}

# EXPLANATION:
Here is another one that you can see it gives some freedom but its not practical it will also do the same thing as the other one and will give out the same output.

----------

# CODE 
namespace Projectpractice
{
    internal class Program
    {
        int a, b, c;
        void accept()
        {
            Console.WriteLine("Enter your first number");
            a = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Enter your second number");
            b = Convert.ToInt32(Console.ReadLine());
        }
        void add()
        { 
            c = a + b;
            Console.WriteLine(c);
        }

        void sub()
        {
            c = a - b;
            Console.WriteLine(c);
        }
        void mul()
        {
            c = a * b;
            Console.WriteLine(c);
        }

        void div()
        {
            c = a / b;
            Console.WriteLine(c);
        }

        static void Main(string[] args)
        {
            Program obj = new Program();
            obj.accept();
            obj.add();



        }
    }
}

# EXPLANATION:
Here it ssolves the number game problem for just taking the exact same number like if the user is going to use this he is going to put the numbers of his choice and he would want to take the output he likes right... in this line of cofde it solves the problem, as you can see here i just removed the values that were fixed in the calculations and have given the freedom of choosing the numbers and the calculation type the user wants to do...
'''Console.WriteLine("Enter your first number");
            a = Convert.ToInt32(Console.ReadLine());''' in this line of code i am asking the user to give the number he like as his first number and then i wrote the '''Console.ReadLine();''' but if i just write this line of code i will get an error in the output so what i did before hand was converted the '''Console.ReadLine();''' into integer and then gave it a try and it worked...!!!!


# SIMPLE SI CALCULATOR 

namespace Projectpractice
{
    internal class Program
    {
       
        static void Main(string[] args)
        {
            SI obj = new SI();
            obj.CalcSI();

        }
    }
}

# This is a new one and in this you can only see that there is only the closing statement of the code but i had made a class for this code before 

using System;
using System.Collections.Generic;
using System.Text;

namespace Projectpractice
{
    internal class SI
    {
        float p, r, t, si;
        internal void CalcSI()
        {
            p = 12000;
            r = 2.2F;
            t = 4.5F;
            si = (p * r * t) / 100;
            Console.WriteLine("Result {0}", si);

        }
    }
}

# This is the class i made and i you might me thinking that why did i made a different class when i could do that in the main program, but thats not it... the program on the above is just for me to practice and check if the code build solution is good or has an error in it, but you might also get a question that how did i manage to execute the code if i did this in another window, i used the internal function in this program so that i can access and check and execute the program of the practice file.

----


----

### Variables 
### Constant 
### Literals 

# Variable 

Variable used to contain the data that can be changed dynamically.
Variable are reepredented by data types and identifiers 

# EXAMPLE:

namespace Projectpractice 
{
    internal class Program 
    {
        static void Main(string[] args)
        {
            int age = 20;

            Console.WriteLine(age);

            age = 25; // variable changed 

            Console.WriteLine(age);
        }
    }
}

Here in this example we wrote '''int age = 20'''... then changed it to '25' that the value change hence the uotput is 20 and 25

# Constant 

Constant is the value that cannot be changed after it is assigned. 

# Literals 

Literals is the actual value that is written directly in the code 

example: 
            10        // Integer literal 
            3.14      // Double literal 
            "Hello"   // String Literal 
            True      // Boolean literal

like if we compare the three of these combined we can get a rough idea that how can they be used, for that i am going to make a table 

-------------------------------------------------------------------------------------------------------------------

         Features               Variable                Constant              Literal 

         Has a name                Yes                      Yes                  No

         Stores data               Yes                      Yes                 Represent the values itself 

         Can change                Yes                      No                  Fixed value 

--------------------------------------------------------------------------------------------------------------------

# What are Datatypes in C# ?

A data type tells C# what kind of data a variable can store and how much memory it needs. there is a table for it as well 

--------------------------------------------------------------------------------------------------------------------

        Datatype                            Stores                                                Examples
        
        int                             whole numbers                                          int age = 25;

        Double                          Decimal numbers                                     double price = 99.99;

        Float                      Decimal numbers(less precise)                            float weight = 72.5f;

        char                            Single character                                      char grade = 'A';

        string                              Text                                             string name = "Anas";

        bool                           True / False values                                   bool inStudent = true;

-----------------------------------------------------------------------------------------------------------------------

in this chart 'doubles' datatype and 'float' data type are different because they both give out values in decimals but the precision is less in 'float' data type 

# EXAMPLE: 
            int age = 25;

            double height = 5.10;

            char grade = 'A';

            string name = "Anas";

            bool inStudent = true;


### What is an Identifier ?

An Identifier is simple the name you give to a variable, methods, class, or other program elements

for example:
            int age = 25;

Here the 'age' is the identifier because you need some sort of name or a string or a character that is easily identified 

like 
        string name = "Anas"

This type of naming gives a unique identity. If the name is given like this 

            int 1age;
                                                                            
            int first-name;

            int class;

These types of identifiers is invalid and will give you an error.

---


---

### DAY 03 

# DATA TYPES

            using System.Formats.Asn1;

            namespace Projectpractice
            {
                internal class Program
                {
                
                    static void Main(string[] args)
                    {
                        // Integers 

                        int Anas_Balance = 500;
                        int Misbah_Balance = -200;

                        uint Anas_age = 22;
                        uint Misbah_age = 26;

                        Console.WriteLine("This is not my first code");
                        Console.WriteLine(Anas_Balance);
                        Console.WriteLine(Misbah_Balance);

                        Console.WriteLine("Max value of int {0}", int.MaxValue);
                        Console.WriteLine("Min value of int {0}", int.MinValue);

                        Console.WriteLine("Max value of unit {0}", uint.MaxValue);
                        Console.WriteLine("Min value of uint {0}", uint.MinValue);

                    }
                }
            }


                        This is not my first code
                        500
                        -200
                        Max value of int 2147483647
                        Min value of int -2147483648
                        Max value of unit 4294967295
                        Min value of uint 0

This over here is a complete example of using 'int' and 'uint' and what is the Maximum and Minimum values that can be stored the the function.

As you can see, that first I wrote the 'int' function to write the balance of 'Anas' and 'Misbah' and after that I wrote there ages using 'uint' function, and then I started executing them line by line and as you can also see that I have also give the command in C# that i want the Minimum and Maximum value of both the 'int' and 'uint'. 

And there we have it in the results, the max value that an 'int' function can store in its memory is '2147483647', and the min value that an 'int' function can store in its memory is '-2147483648' it is in the negetive value.

And the same goes for 'uint' function the max value that in can store in its memory is '4294967295', and min value it can store in its memory is '0'.


                        // Fractions 

                        float Anas_height = 5.10f;
                        double Anas_weight = 150.5;
                        decimal Anas_salary = 50000.75m;

                        Console.WriteLine(Anas_height);
                        Console.WriteLine(Anas_weight);
                        Console.WriteLine(Anas_salary);

                        Console.WriteLine("Max value of float is {0}", float.MaxValue);
                        Console.WriteLine("Min value of float is {0}", float.MinValue);

                        Console.WriteLine("Max value of double is {0}", double.MaxValue);
                        Console.WriteLine("Min value of double is {0}", double.MinValue);

                        Console.WriteLine("Max value of decimal is {0}", decimal.MaxValue);
                        Console.WriteLine("Min value of decimal is {0}", decimal.MinValue);

                        5.1
                        150.5
                        50000.75
                        Max value of float is 3.4028235E+38
                        Min value of float is -3.4028235E+38
                        Max value of double is 1.7976931348623157E+308
                        Min value of double is -1.7976931348623157E+308
                        Max value of decimal is 79228162514264337593543950335
                        Min value of decimal is -79228162514264337593543950335 


                        