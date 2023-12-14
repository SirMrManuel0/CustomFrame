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
frameWithBackground.setBackgroundImage("path/to/background.jpg");
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

### `getScaledDimension(double widthScale, double heightScale): Dimension`

Calculates the scaled dimension based on width and height scales.

### `getScaledDimension(double widthMultiplier, double widthScale, double heightMultiplier, double heightScale): Dimension`

Calculates the scaled dimension based on width and height multipliers and scales.

### `setBackgroundImage(String path): void`

Sets the background image of the frame.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.