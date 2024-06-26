[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\BootstrapMain.cs)

The `BootstrapMain` class is a script that is responsible for initializing and setting up the game when it starts. It is a part of the larger Brick-Force project.

The `Awake` method is called when the script is first loaded. It starts the injection detection process using the `InjectionDetector.StartDetection` method. If an injection is detected, it logs a message and calls the `HardExit` method from the `BuildOption` class.

The `Start` method is called after the `Awake` method. It initializes the `once` variable to false.

The `OnGUI` method is responsible for drawing the loading screen and logo on the screen. It uses the `GUISkinFinder` class to get the GUI skin and sets it as the current GUI skin. It then calculates the position of the loading image and logo based on the screen size and draws them using the `TextureUtil.DrawTexture` method. It also checks if the font is ready and if so, it displays the "Loading Bricks..." text using the `LabelUtil.TextOut` method.

The `Init` method is a coroutine that is responsible for initializing the game settings. It retrieves the screen width, height, and full-screen mode from the player preferences. If the width or height is less than the minimum screen width or height, it sets them to the minimum values. It then checks if the width and height are equal to or greater than the maximum screen resolution and sets the full-screen mode accordingly. Finally, it sets the screen resolution using the `Screen.SetResolution` method and waits for a frame to complete.

The `Update` method is called every frame. It checks if the font is ready and if the game scene is loaded. If both conditions are met and the `once` variable is false, it sets `once` to true and starts loading the game data by calling the `Load` method from the `StringMgr` and `WordFilter` classes. It also starts the `Init` coroutine.

The `LateUpdate` method is called after all other updates have been processed. It checks if the setup is complete and if the "LoadBrick" scene can be loaded. If both conditions are met, it loads the "LoadBrick" scene using the `Application.LoadLevel` method.

In summary, the `BootstrapMain` script is responsible for initializing the game and setting up the initial game settings. It detects injections, displays the loading screen and logo, and loads the game data and scene. It is an essential part of the Brick-Force project as it ensures that the game starts correctly and all necessary resources are loaded.
## Questions: 
 1. What is the purpose of the `Awake()` method?
- The `Awake()` method is used to start the detection of code injection and disable eating key press on text field focus.

2. What is the purpose of the `Init()` method and what does it do?
- The `Init()` method is a coroutine that sets the screen resolution and quality level based on player preferences and system capabilities.

3. What is the purpose of the `LateUpdate()` method and when does it execute?
- The `LateUpdate()` method is executed after all other `Update()` methods and it checks if the setup is complete and if the level "LoadBrick" can be loaded, then it loads the level.