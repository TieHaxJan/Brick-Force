[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\SpectatorSwitch.cs)

The code provided is a script called "SpectatorSwitch" that is part of the larger Brick-Force project. This script is responsible for managing the spectator mode in the game. 

The script contains several variables and references to other classes and objects. Here is a breakdown of the important elements:

- `guiDepth`: A variable that determines the depth of the GUI elements in the game.
- `fpCam`: A reference to the first-person camera object.
- `clrOutline` and `clrText`: Variables that store the colors for the outline and text of the spectator UI.
- `curMode`: A variable that stores the current control mode of the player.
- `target`: A reference to the current target player that the spectator is observing.
- `localController` and `spectatorController`: References to the local and spectator controllers.
- `deactivatedWeapons`: An array of references to deactivated weapons.
- `deltaTime`: A variable that keeps track of the time since the last update.

The script contains several methods that handle different aspects of the spectator mode:

- `Start()`: This method is empty and does not contain any code.
- `OnGUI()`: This method is responsible for rendering the spectator UI on the screen. It checks if the GUI is enabled and if the BrickManager is loaded. If these conditions are met, it retrieves the GUI skin and sets the GUI depth. It then displays the target player's nickname on the screen using two different labels with different colors.
- `OnRemoveBrickMan(GameObject obj)`: This method is called when a brick man (player) is removed from the game. If the removed player is the current target, it disables the ghost switch component and sets the target to the next player. If there are no more players, it sets the parent of the script's transform to null.
- `VerifyLocalController()`: This method checks if the local controller is null and retrieves it if it is.
- `VerifySpectatorController()`: This method checks if the spectator controller is null and retrieves it if it is.
- `Update()`: This method is called every frame and handles various tasks related to the spectator mode. It checks if there is a target player and if the jump button is pressed or if the current target player is null or hidden. If any of these conditions are met, it sets the target to the next player. It also checks if the control mode has changed and calls the `ModeChange()` method accordingly. It then verifies the local and spectator controllers and updates the delta time. Finally, it sends a spectator command and logs the camera usage if the control mode is set to spectator mode.
- `LookFriendlyOnly()`: This method returns a boolean value based on whether the control mode is spectator mode or not.
- `VerifyTarget()`: This method is responsible for verifying the target player. If the player is a spectator and the target is null, it sets the target to a random player. If the target is not null, it checks if the target player is valid and sets the target to null if it is not.
- `ModeChangeBruteforcely(MyInfoManager.CONTROL_MODE controlMode)`: This method changes the control mode forcefully and calls the `ModeChange()` method.
- `ModeChange()`: This method handles the mode change logic. If the local controller, first-person camera, and spectator controller are not null, it checks the current control mode. If the control mode is spectator mode or playing spectator, it disables the local controller, deactivates the weapons, hides the first-person camera, and enables the spectator controller. If the control mode is not spectator mode, it enables the local controller, activates the weapons, shows the first-person camera, disables the spectator controller, and resets the target and parent.

In summary, this script manages the spectator mode in the game. It handles UI rendering, target player selection, control mode changes, and enables/disables relevant components based on the control mode.
## Questions: 
 1. What is the purpose of the `OnGUI` method?
- The `OnGUI` method is responsible for rendering the spectator UI elements on the screen when the GUI is enabled and the BrickManager is loaded.

2. What does the `VerifyTarget` method do?
- The `VerifyTarget` method checks if the current target of the spectator is still valid. If the target is null or the target's status is not 4, the target is set to null.

3. What is the purpose of the `ModeChange` method?
- The `ModeChange` method is called when the control mode of the spectator changes. It enables or disables the necessary components and weapons based on the new control mode.