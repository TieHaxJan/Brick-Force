[View code on GitHub](https://github.com/TieHaxJan/Brick-Force/Assembly-CSharp\_Emulator\Utils\Utils.cs)

The code provided is a utility class called "Utils" that contains two static methods: "SplitList" and "HSVToRGB". 

The "SplitList" method takes in a generic list and an integer chunkSize as parameters. It splits the input list into smaller lists of size chunkSize and returns a list of lists. The method first checks if the chunkSize is greater than 0, and if not, it throws an ArgumentException. It then initializes an empty list called "retVal" to store the smaller lists. The method uses a while loop to iterate through the input list. Inside the loop, it calculates the number of elements to take from the input list based on the chunkSize and the current index. It uses the "GetRange" method to extract the elements from the input list and adds the resulting sublist to "retVal". Finally, it increments the index by the chunkSize. Once the loop is finished, the method returns "retVal".

Here is an example usage of the "SplitList" method:

```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
List<List<int>> splitNumbers = Utils.SplitList(numbers, 3);
```

The "HSVToRGB" method takes in four parameters: float H, float S, float V, and an optional boolean hdr. It converts the given HSV (Hue, Saturation, Value) color values to RGB (Red, Green, Blue) color values and returns a Color object. The method first initializes a Color object called "white" with default RGB values. It then checks if the saturation (S) is 0. If so, it sets the RGB values of "white" to the value (V). If the value (V) is 0, it sets the RGB values of "white" to 0. Otherwise, it calculates the RGB values based on the HSV values using a switch statement. The resulting RGB values are assigned to "white". If the hdr parameter is false, the RGB values are clamped between 0 and 1. Finally, the method returns "white".

Here is an example usage of the "HSVToRGB" method:

```csharp
float H = 0.5f;
float S = 1f;
float V = 1f;
Color rgbColor = Utils.HSVToRGB(H, S, V);
```

Overall, this utility class provides functionality for splitting a list into smaller lists and converting HSV color values to RGB color values. These methods can be used in various parts of the larger project to handle list manipulation and color conversions.
## Questions: 
 1. What does the `SplitList` method do and how does it work?
- The `SplitList` method takes a list and a chunk size as input and splits the list into smaller lists of the specified chunk size. It does this by iterating over the input list and using the `GetRange` method to extract a chunk of elements at each iteration.

2. What does the `HSVToRGB` method do and how does it convert HSV values to RGB?
- The `HSVToRGB` method takes in hue (H), saturation (S), and value (V) values and converts them to an RGB color. It does this by using a series of calculations and conditional statements to determine the RGB values based on the input HSV values.

3. What does the `RGBToHSV` method do and how does it convert RGB values to HSV?
- The `RGBToHSV` method takes in an RGB color and converts it to HSV values. It does this by comparing the RGB values to determine the dominant color, and then using a helper method to calculate the HSV values based on the dominant color and the other two RGB values.