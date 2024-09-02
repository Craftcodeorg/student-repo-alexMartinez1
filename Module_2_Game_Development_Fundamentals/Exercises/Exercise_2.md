# Module Title: Game Development Fundamentals

## Exercise Requirements

### 1. Problem Statement
In this exercise, you will create a simple game where a player-controlled object moves left and right across the screen using keyboard input. This task will help you apply the concepts of game mechanics discussed in Lecture 2, specifically focusing on core mechanics and player interaction. The goal is to implement a moving object that responds to keyboard inputs, reinforcing your understanding of how mechanics dictate gameplay.

### 2. Fill-in-the-Blank Starter Code
Below is a starter code template for your game. You will need to fill in the blanks to complete the functionality of moving the object left and right based on keyboard input.

```python
import pygame

# Initialize Pygame
pygame.init()

# Set up the display
screen = pygame.display.set_mode((800, 600))

# Player variables
player_x = 400  # Starting position in the middle of the screen
player_y = 500  # Fixed vertical position
player_speed = 5  # Speed of player movement

# Game loop
running = True
while running:
    pygame.time.delay(30)  # Control the frame rate

    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    keys = pygame.key.get_pressed()  # Get the state of all keys

    # Move the player based on key presses
    if keys[pygame.K_LEFT]:  # If left arrow is pressed
        player_x -= player_speed  # Move left
    if keys[pygame.K_RIGHT]:  # If right arrow is pressed
        player_x += player_speed  # Move right

    # Drawing the player
    screen.fill((0, 0, 0))  # Clear screen with black
    pygame.draw.rect(screen, (255, 0, 0), (player_x, player_y, 50, 50))  # Draw player as a red square
    pygame.display.update()  # Update the display

pygame.quit()
```

### 3. Hints
- **Hint 1**: Recall how you implemented the jumping mechanic in the previous lecture. You will use similar logic to check for key presses.
- **Hint 2**: Remember that `pygame.key.get_pressed()` returns a list of boolean values indicating whether each key is pressed. You can check specific keys using `pygame.K_LEFT` and `pygame.K_RIGHT`.
- **Hint 3**: Ensure that you maintain the player's position within the window bounds so that the player does not move off-screen.

### 4. Expected Outcome
Upon completing the exercise, you should have a working game where a red square (the player) can move left and right across the screen using the left and right arrow keys. Your final solution should:
- Correctly implement the movement mechanics based on keyboard input.
- Include comments explaining each part of your code.
- Handle potential errors, such as ensuring the player does not move outside the screen boundaries.

This exercise will help solidify your understanding of game mechanics and prepare you for more complex projects in your journey to becoming a proficient Python Developer in game development. 

### Integration
This exercise is structured to be easily integrated into your learning platform. Make sure to test your code thoroughly and seek feedback from community projects or peers as you develop your skills further!