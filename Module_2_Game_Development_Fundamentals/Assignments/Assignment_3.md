### Assignment: Build a Platformer Prototype with Basic Jumping Mechanics and Enemy Interactions

#### Problem Statement:
Create a simple platformer prototype using Python and Pygame that incorporates basic jumping mechanics and enemy interactions. Your prototype should allow the player to jump between platforms while avoiding enemies. This assignment will help you apply key game design principles discussed in Lecture 3, specifically focusing on player engagement and feedback.

#### Starter Code:
Below is a basic framework for your platformer game. You will need to build upon this code by adding jumping mechanics, enemy interactions, and player feedback.

```python
import pygame
import random

# Initialize Pygame
pygame.init()

# Set up display
width, height = 800, 600
screen = pygame.display.set_mode((width, height))
pygame.display.set_caption("Platformer Prototype")

# Define colors
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)

# Player settings
player_pos = [100, 500]
player_size = 50
player_velocity = 5
is_jumping = False
jump_count = 10

# Enemy settings
enemy_pos = [random.randint(0, width - player_size), random.randint(0, height - player_size)]
enemy_size = 50

# Game loop
running = True
while running:
    pygame.time.delay(30)
    screen.fill(WHITE)

    # Event handling
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Player movement
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT] and player_pos[0] > player_velocity:
        player_pos[0] -= player_velocity
    if keys[pygame.K_RIGHT] and player_pos[0] < width - player_size - player_velocity:
        player_pos[0] += player_velocity
    if not is_jumping:
        if keys[pygame.K_SPACE]:
            is_jumping = True
    else:
        if jump_count >= -10:
            neg = 1
            if jump_count < 0:
                neg = -1
            player_pos[1] -= (jump_count ** 2) * 0.5 * neg
            jump_count -= 1
        else:
            is_jumping = False
            jump_count = 10

    # Draw player and enemy
    pygame.draw.rect(screen, BLACK, (player_pos[0], player_pos[1], player_size, player_size))
    pygame.draw.rect(screen, (255, 0, 0), (enemy_pos[0], enemy_pos[1], enemy_size, enemy_size))

    # Check for collisions
    if (player_pos[0] < enemy_pos[0] < player_pos[0] + player_size or player_pos[0] < enemy_pos[0] + enemy_size < player_pos[0] + player_size) and \
       (player_pos[1] < enemy_pos[1] < player_pos[1] + player_size or player_pos[1] < enemy_pos[1] + enemy_size < player_pos[1] + player_size):
        print("Collision detected! Game Over.")

    pygame.display.update()

pygame.quit()
```

#### Detailed Instructions:
1. **Implement Jumping Mechanics**: 
   - Modify the `is_jumping` logic to ensure that the player can only jump when they are on the ground. You may need to add a ground check.
   - Ensure that the player's vertical position is updated correctly based on the jump count.

2. **Create Enemy Interactions**:
   - Add functionality to move the enemy across the screen horizontally.
   - Implement collision detection between the player and the enemy to trigger a "Game Over" message.

3. **Add Player Feedback**:
   - Implement visual feedback when the player jumps (e.g., change the player's color).
   - Provide audio feedback when a collision occurs or when the player jumps successfully. You can use Pygame's mixer for sound effects.

4. **Enhance Gameplay**:
   - Add platforms for the player to jump on. You can create a list of platforms with their positions and sizes.
   - Consider adding a scoring system that rewards players for avoiding enemies or reaching certain platforms.

#### Criteria for Success and Evaluation:
- **Functionality**: The prototype should allow the player to jump between platforms and interact with enemies.
- **Engagement**: The game should provide an engaging experience with feedback mechanisms in place.
- **Code Quality**: The code should be clean, well-structured, and include comments explaining your logic.
- **User Experience**: The game should be playable and enjoyable, reflecting the principles of balance and feedback discussed in the lecture.

This assignment encourages hands-on practice with real-world relevance in game development while reinforcing key concepts from your lecture on game design principles. Good luck, and have fun creating your platformer prototype!