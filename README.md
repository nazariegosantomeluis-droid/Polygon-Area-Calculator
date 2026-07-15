# Polygon Area Calculator

A Python project that models basic geometric shapes using object-oriented programming. The application allows users to calculate the area, perimeter, and diagonal of rectangles and squares, generate ASCII representations of the shapes, and determine how many smaller shapes can fit inside a larger one.

> **Note:** This project currently supports rectangles and squares. Additional polygon types can be added in future versions.

---

## Features

- Create rectangles and squares
- Calculate area
- Calculate perimeter
- Calculate diagonal length
- Generate ASCII art representations of shapes
- Modify dimensions after creation
- Determine how many times one shape fits inside another
- Demonstrates inheritance using Python classes

---

## Project Structure

```
polygon_area_calculator.py
README.md
.gitignore
```

---

## Classes

### Rectangle

Represents a rectangle defined by its width and height.

#### Constructor

```python
rectangle = Rectangle(width, height)
```

### Methods

#### Set Width

```python
rectangle.set_width(width)
```

#### Set Height

```python
rectangle.set_height(height)
```

#### Get Area

```python
rectangle.get_area()
```

Returns:

```
width × height
```

---

#### Get Perimeter

```python
rectangle.get_perimeter()
```

Returns:

```
2 × (width + height)
```

---

#### Get Diagonal

```python
rectangle.get_diagonal()
```

Uses the Pythagorean theorem:

```
√(width² + height²)
```

---

#### Get Picture

```python
rectangle.get_picture()
```

Generates an ASCII representation of the rectangle.

Example:

```
****
****
****
```

If either dimension is greater than 50, the function returns:

```
Too big for picture.
```

---

#### Get Amount Inside

```python
rectangle.get_amount_inside(other_shape)
```

Returns the number of times another rectangle or square can fit inside the current rectangle.

Example:

```python
Rectangle(20, 10).get_amount_inside(Rectangle(4, 5))
```

Returns:

```
10
```

---

## Square

The `Square` class inherits from `Rectangle`.

### Constructor

```python
square = Square(side)
```

Unlike rectangles, a square always keeps both dimensions equal.

### Methods

```python
set_side(side)
set_width(side)
set_height(side)
```

Each method updates both width and height simultaneously.

---

## Example Usage

```python
rect = Rectangle(10, 5)

print(rect)
print(rect.get_area())
print(rect.get_perimeter())
print(rect.get_diagonal())
print(rect.get_picture())

square = Square(4)

print(square)

print(rect.get_amount_inside(square))
```

---

## Example Output

```
Rectangle(width=10, height=5)

Area: 50

Perimeter: 30

Diagonal: 11.1803398875

**********
**********
**********
**********
**********

Square(side=4)

Amount Inside: 2
```

---

## Technologies Used

- Python 3
- Object-Oriented Programming (OOP)

---

## Programming Concepts Demonstrated

- Classes and Objects
- Inheritance
- Method Overriding
- Encapsulation
- Constructors
- String Representation (`__str__`)
- Mathematical Computations
- Integer Division
- ASCII Graphics

---

## Learning Objectives

This project demonstrates how to:

- Build reusable object-oriented classes
- Use inheritance effectively
- Override inherited methods
- Perform geometric calculations
- Generate text-based visualizations
- Design maintainable Python code

---

## Future Improvements

- Support additional polygons (triangle, pentagon, hexagon, etc.)
- Circle calculations
- Polygon validation
- Shape rotation
- SVG image generation
- Matplotlib visualization
- Interactive command-line interface
- Graphical user interface (Tkinter or PyQt)

---

## License

This project is licensed under the MIT License.
