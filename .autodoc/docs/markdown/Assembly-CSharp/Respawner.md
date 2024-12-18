[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\Respawner.cs)

The `Respawner` class is responsible for handling the respawn functionality of a player in the game. It is a part of the larger Brick-Force project.

The class has several member variables, including `guiDepth`, `gaugeFrame`, `gaugeBar`, `gaugeText`, `respawnTimeSecure`, `outOnce`, `resTime`, `localController`, and `changedRespawnTime`. These variables are used to store various data related to the respawn process.

The `Awake()` method is called when the object is initialized. It first finds the "Me" game object and retrieves the `LocalController` component attached to it. If the `LocalController` component is not found, an error message is logged. If the `LocalController` component is found, it checks if the player has any respawn items and adjusts the respawn time accordingly. The respawn time is then initialized using the `respawnTimeSecure` variable. The `NoCheat` instance is also synchronized with the respawn time.

The `OnDestroy()` method is called when the object is destroyed. It releases the `respawnTimeSecure` variable.

The `Resurrect2()` method is used to resurrect the player. It checks if the `localController` is not null and if the player's hit points are greater than 0. If these conditions are met, it initializes the `respawnTimeSecure` variable to a value of 0.5f, sets the `DeltaFromDeath` property of the `localController` to 0.05f, and sets the `changedRespawnTime` flag to true.

The `Resurrect()` method is similar to `Resurrect2()`, but it does not set the `DeltaFromDeath` property and uses the `respawnTime` value instead.

The `DoSpawn()` method is responsible for spawning the player. It first checks if the `localController` is not null. If the `changedRespawnTime` flag is set, it initializes the `respawnTimeSecure` variable to the initial respawn time. The `respawnTimeSecure` variable is then reset. If a `spawner` object is provided, the `localController` is spawned at the specified position and rotation. Otherwise, a random spawn position and rotation are used.

The `CheckJustRespawn()` method checks if the player has just respawned. It finds the "Main" game object and retrieves the `ShooterTools` component attached to it. If the component is not null and it contains the "just_respawn" string, it returns true. Otherwise, it returns false.

The `OnGUI()` method is responsible for displaying the respawn progress bar on the screen. It first checks if the `localController` is not null and if the player's hit points are less than or equal to 0. If these conditions are met, it calculates the progress of the respawn based on the `DeltaFromDeath` and `respawnTime` values. If the progress is greater than or equal to 1, it checks the current room type and performs the appropriate actions for each room type. If the room type is "Tutor", it calls the `DoSpawn()` method with a specific spawner. Otherwise, it checks the room type and performs the appropriate actions based on the room type. The `outOnce` flag is used to ensure that certain actions are only performed once. If the room type is "Explosion", the flag is set to true. Otherwise, it is set to false.

The `Update()` method is called every frame. It calls the `KillCheater()` method of the `NoCheat` instance to check for any cheating attempts related to the respawn time.

In summary, the `Respawner` class handles the respawn functionality of a player in the game. It initializes the respawn time, handles the resurrection process, spawns the player, displays the respawn progress bar, and checks for cheating attempts related to the respawn time.
## Questions: 
 1. What is the purpose of the `Respawner` class?
- The `Respawner` class is responsible for handling the respawn functionality of a player in the game.

2. What is the significance of the `resTime` variable?
- The `resTime` variable represents the time it takes for a player to respawn after dying.

3. What is the purpose of the `OnGUI` method?
- The `OnGUI` method is responsible for displaying the respawn gauge and text on the game screen when the player's hit points are zero.