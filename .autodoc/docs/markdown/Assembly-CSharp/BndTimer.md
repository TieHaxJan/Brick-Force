[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\BndTimer.cs)

The `BndTimer` class is a script that manages the countdown timer for the game phases in the Brick-Force project. It is responsible for displaying the timer on the screen, updating the timer, and shifting between the build and battle phases.

The class has several private variables that store information about the timer and its appearance, such as the GUI depth, the position and size of the timer rectangle, the background texture, and references to other components like the radar and local controller.

The class also has public properties and methods that allow other classes to access and modify the timer properties. For example, the `IsBuildPhase` property allows other classes to check if the current phase is the build phase or the battle phase. The `RemainRepeat` property returns the number of times the timer will repeat.

The class has several static methods that are used to pack and unpack the timer options. The `PackTimerOption` method takes the build phase time, battle phase time, and repeat count as input and returns a packed integer value. The `BuildPhaseTime` and `BattlePhaseTime` methods extract the build and battle phase times from the packed timer option. The `Repeat` method extracts the repeat count from the packed timer option.

The `ResetTimer` method is used to reset the timer based on the current phase and time limit. It sets the remaining time to the build phase time if the current phase is the battle phase, and vice versa.

The `ShiftPhase` method is used to shift between the build and battle phases. It decreases the repeat count if shifting to the build phase, and updates the remaining time based on the new phase and time limit.

The `Start` method is called when the script is initialized. It initializes the radar, sets the initial phase to the build phase, and sets the remaining time and repeat count based on the time limit.

The `VerifyRadar` method is used to check if the radar component is available and assigns it if it is not.

The `OnGUI` method is responsible for drawing the timer on the screen. It uses the GUI functions provided by Unity to draw the timer background and the remaining time text.

The `Update` method is called every frame and updates the timer. It checks if the local player is the master player, if the local player is controllable, and if the brick manager is loaded. If all conditions are met, it updates the timer by decreasing the remaining time, sending network messages, and shifting phases if necessary.

The `OnPlayTime` and `OnTimer` methods are event handlers that are called when the play time and remaining time are received from the network. They update the play time and remaining time if the received values are greater or smaller than the current values, respectively.

In summary, the `BndTimer` class manages the countdown timer for the game phases in the Brick-Force project. It handles the display, update, and shifting of the timer between the build and battle phases. Other classes can access and modify the timer properties through public properties and methods.
## Questions: 
 1. What is the purpose of the `BndTimer` class?
- The `BndTimer` class is responsible for managing the timer functionality in the game.

2. What is the significance of the `isBuildPhase` variable?
- The `isBuildPhase` variable determines whether the game is currently in the build phase or the battle phase.

3. What is the purpose of the `ShiftPhase` method?
- The `ShiftPhase` method is used to shift the game phase between the build phase and the battle phase.