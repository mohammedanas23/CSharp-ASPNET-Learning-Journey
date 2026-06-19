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






                        