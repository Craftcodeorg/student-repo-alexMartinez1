### Assignment: Create a Text-Based Adventure Game

#### Problem Statement
Design a simple text-based adventure game where the player makes choices that affect the outcome of the story. The game will utilize basic Python syntax and data types, such as strings for player input, integers for player health, and booleans to track the game state. This assignment will help you apply the concepts learned in Lecture 3, focusing on basic syntax and data types in Python.

#### Starter Code
Below is a basic framework for your text-based adventure game. You will need to expand upon this starter code by adding more features, choices, and game logic.

```python
# Starter code for a text-based adventure game

# Player attributes
player_name = input("Enter your character's name: ")
player_health = 100
is_game_over = False

# Function to display player status
def display_status():
    print(f"Player: {player_name}, Health: {player_health}, Game Over: {is_game_over}")

# Function to simulate a choice in the game
def make_choice():
    global player_health, is_game_over
    print("You are in a dark forest. What do you want to do?")
    print("1. Explore the forest.")
    print("2. Rest at a campfire.")
    
    choice = input("Enter 1 or 2: ")
    
    if choice == "1":
        print("You encounter a wild beast!")
        player_health -= 20  # Reduce health
        if player_health <= 0:
            is_game_over = True
            print("You have been defeated by the beast!")
    elif choice == "2":
        print("You rest and regain some health.")
        player_health += 10  # Regain health
        if player_health > 100:
            player_health = 100  # Max health cap
    else:
        print("Invalid choice! Please choose again.")

# Game loop
while not is_game_over:
    display_status()
    make_choice()

print("Game Over!")
```

#### Detailed Instructions
1. **Player Input**: Modify the `input()` function to allow players to enter their character's name at the start of the game.
   
2. **Expand Choices**: Add more choices in the `make_choice()` function. For example, allow the player to:
   - Fight the beast or run away.
   - Find an item that could restore health or give them an advantage.

3. **Health Management**: Implement additional logic to manage player health:
   - Create a function to check if the player is still alive.
   - If health drops below zero, set `is_game_over` to `True` and break out of the loop.

4. **Game Narrative**: Enhance the storytelling aspect of your game by adding descriptive text for each scenario, making it more immersive.

5. **Victory Condition**: Introduce a victory condition where the player can win by completing certain tasks or defeating an enemy.

#### Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:
- **Functionality**: The game should run without errors and allow for player choices that affect the outcome.
- **Code Quality**: The code should be clean, well-structured, and include comments explaining key sections.
- **User Experience**: The game should provide clear instructions and feedback to the player, enhancing engagement.
- **Creativity**: Incorporate unique elements or storylines that showcase your creativity in game design.

### Submission Instructions
Once you have completed your text-based adventure game, submit your Python file (.py) via email to alexMartinez1@example.com. Ensure that your code is well-documented and follows best practices for readability and maintainability.