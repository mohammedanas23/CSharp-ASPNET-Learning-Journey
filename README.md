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

### DAY 2 / 07-06-2026

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
 