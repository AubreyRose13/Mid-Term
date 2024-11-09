# Mid-Term
Second part of the mid-term

Week 8 Projects 
Project 1 testsort.py
def isSorted(lst):
    """
    Check if the provided list is sorted in ascending order.

    :param lst: List of comparable elements.
    :return: True if the list is sorted, False otherwise.
    """
    # An empty list is considered sorted
    if len(lst) <= 1:
        return True

    # Loop through the list and compare each item with its successor
    for i in range(len(lst) - 1):
        if lst[i] > lst[i + 1]:
            return False  # Return False if a pair is out of order

    return True  # Return True if no out-of-order pairs were found


# Tester program
if __name__ == "__main__":
    # Test cases
    test_lists = [
        [],  # Empty list (should return True)
        [1],  # Single element (should return True)
        [1, 2, 3],  # Sorted list (should return True)
        [1, 2, 2, 3],  # Sorted list with duplicates (should return True)
        [3, 1, 2],  # Unsorted list (should return False)
        [1, 3, 2],  # Unsorted list (should return False)
        [2, 2, 2],  # All elements equal (should return True)
    ]

    for i, test_list in enumerate(test_lists):
        print(f"Test case {i + 1}: {test_list} => isSorted: {isSorted(test_list)}")

Project 2 testfunction.py
# testinputfunctions.py

def inputFloat(prompt="Enter a floating-point number: "):
    """
    Prompt the user for a floating-point number and return it.
    The function ensures robust input of floating-point numbers.
    It allows digits and a single decimal point only.
    
    :param prompt: The prompt message to display to the user.
    :return: The validated floating-point number.
    """
    while True:
        user_input = input(prompt).strip()  # Read input and remove whitespace
        if validate_float(user_input):
            return float(user_input)  # Convert to float and return
        else:
            print("Invalid input. Please enter a valid floating-point number.")

def validate_float(input_string):
    """
    Validate that the input string is a valid floating-point number.
    It allows digits and a single decimal point only.
    
    :param input_string: The input string to validate.
    :return: True if valid, False otherwise.
    """
    if input_string.count('.') > 1:  # More than one decimal point
        return False
    try:
        float(input_string)  # Try converting to float
        return True
    except ValueError:
        return False  # Not a valid float

# Testing the inputFloat function
if __name__ == "__main__":
    # Run a test for the inputFloat function
    test_cases = [
        "123.456",   # Valid
        "0.0",       # Valid
        "-123.456",  # Valid
        "123",       # Valid (integer)
        "12.34.56",  # Invalid
        "abc",       # Invalid
        "123abc",    # Invalid
        "123.",      # Valid (will be 123.0)
        ".456",      # Valid (will be 0.456)
        "-.456",     # Valid (will be -0.456)
    ]

    for test in test_cases:
        print(f"Testing input: '{test}' => ", end="")
        if validate_float(test):
            print("Valid float:", float(test))
        else:
            print("Invalid input.")

Week 9 Projects
Project 1 drawcircle.py
import turtle
import math

def drawCircle(t, center, radius):
    # Move the turtle to the center position
    t.penup()
    t.goto(center)
    t.pendown()

    # Calculate the distance moved for each step
    distance = (2.0 * math.pi * radius) / 120.0

    # Draw the circle by turning and moving
    for _ in range(120):
        t.forward(distance)
        t.right(3)

# Example usage
if __name__ == "__main__":
    # Create a turtle object
    my_turtle = turtle.Turtle()

    # Set the speed (optional)
    my_turtle.speed(1)

    # Define the radius
    radius = 100

    # Call the drawCircle function
    drawCircle(my_turtle, (0, -radius), radius)  # Draw circle of radius 100 at (0, -100)

    # Finish
    turtle.done()

Project 2 gif.py
from PIL import Image

def gray_scale(image):
    """Converts the argument image to gray scale."""
    for y in range(image.height):
        for x in range(image.width):
            (r, g, b) = image.getpixel((x, y))
            r = int(r * 0.299)
            g = int(g * 0.587)
            b = int(b * 0.114)
            lum = r + g + b
            image.putpixel((x, y), (lum, lum, lum))  # Set the pixel to gray

# Load the image
image = Image.open("smokey.gif")  # Ensure the image path is correct

# Convert to grayscale
gray_scale(image)

# Save the modified image
image.save("smokey_gray.gif")

# Display the modified image
image.show()

Project 3 hexagon.py
# Define the variables
width = 300
height = 200
using_underscore_idle = True
color_mode = 255

# Optional: Print the variables to verify their values
print("Width:", width)
print("Height:", height)
print("Using Underscore Idle:", using_underscore_idle)
print("Color Mode:", color_mode)

import turtle

# Create a turtle object
t = turtle.Turtle()

# Line 1: For bolder lines
t.width(2)  # Set the line width

# Line 2: Turn to face north
t.left(90)  # Turn to face north

# Line 3: Draw a vertical line in black
t.forward(30)  # Draw a vertical line

# Line 4: Turn to face west
t.left(90)  # Turn to face west

# Line 5: Prepare to move without drawing
t.penup()  # Lift the pen up

# Line 6: Move to beginning of horizontal line
t.forward(10)  # Move to starting position

# Line 7: Turn to face east
t.setheading(0)  # Turn to face east

# Line 8: Set pen color to red
t.pencolor("red")  # Set the pen color

# Line 9: Prepare to draw
t.pendown()  # Lower the pen to start drawing

# Line 10: Draw a horizontal line in red
t.forward(20)  # Draw a horizontal line

# Line 11: Make the turtle invisible
t.hideturtle()  # Hide the turtle

# Finish drawing
turtle.done()

Project 4 PIP.py
from PIL import Image

# Load the image
image = Image.open("smokey.gif")  # Make sure the image path is correct

# Get the RGB values of the pixel at (0, 0)
(r, g, b) = image.getpixel((0, 0))

# Print the RGB values
print("RGB values at (0, 0):", r, g, b)
from PIL import Image

# Load the image
image = Image.open("smokey.gif")  # Ensure the image path is correct

# Get the RGB values of the pixel at (0, 0)
(r, g, b) = image.getpixel((0, 0))

# Modify the pixel color (increasing each channel by 10)
image.putpixel((0, 0), (r + 10, g + 10, b + 10))

# Save the modified image (optional)
image.save("smokey_modified.gif")

# Display the modified image (optional)
image.show()
def average(triple):
    (a, b, c) = triple  # Unpack the tuple
    return (a + b + c) // 3  # Return the average

# Call the average function with a tuple of numbers
result = average((40, 50, 60))

# Print the output
print(result)  # Expected output: 50

Project 5 radial.py
# Define the variables
width = 300
height = 200
using_underscore_idle = True
color_mode = 255

# Optional: Print the variables to verify their values
print("Width:", width)
print("Height:", height)
print("Using Underscore Idle:", using_underscore_idle)
print("Color Mode:", color_mode)

import turtle

# Create a turtle object
t = turtle.Turtle()

# Line 1: For bolder lines
t.width(2)  # Set the line width

# Line 2: Turn to face north
t.left(90)  # Turn to face north

# Line 3: Draw a vertical line in black
t.forward(30)  # Draw a vertical line

# Line 4: Turn to face west
t.left(90)  # Turn to face west

# Line 5: Prepare to move without drawing
t.penup()  # Lift the pen up

# Line 6: Move to beginning of horizontal line
t.forward(10)  # Move to starting position

# Line 7: Turn to face east
t.setheading(0)  # Turn to face east

# Line 8: Set pen color to red
t.pencolor("red")  # Set the pen color

# Line 9: Prepare to draw
t.pendown()  # Lower the pen to start drawing

# Line 10: Draw a horizontal line in red
t.forward(20)  # Draw a horizontal line

# Line 11: Make the turtle invisible
t.hideturtle()  # Hide the turtle

# Finish drawing
turtle.done()

Project 6 random.py
import turtle

def radial_pattern(t, n, length, shape):
    """Draws a radial pattern of n shapes with the given length."""
    for count in range(n):
        shape(t, length)  # Draw the specified shape
        t.left(360 / n)   # Turn to create the radial pattern

def square(t, length):
    """Draws a square with the given length."""
    for _ in range(4):
        t.forward(length)
        t.left(90)

def hexagon(t, length):
    """Draws a hexagon with the given length."""
    for _ in range(6):
        t.forward(length)
        t.left(60)

# Create a turtle object
t = turtle.Turtle()

# Draw a radial pattern of squares
radial_pattern(t, n=10, length=50, shape=square)

# Clear the drawing
t.clear()

# Draw a radial pattern of hexagons
radial_pattern(t, n=10, length=50, shape=hexagon)

# Finish drawing
turtle.done()

Project 7 smokey.py
from PIL import Image, ImageDraw

# Create a new image with a specific size (150x150)
image = Image.new("RGB", (150, 150))

# Initialize drawing context
draw = ImageDraw.Draw(image)

# Define blue color
blue = (0, 0, 255)

# Get the height of the image
y = image.height // 2  # Middle of the image

# Draw a blue line at the center
for x in range(image.width):
    draw.point((x, y - 1), fill=blue)  # Draw pixel above the center
    draw.point((x, y), fill=blue)      # Draw pixel at the center
    draw.point((x, y + 1), fill=blue)  # Draw pixel below the center

# Display the image
image.show()  # Open the image in the default viewer

Project 8 smokey2.py
# Assuming 'image' is a predefined image object with a 'get_pixel' method

# Get the pixel color at (x, y)
red, green, blue = image.get_pixel(x, y)

# Adjust the red and blue values based on their intensity
if red < 63:
    red = int(red * 1.1)
    blue = int(blue * 0.9)
elif red < 192:
    red = int(red * 1.15)
    blue = int(blue * 0.85)
else:
    red = min(int(red * 1.08), 255)
    blue = int(blue * 0.93)

Project 9 snowflake.py
import turtle
import math

def drawFractalLine(t, distance, angle, level):
    if level == 0:
        # Move the turtle forward by the specified distance
        t.forward(distance)
    else:
        # Calculate the distance for the fractal segments
        third = distance / 3.0
        # Draw the first segment
        drawFractalLine(t, third, angle, level - 1)
        # Turn left 60 degrees to create the peak of the Koch curve
        t.left(60)
        # Draw the second segment
        drawFractalLine(t, third, angle, level - 1)
        # Turn right 120 degrees
        t.right(120)
        # Draw the third segment
        drawFractalLine(t, third, angle, level - 1)
        # Turn left 60 degrees to complete the segment
        t.left(60)
        # Draw the last segment
        drawFractalLine(t, third, angle, level - 1)

def drawKochSnowflake(t, size, level):
    for angle in [0, -120, 120]:
        drawFractalLine(t, size, angle, level)

if __name__ == "__main__":
    # Create a turtle object
    my_turtle = turtle.Turtle()
    
    # Set the speed (optional)
    my_turtle.speed(0)  # Fastest speed

    # Move the turtle to the starting position
    my_turtle.penup()
    my_turtle.goto(-100, 50)  # Center the snowflake
    my_turtle.pendown()

    # Define the size and level of the Koch snowflake
    size = 300
    level = 4  # Change this to adjust the detail level of the fractal

    # Draw the Koch snowflake
    drawKochSnowflake(my_turtle, size, level)

    # Finish
    turtle.done()

Project 10 squares.py
  def square(t, length):
    """Draws a square with the given length."""
    for count in range(4):
        t.forward(length)
        t.left(90)

# Example usage
import turtle

# Create a turtle object
t = turtle.Turtle()

# Draw a square of length 100
square(t, 100)

# Finish drawing
turtle.done()

Project 11 turtle.py
# Define the variables
width = 300
height = 200
using_underscore_idle = True
color_mode = 255

# Optional: Print the variables to verify their values
print("Width:", width)
print("Height:", height)
print("Using Underscore Idle:", using_underscore_idle)
print("Color Mode:", color_mode)

import turtle

# Create a turtle object
t = turtle.Turtle()

# Line 1: For bolder lines
t.width(2)  # Set the line width

# Line 2: Turn to face north
t.left(90)  # Turn to face north

# Line 3: Draw a vertical line in black
t.forward(30)  # Draw a vertical line

# Line 4: Turn to face west
t.left(90)  # Turn to face west

# Line 5: Prepare to move without drawing
t.penup()  # Lift the pen up

# Line 6: Move to beginning of horizontal line
t.forward(10)  # Move to starting position

# Line 7: Turn to face east
t.setheading(0)  # Turn to face east

# Line 8: Set pen color to red
t.pencolor("red")  # Set the pen color

# Line 9: Prepare to draw
t.pendown()  # Lower the pen to start drawing

# Line 10: Draw a horizontal line in red
t.forward(20)  # Draw a horizontal line

# Line 11: Make the turtle invisible
t.hideturtle()  # Hide the turtle

# Finish drawing
turtle.done()


