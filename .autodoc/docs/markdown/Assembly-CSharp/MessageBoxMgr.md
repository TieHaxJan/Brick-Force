[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\MessageBoxMgr.cs)

The `MessageBoxMgr` class is responsible for managing message boxes in the Brick-Force project. It provides methods to add, delete, and retrieve message boxes, as well as check for the presence of message boxes.

The class has a private list variable `msgBoxes` to store the message boxes. It also has a private static variable `_instance` to hold the instance of the `MessageBoxMgr` class.

The class has a public static property `Instance` that allows access to the instance of the `MessageBoxMgr` class. It uses a singleton pattern to ensure that only one instance of the class is created. If the `_instance` variable is null, it tries to find an existing instance of the `MessageBoxMgr` class using `Object.FindObjectOfType`. If no instance is found, it logs an error message. The `Instance` property is used to access the methods and properties of the `MessageBoxMgr` class throughout the project.

The `Awake` method initializes the `msgBoxes` list and ensures that the `MessageBoxMgr` object is not destroyed when a new scene is loaded using `Object.DontDestroyOnLoad`.

The `OnApplicationQuit` method sets the `_instance` variable to null when the application is quitting.

The `Update` method checks if the `openForcePointChargeDlg` flag is true. If it is, it retrieves a `Good` object from the `ShopManager` using a code string "s80". If the `Good` object is not found, it logs an error message. Otherwise, it initializes a `BuyTermDialog` dialog with the retrieved `Good` object using the `InitDialog` method. Finally, it sets the `openForcePointChargeDlg` flag to false.

The class provides several methods to manipulate the message boxes. The `GetNextItem` method returns the next message box in the list based on the given message box. The `HasNextItem` method checks if there is a next message box after the given message box. The `GetPrevItem` method returns the previous message box in the list based on the given message box. The `HasPrevItem` method checks if there is a previous message box before the given message box. The `DelMessage` method removes a message box from the list. The `HasMsg` method checks if there are any message boxes in the list. The `Clear` method clears all the message boxes from the list.

The class also provides methods to add different types of message boxes. The `AddMessage` method adds a warning type message box to the list. The `AddSelectMessage` method adds a select type message box to the list. The `AddForcePointChargeMessage` method adds a force point charge type message box to the list. The `AddQuitMesssge` method adds a quit type message box to the list. These methods create a new `MsgBox` object with the given message and add it to the `msgBoxes` list. They also initialize a `MsgBoxDialog` dialog with the created `MsgBox` object using the `InitDialog` method.

Overall, the `MessageBoxMgr` class provides functionality to manage message boxes in the Brick-Force project. It allows adding, deleting, and retrieving message boxes, as well as checking for the presence of message boxes. It also handles the display of different types of message boxes using dialogs.
## Questions: 
 1. What is the purpose of the `MessageBoxMgr` class?
- The `MessageBoxMgr` class manages a list of message boxes and provides methods for adding, removing, and accessing message boxes.

2. What is the significance of the `openForcePointChargeDlg` variable?
- The `openForcePointChargeDlg` variable is a boolean flag that determines whether a force point charge dialog should be opened. If it is true, the code in the `Update()` method will execute.

3. What is the purpose of the `AddQuitMesssge()` method?
- The `AddQuitMesssge()` method adds a message box of type "QUIT" to the list of message boxes, clears the existing message boxes, and displays the new message box using the `MsgBoxDialog` class.