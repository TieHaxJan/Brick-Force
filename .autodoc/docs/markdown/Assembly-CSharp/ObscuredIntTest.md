[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\ObscuredIntTest.cs)

The code provided is a part of the Brick-Force project and is a script called "ObscuredIntTest". This script is responsible for testing and demonstrating the usage of the ObscuredInt class from the CodeStage.AntiCheat.ObscuredTypes namespace.

The ObscuredInt class is a data type that provides a way to store and manipulate integer values in an obscured manner, making it difficult for cheaters to modify the values during runtime. It achieves this by encrypting the integer value and storing it in memory.

The script starts by setting the initial value of the "cleanLivesCount" variable to 11 and the "obscuredLivesCount" variable to an obscured version of 11. It then logs the original lives count and how the obscured lives count is stored in memory.

The script then demonstrates the usage of various methods provided by the ObscuredInt class. It sets a new crypto key using the SetNewCryptoKey method, which is used to encrypt and decrypt the integer values. It performs several arithmetic operations on an ObscuredInt variable named "value", such as subtracting 10, adding 100, and dividing by 10. It also increments and decrements the value using the ++ and -- operators.

The script also sets different crypto keys before performing the increment and decrement operations, showcasing the ability to change the encryption key at runtime. This adds an extra layer of security against cheaters who may try to reverse engineer the encryption algorithm.

The script also demonstrates the usage of a callback function named "OnCheatingDetected", which is invoked when cheating is detected. In this case, it simply logs a message and sets the "cheatingDetected" variable to true.

Finally, the script provides two public methods: "UseRegular" and "UseObscured". These methods allow the user to choose between using the regular integer variable "cleanLivesCount" or the obscured integer variable "obscuredLivesCount". They also modify the values by adding a random range between -10 and 50. The purpose of these methods is to show the difference in behavior between regular and obscured integer variables when attempting to modify them.

In summary, this script serves as a demonstration of the ObscuredInt class and its usage in the Brick-Force project. It showcases the ability to store and manipulate integer values in an obscured manner, providing an extra layer of security against cheating.
## Questions: 
 1. What is the purpose of the ObscuredInt class and how does it work?
- The ObscuredInt class is used to store an integer value in an encrypted form in memory. It provides methods to perform arithmetic operations on the encrypted value.

2. How does the code detect cheating and what happens when cheating is detected?
- The code detects cheating by calling the OnCheatingDetected method, which sets the cheatingDetected variable to true. It then logs a message indicating that cheating has been detected.

3. What is the difference between using the regular integer variable cleanLivesCount and the obscured integer variable obscuredLivesCount?
- The regular integer variable cleanLivesCount is not encrypted and can be easily modified in memory. The obscured integer variable obscuredLivesCount is encrypted and provides a level of protection against memory manipulation.