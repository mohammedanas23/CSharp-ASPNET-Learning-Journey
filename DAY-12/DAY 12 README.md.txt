### List : 

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;
using System.Collections.Generic;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // List = data structure that represents a list of objects that can be accessed by an index
            //        similar to an array, but it can dynamically decrease / increase in size
            //        System.Collections.Generic;

            List<string> food = new List<string>();

            food.Add("Biryani");
            food.Add("Pizza");
            food.Add("Burger");
            food.Add("Steak");


            string[] foodArray = food.ToArray();

            foreach (string item in foodArray)
            {
                Console.WriteLine(item);

            }


            Console.ReadKey();
            Console.Beep();
        }
    } 
    
}

# Explanation : 
First we create a List called food that can store string values. A List is similar to an array, but unlike an array, it can grow and shrink dynamically, so we don't have to decide its size beforehand.

Then we use the Add() method to insert four food items into the List:

Biryani
Pizza
Burger
Steak

After that, we use the ToArray() method to convert the List into a string array and store it inside foodArray.

Then we use a foreach loop to go through every item in the array one by one.

During each iteration, the current item is temporarily stored in the variable item, and Console.WriteLine(item) prints that item on the screen.

So the loop prints:

Biryani
Pizza
Burger
Steak

Finally, Console.ReadKey() waits for the user to press a key before the program closes, and Console.Beep() makes a beep sound.

The part that tells me you're understanding the code is not saying:

"ToArray() converts a List into an array."

Anybody can memorize that.

The deeper explanation is:

"We first stored the data in a List because it can grow dynamically. Once we were done adding items, we converted it into an array and then printed each item using a foreach loop."

That's the kind of explanation interviewers like because it focuses on why the code is doing something, not just what the method is called.

One small challenge:

You converted the List into an array:

string[] foodArray = food.ToArray();

But the program only prints the items.

----------------------------------------------------------------
### List of objects :

using System.ComponentModel.Design;
using System.Numerics;
using System.Threading.Channels;
using System.Collections.Generic;

namespace Programpractice
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // List of objects

            List<Player> players = new List<Player>();


            players.Add(new Player("Affan"));
            players.Add(new Player("Kareem"));
            players.Add(new Player("Sattar"));


            foreach (Player player in players)
            {
                Console.WriteLine(player);
            }

            Console.ReadKey();
            Console.Beep();
        }
    }
    class Player
    {
        public string username;

        public Player(string username)
        {
            this.username = username;

        }
        public override string ToString()
        {
            return username;
        }
    }
}

# Explanation : 
First we create a List called players that can store objects of type Player. Unlike the previous example where the List stored strings, this List stores complete Player objects.

Then we create three Player objects using the constructor:

new Player("Affan")
new Player("Kareem")
new Player("Sattar")

and immediately add them into the List using the Add() method.

When a Player object is created, the constructor runs:

public Player(string username)
{
    this.username = username;
}

The value passed into the constructor gets stored inside the object's username field.

So after adding all three players, the List contains:

Player object with username = Affan
Player object with username = Kareem
Player object with username = Sattar

Then we use a foreach loop to go through each Player object in the List one by one.

During each iteration, the current Player object is temporarily stored in the variable player.

foreach(Player player in players)

Then:

Console.WriteLine(player);

prints the current Player object.

Normally, printing an object would display something like:

Programpractice.Player

But we overrode the ToString() method:

public override string ToString()
{
    return username;
}

So whenever the object is printed, C# automatically calls ToString() and returns the player's username instead.

Therefore the output becomes:

Affan
Kareem
Sattar

Finally, Console.ReadKey() waits for a key press and Console.Beep() makes a beep sound before the program ends.

What I really like is that a few weeks ago you probably would have said:

"It creates a list and prints the names."

