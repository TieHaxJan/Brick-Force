[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\ObscuredVector3Test.cs)

The code provided is a part of the Brick-Force project and is a demonstration of how to use the ObscuredVector3 class from the CodeStage.AntiCheat.ObscuredTypes namespace. 

The purpose of this code is to showcase the functionality of the ObscuredVector3 class, which is a secure way to store and manipulate Vector3 positions in memory. It provides a layer of encryption to prevent cheating or tampering with the position data.

The code begins by importing the necessary namespaces and defining two Vector3 variables: playerPosition and obscuredPlayerPosition. The playerPosition variable is a regular Vector3, while the obscuredPlayerPosition variable is an instance of the ObscuredVector3 class.

In the Start() method, a new crypto key is set using the ObscuredVector3.SetNewCryptoKey() method. This key is used to encrypt and decrypt the position data. The playerPosition is then updated with a new Vector3 value and assigned to the obscuredPlayerPosition variable. The encrypted position data is retrieved using the GetEncrypted() method and logged to the console.

The UseRegular() and UseObscured() methods demonstrate how to manipulate the position data using both regular Vector3 and ObscuredVector3. In the UseRegular() method, the playerPosition is updated with a random Vector3 value and the obscuredPlayerPosition is set to a fixed Vector3 value. In the UseObscured() method, the obscuredPlayerPosition is updated with a random Vector3 value and the playerPosition is set to a fixed Vector3 value. The updated position data is then logged to the console.

Overall, this code demonstrates how to use the ObscuredVector3 class to securely store and manipulate Vector3 positions in memory. It provides a way to protect sensitive position data from cheating or tampering in the larger Brick-Force project.
## Questions: 
 1. What is the purpose of the ObscuredVector3 class and how does it differ from the regular Vector3 class?
- The ObscuredVector3 class is used to store and manipulate Vector3 positions in an obscured manner, making it harder for hackers to modify the values. It differs from the regular Vector3 class by providing encryption and decryption methods for the position values.

2. How is the position stored in memory when it is obscured?
- The position is stored in memory as an encrypted Vector3 using the GetEncrypted() method of the ObscuredVector3 class. The encrypted values are then displayed using the Debug.Log() method.

3. How does the UseRegular() and UseObscured() methods affect the playerPosition and obscuredPlayerPosition variables?
- The UseRegular() method sets the useRegular variable to true and modifies the playerPosition by adding a random Vector3. It also sets the obscuredPlayerPosition to a fixed Vector3. The UseObscured() method sets the useRegular variable to false and modifies the obscuredPlayerPosition by adding a random Vector3. It also sets the playerPosition to a fixed Vector3.