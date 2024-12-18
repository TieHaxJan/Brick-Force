[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\IndividualMatchScore.cs)

The code provided is a script called "IndividualMatchScore" that is a part of the Brick-Force project. This script is responsible for displaying the individual match score on the Heads-Up Display (HUD) during gameplay.

The script contains several public variables that can be set in the Unity editor. These variables include the GUI depth, score font, goal font, score background texture, size of the score display, and the coordinates for the score and goal text.

The script also has a private variable called "score" that keeps track of the current score. The score is initially set to 0 in the Start() method.

The Start() method is called when the script is first initialized. In this method, the score is set to 0 and a check is made to see if the player is currently breaking into something. If the player is breaking into something, a request is sent to the server to update the individual score.

The OnIndividualScore() method is called when the individual score is updated. In this method, the score font is scaled to 2 and the score is updated with the new total kill count.

The OnGUI() method is responsible for rendering the score display on the HUD. It first checks if the GUI is enabled in the game settings. If it is enabled, it retrieves the GUI skin and sets the GUI depth. It then begins a GUI group with a rectangle that represents the size and position of the score display. The score background texture is drawn within this group, and the score and goal text are printed using the score and goal fonts at the specified coordinates. Finally, the GUI group is ended and the GUI skin is reset.

The Update() method is empty and does not contain any code.

Overall, this script is an essential part of the Brick-Force project as it handles the display of the individual match score on the HUD during gameplay. It allows players to see their current score and the goal score they need to achieve.
## Questions: 
 1. What is the purpose of the `OnIndividualScore` method?
- The `OnIndividualScore` method is called when the individual score is updated, and it updates the score font and assigns the new score value.

2. What is the purpose of the `Start` method?
- The `Start` method initializes the score variable to 0 and sends a request for the individual score if the player is breaking into something.

3. What is the purpose of the `OnGUI` method?
- The `OnGUI` method is responsible for rendering the graphical user interface (GUI) elements related to the individual match score, including the score background, score font, and goal font.