# CustomFrame

`CustomFrame` is a Java Swing class extending `JFrame`, providing additional functionalities and customization for creating GUI windows. It allows for easy customization of window size, title, and background image.

## Usage

### Basic Usage

```java
// Default size and title and resizable
CustomFrame frame = new CustomFrame("My Frame", true);

// Custom size and title and resizable
CustomFrame customSizeFrame = new CustomFrame(1.5, 1, 1.5, 1, "Custom Size Frame", true);

// Custom size based on the golden ratio and resizable
CustomFrame goldenRatioFrame = new CustomFrame(CustomFrame.PHI_HEIGHT, 1, 1, "Golden Ratio Frame", true);
```

### Set Background Image

```java
CustomFrame frameWithBackground = new CustomFrame("Frame with Background", true);
frameWithBackground.setBackgroundImage(frameWithBackground.loadImage("background.jpg"));
```

### Scaled Dimensions

```java
// Get scaled dimension
Dimension scaledDimension = frame.getScaledDimension(2, 2);

// Get scaled dimension with custom multipliers and scales
Dimension customScaledDimension = frame.getScaledDimension(1.5, 2, 1.5, 2);
```

## Constructors

### Default Constructor

```java
CustomFrame(String title, boolean resizable)
```

Constructs a `CustomFrame` with default size and title.

### Custom Size Constructor

```java
CustomFrame(double widthMultiplier, double widthScale,
            double heightMultiplier, double heightScale, String title, boolean resizable)
```

Constructs a `CustomFrame` with a custom size and title.

### Golden Ratio Constructor

```java
CustomFrame(int phi, double multiplier, double scale, String title, boolean resizable)
```

Constructs a `CustomFrame` with a custom size based on the golden ratio.



## Methods

```java
getScaledDimension(double widthScale, double heightScale)
```

Calculates the scaled dimension based on width and height scales.

* Params:
    - `widthScale`: Scale factor for width.
    - `heightScale`: Scale factor for height.
* Returns: `Dimension`

```java
getScaledDimension(double widthMultiplier, double widthScale, double heightMultiplier, double heightScale)
```

Calculates the scaled dimension based on width and height multipliers and scales.

* Params:
    - `widthMultiplier`: Multiplier for the original width.
    - `widthScale`: Scale factor for width.
    - `heightMultiplier`: Multiplier for the original height.
    - `heightScale`: Scale factor for height.
* Returns: `Dimension`

```java
setBackgroundImage(String path)
```

Sets the background image of the frame.

* Params:
    - `path`: Path to the background image file.

```java
setBackgroundImage(Image image)
```

Sets the background image of the frame.

* Params:
    - `image`: Image to set as the background.

```java
loadImage(String filename)
```

Returns the loaded image.

* Params:
    - `filename`: Name of the image file.
* Returns: `Image`

```java
loadImage(String filename, String path)
```

Returns the loaded image.

* Params:
    - `filename`: Name of the image file.
    - `path`: Path to the image file.
* Returns: `Image`

```java
scaleImageIcon(ImageIcon imageIcon, int width, int height)
```

Scales an image.

* Params:
    - `imageIcon`: The ImageIcon to scale.
    - `width`: The desired width of the scaled icon.
    - `height`: The desired height of the scaled icon.
* Returns: The scaled ImageIcon.

```java
scaleImageIcon(ImageIcon imageIcon, double scaleWidth, double scaleHeight)
```

Scales an image.

* Params:
    - `imageIcon`: The ImageIcon to scale.
    - `scaleWidth`: The scale width of the scaled icon (original width * scaleWidth).
    - `scaleHeight`: The scale height of the scaled icon (original height * scaleHeight).
* Returns: The scaled ImageIcon.

```java
scaleImage(Image img, int width, int height)
```

Scales an image.

* Params:
    - `img`: The Image to scale.
    - `width`: The desired width of the scaled icon.
    - `height`: The desired height of the scaled icon.
* Returns: The scaled Image.

```java
scaleImage(Image img, double scaleWidth, double scaleHeight)
```

Scales an image.

* Params:
    - `img`: The Image to scale.
    - `scaleWidth`: The scale width of the scaled icon (original width * scaleWidth).
    - `scaleHeight`: The scale height of the scaled icon (original height * scaleHeight).
* Returns: The scaled Image.

```java
getImageIconWidth(ImageIcon imageIcon)
```

Retrieves the width of an image represented by the provided ImageIcon object.

* Params:
    - `imageIcon`: The ImageIcon containing the image to query.
* Returns: The width of the image in pixels.

```java
getImageIconHeight(ImageIcon imageIcon)
```

Retrieves the height of an image represented by the provided ImageIcon object.

* Params:
    - `imageIcon`: The ImageIcon containing the image to query.
* Returns: The height of the image in pixels.

```java
getImageIconDimension(ImageIcon imageIcon)
```

Retrieves the dimensions of an image represented by the provided ImageIcon object as a Dimension object.

* Params:
    - `imageIcon`: The ImageIcon containing the image to query.
* Returns: A Dimension object containing the width and height of the image.

```java
getImageWidth(Image image)
```

Retrieves the width of an image represented by the provided Image object.

* Params:
    - `image`: The Image containing the image to query.
* Returns: The width of the image in pixels.

```java
getImageHeight(Image image)
```

Retrieves the height of an image represented by the provided Image object.

* Params:
    - `image`: The Image containing the image to query.
* Returns: The height of the image in pixels.

```java
getImageDimension(Image image)
```

Retrieves the dimensions of an image represented by the provided Image object as a Dimension object.

* Params:
    - `image`: The ImageIcon containing the image to query.
* Returns: A Dimension object containing the width and height of the image.



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.
