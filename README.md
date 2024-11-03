# 🎨 Hirst Painting with Turtle Graphics 🎨

This project uses Python's Turtle Graphics module to create a dot-painting effect inspired by the artwork of **Damien Hirst**. The program randomly places dots of various colors in a grid layout, creating a vibrant and visually appealing piece of digital art.

## 🖼️ Project Description

This program:
1. Extracts a list of RGB colors from an image (this step is currently commented out in the code).
2. Uses Turtle Graphics to paint a grid of dots, with each dot having a randomly selected color from a predefined color palette.

## 📁 Project Structure

- **Main Script**: This code uses Turtle Graphics to create a 10x10 grid of colored dots.
- **Color Palette**: A predefined list of colors, `colorList`, is used to color each dot, which is based on colors extracted from an image (can be uncommented for image extraction using `colorgram`).

## 🖥️ Code Breakdown

### 1. Importing Libraries and Setting Up Turtle

```python
import turtle
import random
```

### 2. Color Extraction (Optional)
The color extraction section is commented out. You can uncomment and run it with the colorgram library to extract colors from an image named image.jpg:
```python
# import colorgram
# colors = colorgram.extract('image.jpg', 30)
# for color in colors:
#     rgbColors.append((color.rgb.r, color.rgb.g, color.rgb.b))
```

### 3. Turtle Graphics Setup
The Turtle is set up with color mode to support RGB colors, and the starting position is adjusted for the dot grid:
```python
turtle.colormode(255)
tim = turtle.Turtle()
tim.speed("fastest")
tim.penup()
tim.hideturtle()
```

### 4. Dot Painting Logic
The program creates a grid of dots, with each dot randomly colored from colorList. After every 10 dots, the Turtle moves up a row and returns to the start of the new row:
```python
for dotCount in range(1, numberOfDots + 1):
    tim.dot(20, random.choice(colorList))
    tim.forward(50)
    if dotCount % 10 == 0:
        tim.setheading(90)
        tim.forward(50)
        tim.setheading(180)
        tim.forward(500)
        tim.setheading(0)
```

## 🎨 Color Palette
```bash
colorList = [(245, 243, 238), (246, 242, 244), (202, 164, 110), ... (168, 99, 102)]
```

## 🚀 Getting Started
1. Clone the Repository:
```bash
git clone https://github.com/your-username/hirst-painting.git
cd hirst-painting
```
2. Run the Program:
```bash
python main.py
```

## 📝 Notes
- Ensure colorgram is installed if you plan to use color extraction.
- Exit: Click on the screen to exit the program once the painting is complete.

## 📜 License
- This project is licensed under the MIT License. See the LICENSE file for more details.


Enjoy creating your own Hirst-inspired dot painting! 🎨

