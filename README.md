<h1>Spooky House Escape - Advanced Python Game</h1>
<h2>This version adds: </h2>
✅ More random events<br>
✅ Inventory system (player can collect and use items)<br>
✅ Loops (to let players try again)<br>
✅ Functions (to organize the code)<br>

<br>Step 1: Import Modules
At the top of your file, import random for random events.
import random

<br>Step 2: Create a List of Spooky Sounds
We use this to make the game unpredictable.
scary_sounds = ["a creaky door", "a whisper", "a loud bang", "footsteps behind you"]

<br>Step 3: Define the Game Function
Wrap the game logic inside a function so the player can restart easily.
def play_game():
    inventory = []  # Store collected items

    print("\n🎃 Welcome to the Spooky House! 🎃")
    print("You enter a spooky house. It's dark and silent... except for", random.choice(scary_sounds))
    print("You see two doors: one RED and one BLUE.")

    choice1 = input("Which door do you choose? (red/blue) ").lower()

    if choice1 == "red":
        print("\nThe red door creaks open... You see a dusty staircase or a dark hallway.")
        choice2 = input("Do you go UP the stairs or into the HALLWAY? (up/hallway) ").lower()

        if choice2 == "up":
            print("\nYou reach the attic and find a window. But it's locked! You need a key.")
            if "key" in inventory:
                print("You use the key to open the window and escape! 🎉")
            else:
                print("You don’t have the key. A ghost appears... GAME OVER! 👻")
        else:
            print("\nThe hallway leads to an old table with a key on it.")
            inventory.append("key")
            print("You take the key. But suddenly, the lights go out! 👻")
            print("Try again and use the key next time!")
    
    elif choice1 == "blue":
        print("\nThe blue door leads to a basement. It's cold and smells old.")
        choice2 = input("Do you check the SHELVES or look behind the CURTAIN? (shelves/curtain) ").lower()

        if choice2 == "shelves":
            print("\nYou find a flashlight and a secret passage!")
            print("You use the passage and escape! 🎉")
        else:
            print("\nA ghost appears and traps you forever! GAME OVER! 👻")
    
    else:
        print("\nYou stand frozen in fear... Something grabs you! GAME OVER! 👻")

    restart = input("\nDo you want to play again? (yes/no) ").lower()
    if restart == "yes":
        play_game()

# Start the game
play_game()


Step 5: Challenge Students
I encourage you to improve the game by:<br>
🎃 Adding more rooms and choices<br>
👻 Creating random ghost encounters<br>
🗝️ Making an inventory system with multiple items<br>
🎲 Using random events for different outcomes<br>
