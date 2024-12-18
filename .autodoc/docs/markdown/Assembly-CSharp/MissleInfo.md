[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\MissleInfo.cs)

The code provided defines a class called "MissleInfo" that is used to store information about a missile object in the larger Brick-Force project. 

The class has several properties and fields:
- "obj" is a reference to the missile's GameObject in the Unity engine.
- "uniq" is an integer that represents a unique identifier for the missile.
- "prepos" is a Vector3 that represents the previous position of the missile.
- "elapsed" is a float that represents the amount of time that has passed since the missile was created.
- "elapsedP2P" is a float that represents the amount of time that has passed since the missile was last updated.

The class also has two properties, "Elapsed" and "ElapsedP2P", that provide access to the "elapsed" and "elapsedP2P" fields respectively. These properties allow other parts of the code to read and modify these values.

The purpose of this class is to store and manage information about a missile object. It provides a way to access and update the elapsed time values for the missile, as well as store references to the missile's GameObject and its unique identifier.

This class can be used in the larger Brick-Force project to track and manage missiles. For example, it could be used in a missile manager class that creates and updates missile objects. The "MissleInfo" objects could be created when a missile is spawned and then updated each frame to keep track of the missile's position and elapsed time. Other parts of the code could then access the "MissleInfo" objects to retrieve information about the missiles.

Here is an example of how this class could be used in code:

```csharp
MissleInfo missile = new MissleInfo();
missile.obj = missileGameObject;
missile.uniq = missileId;

// Update the elapsed time values
missile.Elapsed += Time.deltaTime;
missile.ElapsedP2P += Time.deltaTime;

// Get the current elapsed time
float elapsed = missile.Elapsed;

// Get the previous position of the missile
Vector3 previousPosition = missile.prepos;
```

In this example, a new "MissleInfo" object is created and assigned the missile's GameObject and unique identifier. The elapsed time values are then updated each frame using the "Time.deltaTime" value. The current elapsed time and previous position of the missile can then be accessed using the properties and fields of the "MissleInfo" object.
## Questions: 
 1. What is the purpose of the `MissleInfo` class?
- The `MissleInfo` class is used to store information about a missile, including its game object, unique identifier, previous position, and elapsed time.

2. What is the significance of the `Elapsed` and `ElapsedP2P` properties?
- The `Elapsed` property represents the elapsed time since the missile was created, while the `ElapsedP2P` property represents the elapsed time for a point-to-point missile.

3. What is the purpose of the `prepos` variable?
- The `prepos` variable is used to store the previous position of the missile.