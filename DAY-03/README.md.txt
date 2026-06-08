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