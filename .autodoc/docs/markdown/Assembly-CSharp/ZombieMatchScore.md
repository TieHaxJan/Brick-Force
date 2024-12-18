[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\ZombieMatchScore.cs)

The code provided is a script for managing and displaying the score and progress of a zombie-themed game mode in the larger Brick-Force project. 

The `ZombieMatchScore` class extends the `MonoBehaviour` class from the Unity engine, indicating that it is a script that can be attached to a game object in the Unity editor. 

The script contains several public variables that can be set in the Unity editor, including `guiDepth`, `curFont`, `totalFont`, `scoreBg`, `gaugeBg`, `gauge`, `humanIcon`, `zombieIcon`, and `arrow`. These variables represent various textures and fonts used for displaying the score and progress.

The script also contains several private variables, such as `cur` and `total`, which represent the current and total score, and `size`, `crdCurrent`, `crdTotal`, `sizeZH`, and `offsetZH`, which represent the size and coordinates of various UI elements.

The `Start` method is called when the script is first initialized. It sets the initial value of `cur` to 1 and `total` to the kill count obtained from the `RoomManager` instance. If the player is in "Breaking Into" mode, it sends a request to the server to retrieve the zombie mode score.

The `Update` method is empty and does not contain any code.

The `DrawRounding` method is responsible for drawing the score UI elements. It uses the `GUI` class from Unity to draw a background texture (`scoreBg`) and the current and total scores using the `curFont` and `totalFont` fonts, respectively.

The `DrawZombieVsHuman` method is responsible for drawing the progress of the zombie vs human game mode. It uses the `ZombieVsHumanManager` instance to retrieve the human and zombie ratios and counts. It then uses the `TextureUtil` and `LabelUtil` classes to draw the UI elements, including icons, gauges, arrows, and text labels.

The `OnGUI` method is called by Unity to draw the GUI elements. It sets the GUI skin, depth, and enabled state based on the game state and whether a modal dialog is open. It then calls the `DrawRounding` and `DrawZombieVsHuman` methods to draw the score and progress UI elements.

The `OnZombieScore` method is called when the server sends an updated zombie score. It updates the `cur` and `total` variables and adjusts the scale of the fonts if necessary.

In summary, this script manages and displays the score and progress of a zombie-themed game mode in the Brick-Force project. It uses various textures, fonts, and UI elements to draw the score and progress on the screen. The `Start` method initializes the score values and sends a request to the server if necessary. The `Update` method is empty. The `DrawRounding` and `DrawZombieVsHuman` methods are responsible for drawing the score and progress UI elements. The `OnGUI` method is called by Unity to draw the GUI elements. The `OnZombieScore` method is called when the server sends an updated zombie score.
## Questions: 
 1. What is the purpose of the `ZombieMatchScore` class?
- The `ZombieMatchScore` class is responsible for displaying the score and other UI elements related to a zombie match in the game.

2. What are the `cur` and `total` variables used for?
- The `cur` variable represents the current score in the zombie match, while the `total` variable represents the total score.

3. What is the purpose of the `DrawZombieVsHuman` method?
- The `DrawZombieVsHuman` method is responsible for drawing the UI elements related to the zombie vs human ratio and count in the game.