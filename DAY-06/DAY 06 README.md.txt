### ROCK PAPER SCISSORS GAME:

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Random random = new Random();
            bool playagain = true;
            string player;
            string computer;
            string answer;

            while (playagain)
            {
                player = "";
                computer = "";
                answer = "";

                while(player != "ROCK" && player != "PAPER" && player != "SCISSOERS")
                {
                    Console.WriteLine("Enter ROCK, PAPER OR SCISSORS: ");
                    player = Console.ReadLine();
                    player = player.ToUpper();
                }
                switch(random.Next(1, 4))
                {
                    case 1:
                        computer = "ROCK";
                        break;
                    case 2:
                        computer = "PAPER";
                        break;
                    case 3:
                        computer = "SCISSORS";
                        break;
                }
                Console.WriteLine("Player : " + player);
                Console.WriteLine("Computer: " + computer);

                switch (player)
                {
                    case "ROCK":
                    if (computer == "ROCK")
                        {
                            Console.WriteLine("It's a Draw!");
                        }
                    else if(computer == "PAPER")
                        {
                            Console.WriteLine("You lose!");
                        }
                    else
                        {
                            Console.WriteLine("You Win!");
                        }
                        break;

                    case "PAPER":   
                        if (computer == "ROCK")
                        {
                            Console.WriteLine("You Win!");
                        }
                        else if (computer == "PAPER")
                        {
                            Console.WriteLine("It's a Draw!");
                        }
                        else
                        {
                            Console.WriteLine("You lose!");
                        }
                        break;

                    case "SCISSORS":
                        if (computer == "ROCK")
                        {
                            Console.WriteLine("You lose!");
                        }
                        else if (computer == "PAPER")
                        {
                            Console.WriteLine("You Win!!");
                        }
                        else
                        {
                            Console.WriteLine("It's a draw!");
                        }
                        break;
                }

            }
            Console.Write("Would you like to play again (Y/N): ");
            answer = Console.ReadLine();
            answer = answer.ToUpper();

            if(answer == "Y")
            {
                playagain = true;
            }
            else
            {
                playagain = false;
            }

            Console.WriteLine("Thanks for playing");

            Console.ReadKey();
        }    
    }
}
