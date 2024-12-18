[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\BattleTutor.cs)

The `BattleTutor` class is a script that is part of the larger Brick-Force project. This script is responsible for managing the tutorial mode in the game. 

The `Start()` method is called when the script is first initialized. It sets up various global variables and initializes the tutorial map. It also finds the `TutoInput` component attached to the "Main" game object.

The `InitializeFirstPerson()` method is called to initialize the first-person perspective for the player. It sets up the usable items for the player and spawns the player character at the appropriate location.

The `OnDisable()` method is called when the script is disabled. It checks if the game is still loading a level and performs cleanup tasks such as clearing the brick manager, disabling the palette manager, and resetting certain global variables.

The `OnGUI()` method is responsible for rendering the graphical user interface (GUI) elements for the tutorial mode. It displays a help box with a specific text and an icon. It also calls the `drawInputs()` method of the `TutoInput` component to render any tutorial-specific input prompts.

The `Update()` method is called every frame. It updates the state of the game, checks for user input, and performs various actions. It locks the cursor to the screen if certain conditions are met. It also checks if the tutorial map has been loaded and initializes the first-person perspective if it hasn't been done already. It also checks for button presses to open the main menu or the help window.

The `OnNoticeCenter()` method is a callback method that is called when a notice is received from the game's notice center. It adds the received message to the system inform instance.

Overall, this script manages the tutorial mode in the game by setting up the tutorial map, initializing the player character, rendering the tutorial GUI elements, and handling user input. It is an essential part of the Brick-Force project as it provides a guided learning experience for new players.
## Questions: 
 1. What is the purpose of the `InitializeFirstPerson()` method?
- The `InitializeFirstPerson()` method is responsible for initializing the first-person perspective of the player character, including equipping usable items and spawning the character in the game world.

2. What does the `OnGUI()` method do?
- The `OnGUI()` method is responsible for rendering the graphical user interface (GUI) elements on the screen, including a help box and an icon.

3. What is the purpose of the `OnNoticeCenter()` method?
- The `OnNoticeCenter()` method is called when a notice is received from the game's notice center, and it adds the received message to the system inform message center.