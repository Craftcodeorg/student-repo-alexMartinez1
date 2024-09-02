### Module Title: Game Development Fundamentals

---

### Exercise Requirements

#### 1. Problem Statement
As a budding game developer, you are tasked with creating the initial setup for a simple game. Your objective is to set up a Pygame window and display a background color that represents the theme of your game. Imagine you are designing a game where the player explores a mysterious forest. The background color should evoke the feeling of being in a lush, green environment. 

Using the concepts discussed in Lecture 1, implement the code to create a Pygame window with an appropriate background color that reflects this theme.

#### 2. Fill-in-the-Blank Starter Code
```python
import pygame

# Initialize Pygame
pygame.init()

# Set up the game window
screen = pygame.display.set_mode((800, 600))
running = True

# Game loop
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Fill the screen with a color that represents a lush forest
    screen.fill((_____, _____, _____))  # Fill in RGB values for green shades
    pygame.display.flip()

pygame.quit()
```

#### 3. Hints
- Remember that colors in Pygame are represented using RGB values, where each value can range from 0 to 255.
- For a lush green background, consider using different shades of green. You might want to use a darker green for a more mysterious atmosphere.
- Look back at the lecture notes for examples of how colors are defined in Pygame.

#### 4. Expected Outcome
Upon completing this exercise, you should be able to:
- Successfully fill in the blanks with appropriate RGB values to create a green background.
- Demonstrate an understanding of how to set up a Pygame window and manipulate its display properties.
- Ensure your code is well-commented, explaining the purpose of each section and any choices made regarding color selection.
- Implement basic error handling by ensuring that the program can exit gracefully when the window is closed.

---

### Additional Resources
- [Pygame Documentation](https://www.pygame.org/docs/)
- [Color Picker Tool](https://www.w3schools.com/colors/colors_picker.asp) (to help you choose your RGB values)

### Integration
This exercise is designed to reinforce the concepts introduced in Lecture 1 and apply them in a practical context relevant to your interests in game development and interactive storytelling. Ensure you follow best practices in coding and maintain clarity in your comments for future reference as you build your portfolio of small games.