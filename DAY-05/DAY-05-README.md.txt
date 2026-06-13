### DAY 05

### SWITCHES

Switch = An efficient alternative to many if else statements.

using System.ComponentModel.Design;
using System.Formats.Asn1;
using System.Threading.Channels;

                                namespace Projectpractice
                                {
                                    internal class Program
                                    {
                                    
                                        
                                        static void Main(string[] args)
                                        {
                                            // if statements = a basic form of dision making 

                                            Console.WriteLine("What is the day today? : ");
                                            string day = Console.ReadLine();

                                            if (day == "Monday")
                                            {
                                                Console.WriteLine("Today is Monday");
                                            }
                                            else if (day == "Tuesday")
                                            {
                                                Console.WriteLine("Today is tuesday");
                                            }
                                            else if (day == "Wednesday")
                                            {
                                                Console.WriteLine("Today is wednesday");
                                            }
                                            else if (day == "Thrusday")
                                            {
                                                Console.WriteLine("Today is thrusday");
                                            }
                                            else if (day == "Friday")
                                            {
                                                Console.WriteLine("Today is friday");
                                            }
                                            else if (day == "Saturday")
                                            {
                                                Console.WriteLine("Today is saturday");
                                            }
                                            else if (day == "Sunday")
                                            {
                                                Console.WriteLine("Today is sunday");
                                            }
                                            else
                                            {
                                                Console.WriteLine(day + "this is not a day");
                                            }
                                            Console.ReadLine();
                                            Console.Beep();



                                                Console.ReadKey();
                                            }
                                        }
                                    }

# EXPLANATION :
                In this program I wrote if else statement but this is way too long to use and very time consuming, rather you can just 'switches' insted of writing this whole line code.


                                        namespace Programpractice
                                        {
                                            internal class Program
                                            {
                                                static void Main(string[] args)
                                                {
                                                    Console.WriteLine("What day is today? : ");
                                                    string day = Console.ReadLine();

                                                    switch(day)
                                                    {
                                                        case "Monday":
                                                            Console.WriteLine("Today is Monday");
                                                            break;
                                                        case "Tuesday":
                                                            Console.WriteLine("Today is Tuesday");
                                                            break;
                                                        case "Wednesday":
                                                            Console.WriteLine("Today is Wednesday");
                                                            break;
                                                        case "Thursday":
                                                            Console.WriteLine("Today is Thursday");
                                                            break;
                                                        case "Friday":
                                                            Console.WriteLine("Today is Friday");
                                                            break;
                                                        case "Saturday":
                                                            Console.WriteLine("Today is Saturday");
                                                            break;
                                                        case "Sunday":
                                                            Console.WriteLine("Today is Sunday");
                                                            break;
                                                        default:
                                                            Console.WriteLine("Invalid input. Please enter a valid day of the week.");
                                                            break;
                                                    }

                                                    Console.Beep();
                                                    Console.ReadKey();
                                                }
                                            }
                                        }

# EXPLANATION : 
                This here is more clean although this is also a long code but it is clean and very useful way, and by the way we are here to learn new thing right so this is how you use switches.



### LOGICAL OPERATORS 

Can be used to check if more than 1 condition is true/false

                                    namespace Programpractice
                                    {
                                        internal class Program
                                        {
                                            static void Main(string[] args)
                                            {
                                                // logical operators = used to determine the logic between variables or values \
                                                //                     can be used to check if more than 1 condition is true or false
                                                //                     && = and
                                                //                     || = or

                                                Console.WriteLine("What is the temperature outside: ");
                                                double temp = Convert.ToDouble(Console.ReadLine());

                                                if (temp >= 10 && temp <= 25)
                                                {
                                                    Console.WriteLine("It's warm outside!");
                                                }
                                                else if (temp <= -50 || temp >= 50)
                                                {
                                                    Console.WriteLine("DO NOT GO OUTSIDE!!!");
                                                }

                                                Console.Beep();
                                                Console.ReadKey();
                                            }
                                        }
                                    }



### WHILE LOOPS 


                                    namespace Programpractice
                                    {
                                        internal class Program
                                        {
                                            static void Main(string[] args)
                                            {
                                                // while loop = repeats a block of code while a specified condition is true 

                                                string name = "";

                                                while (name == "") 
                                                {
                                                    Console.WriteLine("Enter your name: ");
                                                    name = Console.ReadLine();
                                                }
                                                Console.WriteLine("Hello " + name );


                                                Console.Beep();
                                                Console.ReadKey();
                                            }
                                        }
                                    }



### FOR LOOPS :

                                    namespace Programpractice
                                    {
                                        internal class Program
                                        {
                                            static void Main(string[] args)
                                            {
                                                // for loop = repeats some code a FINITE amount of times 
                                                /*
                                                for (int i = 1; i < 10; i++)
                                                {
                                                    Console.WriteLine(i);
                                                }
                                                */

                                                for (int i = 10; i > 0; i--)
                                                {
                                                    Console.WriteLine(i);
                                                }
                                                Console.WriteLine("HPpY NEW YEAR!!!");

                                                Console.Beep();
                                                Console.ReadKey();
                                            }
                                        }
                                    }


### NESTED LOOPS:


                                        namespace Programpractice
                                        {
                                            internal class Program
                                            {
                                                static void Main(string[] args)
                                                {
                                                    // nested loops = loops inside of other loops 
                                                    //                Uses vary. used a lot in sorting algorithms 

                                                    Console.Write("How many rows: ");
                                                    int rows = Convert.ToInt32(Console.ReadLine());

                                                    Console.Write("How many columns: ");
                                                    int columns = Convert.ToInt32(Console.ReadLine());

                                                    Console.Write("What symbol: ");
                                                    string symbol = Console.ReadLine();

                                                    for (int i = 0; i < rows; i++)
                                                    {
                                                        for (int j = 0; j < columns; j++)
                                                        {
                                                            Console.Write(symbol);
                                                        }
                                                        Console.WriteLine();
                                                    }
                                                
                                                    Console.Beep();
                                                    Console.ReadKey();
                                                }
                                            }
                                        }



### NUMBER GUESSING GAME MINI PROJECT:

                                    namespace Programpractice
                                    {
                                        internal class Program
                                        {
                                            static void Main(string[] args)
                                            {
                                                // number guessing game

                                                Random random = new Random();
                                                bool playagain = true;
                                                int min = 1;
                                                int max = 500;
                                                int guess;
                                                int number;
                                                int guesses;
                                                string response;

                                                while (playagain)
                                                {
                                                    guess = 0;
                                                    guesses = 0;
                                                    response = "";
                                                    number = random.Next(min, max + 1);

                                                    while (guess != number && guesses < 10)
                                                    {
                                                        Console.WriteLine("Guess the number between " + min + " - " + max + " : ");
                                                        guess = Convert.ToInt32(Console.ReadLine());
                                                        Console.WriteLine("Guess: " + guess);

                                                        if (guess > number + 20)
                                                        {
                                                            Console.WriteLine("Way too high");
                                                        }
                                                        else if (guess > number)
                                                        {
                                                            Console.WriteLine(guess + " is too high");

                                                        }
                                                        else if (guess < number)
                                                        {
                                                            Console.WriteLine(guess + " is too low");
                                                        }
                                                        guesses++;
                                                    }
                                                    if (guess == number)
                                                    {
                                                        Console.WriteLine("Number: " + number);
                                                        Console.WriteLine("YOU WIN THE GAME!!!");
                                                        Console.WriteLine("Guesses: " + guesses);
                                                    }
                                                    else
                                                    {
                                                        Console.WriteLine("You ran out of guesses!");
                                                        Console.WriteLine("The actual number was " + number);
                                                    }
                                                    Console.WriteLine("Would you like to play again: (Y/N) ");
                                                    response = Console.ReadLine();
                                                    response = response.ToUpper();

                                                    playagain = (response == "Y");
                                                }
                                            
                                                Console.Beep();
                                                Console.ReadKey();
                                            }
                                        }
                                    }


# EXPLANATION :
                # Number Guessing Game - Code Explanation

                ## Creating the Random Number Generator

                ```csharp
                Random random = new Random();
                ```

                The first `Random` is the type (class), and the second `random` is the variable name. `new Random()` creates a new random number generator object and stores it in the variable `random`. This object is later used to generate a random number for the game.

                ---

                ## Declaring Variables

                ```csharp
                bool playagain = true;
                int min = 1;
                int max = 100;
                int guess;
                int number;
                int guesses;
                string response;
                ```

                These variables are used throughout the game:

                * `playagain` controls whether the player wants to play another round.
                * `min` stores the minimum possible number (1).
                * `max` stores the maximum possible number (100).
                * `guess` stores the player's current guess.
                * `number` stores the secret random number generated by the computer.
                * `guesses` keeps track of how many attempts the player has made.
                * `response` stores the player's answer when asked if they want to play again.

                ---

                ## Starting the Game Loop

                ```csharp
                while (playagain)
                ```

                This loop keeps the game running as long as `playagain` is `true`. Each time the player chooses to play again, the loop starts a new round.

                Before the round begins, several variables are reset:

                ```csharp
                guess = 0;
                guesses = 0;
                response = "";
                ```

                This ensures that each new game starts with fresh values.

                ---

                ## Generating the Secret Number

                ```csharp
                number = random.Next(min, max + 1);
                ```

                This generates a random number between the minimum and maximum values. Since `Random.Next()` excludes the upper limit, `max + 1` is used so that 100 can also be selected.

                ---

                ## The Guessing Loop

                ```csharp
                while (guess != number)
                ```

                This is a nested loop. It continues running until the player's guess matches the secret number.

                The player is asked to enter a number:

                ```csharp
                guess = Convert.ToInt32(Console.ReadLine());
                ```

                `Console.ReadLine()` reads input as text (a string), so `Convert.ToInt32()` converts it into an integer.

                ---

                ## Checking the Guess

                If the player's guess is higher than the secret number:

                ```csharp
                if (guess > number)
                {
                    Console.WriteLine(guess + " is too high");
                }
                ```

                The program tells the player that the guess is too high.

                If the player's guess is lower than the secret number:

                ```csharp
                else if (guess < number)
                {
                    Console.WriteLine(guess + " is too low");
                }
                ```

                The program tells the player that the guess is too low.

                ---

                ## Counting Attempts

                ```csharp
                guesses++;
                ```

                This increases the guess counter by one every time the player makes an attempt. At the end of the game, the program can display how many guesses were required to find the correct number.

                ---

                ## Winning the Game

                When the player's guess matches the secret number, the loop ends and the program displays:

                ```csharp
                Console.WriteLine("YOU WIN THE GAME!!!");
                ```

                It also shows:

                * The correct number.
                * The total number of guesses used.

                ---

                ## Playing Again

                After the game ends, the player is asked whether they want to play another round:

                ```csharp
                response = Console.ReadLine();
                response = response.ToUpper();
                ```

                `ToUpper()` converts the player's input to uppercase. This allows the program to treat `y` and `Y` as the same response, making the game more user-friendly.

                If the player chooses to continue, the outer loop starts another round. Otherwise, the game ends.
 
THANKS 


