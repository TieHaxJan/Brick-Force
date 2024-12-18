[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\RadioMenu.cs)

The `RadioMenu` class is a script that handles the radio communication functionality in the larger Brick-Force project. It is responsible for managing the different radio modes (ASK, CMD, REPLY), handling user input for sending radio messages, and playing corresponding audio clips.

The class has several public and private variables. The `guiDepth` variable determines the layer at which the radio menu GUI will be displayed. The `radioAskKeys`, `radioCmdKeys`, and `radioReplyKeys` arrays store the keys for the different radio messages in each mode. The `radioCancelKey` stores the key for canceling the radio menu. The `sndRadioAsks`, `sndRadioCmds`, and `sndRadioReplys` arrays store the names of the audio clips that will be played when a radio message is sent. The `offset` variable determines the vertical spacing between radio messages in the GUI. The `battleChat` variable is a reference to the `BattleChat` component, which handles the chat functionality in the game. The `audioSource` variable is a reference to the `AudioSource` component, which is responsible for playing audio clips. The `localController` variable is a reference to the `LocalController` component, which controls the player's character.

The `Start` method is called when the script is initialized. It retrieves references to the `BattleChat`, `AudioSource`, and `LocalController` components. The `CheckShortcut` method is called in the `Update` method to check if a radio message shortcut key has been pressed. If a shortcut key is pressed, it sends a radio message using the `CSNetManager` class.

The `GetString` method takes a `RadioSignal` object as a parameter and returns the corresponding string message based on the signal's category and message index. The `OnRadioMsg` method is called when a radio message is received. It checks if the sender is the player's character and sets the radio mode to NONE if it is. Otherwise, it retrieves the corresponding audio clip name based on the signal's category and message index and plays the audio clip using the `VoiceManager` class.

The `GetHeight` method calculates the height of the radio menu GUI based on the current radio mode. The `OnGUI` method is responsible for drawing the radio menu GUI using the Unity GUI system. It displays the radio messages and their corresponding shortcut keys in a box on the screen.

The `CheckOnOff` method checks if the radio sound mute button has been pressed and toggles the radio sound mute setting accordingly. The `Update` method is called every frame and handles user input for activating the different radio modes and checking for shortcut key presses.

In summary, the `RadioMenu` class manages the radio communication functionality in the Brick-Force project. It handles user input for sending radio messages, plays corresponding audio clips, and displays the radio menu GUI on the screen.
## Questions: 
 1. What is the purpose of the `RadioMenu` class?
- The `RadioMenu` class is responsible for managing radio communication in the game. It allows players to send and receive radio messages.

2. What are the different modes of the `RadioMenu` class?
- The `RadioMenu` class has three modes: `ASK`, `CMD`, and `REPLY`. These modes determine the type of radio message being sent or received.

3. How does the `RadioMenu` class handle user input for sending radio messages?
- The `RadioMenu` class checks for specific key inputs (e.g., `Alpha1`, `Alpha2`, etc.) and sends the corresponding radio message based on the current mode.