[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\SystemMsgManager.cs)

The `SystemMsgManager` class is responsible for managing system messages in the Brick-Force project. It handles the display and management of messages that appear on the screen during gameplay.

The class contains a private queue `qMessages` that stores instances of the `SystemMsg` class. The `SystemMsg` class represents a single system message and contains information such as the message text and the duration it should be displayed.

The `SystemMsgManager` class is a singleton, meaning that there can only be one instance of it in the project. The `Instance` property provides access to this singleton instance. If there is no existing instance, it tries to find one using `Object.FindObjectOfType`. If it fails to find an instance, it logs an error message.

The `Awake` method initializes the `qMessages` queue and ensures that the `SystemMsgManager` object is not destroyed when a new scene is loaded using `Object.DontDestroyOnLoad`.

The `OnGUI` method is called every frame and is responsible for displaying the system messages on the screen. It retrieves the GUI skin from the `GUISkinFinder` class and sets the GUI depth. It then iterates over the messages in the queue and adjusts their position based on the height of the previous message. Finally, it calls the `Show` method on each message to display it on the screen.

The `ShowMessage` methods are used to add new system messages to the queue. The first method takes only the message text as a parameter and adds a new `SystemMsg` instance with a default duration of 5 seconds. The second method allows specifying a custom duration for the message.

The `Update` method is called every frame and updates each message in the queue by calling their `Update` method. It also removes any messages from the queue that have expired and are no longer valid.

In summary, the `SystemMsgManager` class manages the display and management of system messages in the Brick-Force project. It provides methods to add new messages to the queue and handles their display on the screen. This class is an important component of the user interface system in the larger project.
## Questions: 
 1. What is the purpose of the `SystemMsgManager` class?
- The `SystemMsgManager` class manages a queue of system messages and displays them on the GUI.

2. What is the significance of the `guiDepth` variable?
- The `guiDepth` variable determines the depth at which the system messages will be displayed on the GUI.

3. What is the purpose of the `ShowMessage` methods?
- The `ShowMessage` methods are used to add system messages to the queue, with an optional time parameter to control how long the message will be displayed.