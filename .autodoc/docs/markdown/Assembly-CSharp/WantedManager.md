[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\WantedManager.cs)

The code provided is for a class called `WantedManager` in the Brick-Force project. This class is responsible for managing a list of "wanted" items and providing various functionalities related to these items.

The class has a private static variable `_instance` which holds a reference to the singleton instance of the `WantedManager` class. The instance is accessed through a public static property `Instance`. The purpose of this singleton pattern is to ensure that there is only one instance of the `WantedManager` class throughout the project.

The class also has a private list variable `list` which stores integers representing the "wanted" items. The class provides methods to add, remove, and check if an item is wanted. The `AddWanted` method adds an item to the list if certain conditions are met, such as the current room type being a team match or individual match, and the use of wanted items being enabled. The `DelWanted` method removes an item from the list if it exists.

The class also provides methods to retrieve information about the wanted items. The `ToArray` method returns an array representation of the list. The `IsWanted` method checks if a given item is in the list. The `GetWantedHpMaxBoost` and `GetWantedAtkPowBoost` methods calculate and return the boost values for the maximum HP and attack power of a given item, based on whether it is wanted or not.

The `Awake` method is called when the object is initialized and ensures that the `WantedManager` instance is not destroyed when a new scene is loaded. The `Start` and `Update` methods are empty and do not have any functionality.

Overall, the `WantedManager` class is responsible for managing a list of wanted items, providing methods to add, remove, and check if an item is wanted, as well as retrieving boost values for wanted items. This class is likely used in the larger Brick-Force project to handle the logic and functionality related to wanted items in the game.
## Questions: 
 1. What is the purpose of the `WantedManager` class?
- The `WantedManager` class is responsible for managing a list of wanted items and providing methods to add, remove, and check if an item is wanted.

2. What is the significance of the `Instance` property?
- The `Instance` property provides a singleton instance of the `WantedManager` class, ensuring that there is only one instance of the class throughout the application.

3. What is the purpose of the `GetWantedHpMaxBoost` and `GetWantedAtkPowBoost` methods?
- These methods calculate and return the boost values for maximum HP and attack power based on whether a specific item is wanted or not.