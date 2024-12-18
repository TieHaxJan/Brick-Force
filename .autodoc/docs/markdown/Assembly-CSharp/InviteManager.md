[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\InviteManager.cs)

The `InviteManager` class is a component in the Brick-Force project that manages a list of `Invite` objects. It provides methods to add, remove, and retrieve invite data.

The `InviteManager` class has a public list called `listInvite` which stores instances of the `Invite` class. This list is initially empty.

The class also has a private static instance variable `_instance` and a public static property `Instance`. The `Instance` property is a singleton pattern implementation that ensures only one instance of the `InviteManager` class is created. It uses the `Object.FindObjectOfType` method to find an existing instance of `InviteManager` in the scene or creates a new one if none exists. If the instance is not found or created, it logs an error message.

The `Awake` method is called when the `InviteManager` object is initialized. It uses `Object.DontDestroyOnLoad` to prevent the object from being destroyed when a new scene is loaded.

The `AddInvite` method takes an `Invite` object as a parameter and adds it to the `listInvite` list. It first calls the `Remove` method to remove any existing invite with the same `invitorSeq` value. Then it adds the new invite to the list. It also checks if an instance of the `InviteNoticeDialog` is already open and if so, it initializes the dialog.

The `Remove` method takes an integer `key` as a parameter and removes the invite with the matching `invitorSeq` value from the `listInvite` list. It iterates through the list and compares the `invitorSeq` value of each invite with the `key` value. If a match is found, it removes the invite from the list and exits the loop.

The `RemoveAll` method clears the `listInvite` list and stores the first invite in the list in the `savedForClan` variable.

The `GetData` method returns the value of the `savedForClan` variable.

Overall, the `InviteManager` class provides functionality to manage a list of invites, add new invites, remove invites by key, and retrieve invite data. It also ensures that only one instance of the `InviteManager` class exists in the scene. This class can be used in the larger Brick-Force project to handle invite-related operations and manage invite data.
## Questions: 
 1. What is the purpose of the `InviteManager` class?
- The `InviteManager` class is responsible for managing a list of invites and performing operations such as adding, removing, and retrieving invites.

2. What is the significance of the `Instance` property?
- The `Instance` property is a singleton pattern implementation that ensures there is only one instance of the `InviteManager` class throughout the application.

3. What does the `RemoveAll` method do?
- The `RemoveAll` method clears the list of invites and saves the first invite in the list to a variable called `savedForClan`.