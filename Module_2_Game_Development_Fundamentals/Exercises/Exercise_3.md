### Module Title: Game Development Fundamentals

### Exercise Requirements

#### 1. Problem Statement
You are tasked with creating a simple scoring system for a basic platformer game using Python. In this game, players earn points by collecting items scattered throughout the levels. Your goal is to implement a scoring system that tracks the player's score, provides feedback when they collect an item, and displays the current score on the screen. This exercise will help you apply the game design principles discussed in Lecture 3, particularly focusing on player engagement and feedback.

#### 2. Fill-in-the-Blank Starter Code
Below is the starter code for implementing the scoring system. Fill in the blanks to complete the functionality.

```python
import pygame

# Initialize Pygame
pygame.init()

# Set up display
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("Simple Scoring System")

# Define colors
WHITE = (255, 255, 255)
GREEN = (0, 255, 0)

# Initialize score
score = 0

def display_score(score):
    # Display the current score on the screen
    font = pygame.font.Font(None, 36)
    text = font.render("Score: " + str(score), True, GREEN)
    screen.blit(text, (10, 10))

def collect_item():
    global score
    # Increment score when an item is collected
    score += 10
    # Play sound effect for collecting item (ensure you have 'collect_sound.wav' in your project directory)
    pygame.mixer.Sound('collect_sound.wav').play()

# Main game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Clear the screen
    screen.fill(WHITE)

    # Call the function to display the score
    display_score(______)

    # Simulate collecting an item (for testing purposes)
    if pygame.key.get_pressed()[pygame.K_SPACE]:  # Press space to collect an item
        collect_item()

    # Update the display
    pygame.display.flip()

# Quit Pygame
pygame.quit()
```

#### 3. Hints
- To track the player's score, you will need to use a global variable. Make sure to declare it as `global` within any function that modifies it.
- The `display_score` function takes a parameter that represents the current score. You will need to pass the correct variable when calling this function.
- Remember to play a sound when an item is collected. Ensure that you have the sound file in your project directory.
- Use the `pygame.key.get_pressed()` method to simulate collecting an item when a specific key is pressed (in this case, the space bar).

#### 4. Expected Outcome
By filling in the blanks correctly, you should have a functional scoring system that:
- Tracks and displays the player's score.
- Increases the score by 10 points each time an item is "collected" by pressing the space bar.
- Plays a sound effect whenever an item is collected.
- Properly utilizes game design principles such as feedback (through sound and score display) and player engagement (through interactive item collection).

The final solution should adhere to best practices, include error handling where necessary, and be well-commented to explain the reasoning behind each step.

### Integration
This exercise is designed to reinforce your understanding of game design principles while providing practical coding experience in Python. Make sure to test your code thoroughly and consider how you can expand upon this scoring system in future projects!