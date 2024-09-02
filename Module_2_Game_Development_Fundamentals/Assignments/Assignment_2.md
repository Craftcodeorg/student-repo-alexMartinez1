### Assignment: Create an Interactive Storytelling Game

#### Problem Statement:
Create an interactive storytelling game where players make choices that affect the outcome of the story. This assignment will focus on applying game mechanics discussed in Lecture 2, specifically core mechanics and feedback mechanics. Your game should allow players to navigate through a narrative by making decisions that influence the storyline and lead to different endings.

#### Starter Code:
Below is a basic framework for your interactive storytelling game. This code sets up the environment and provides a simple structure for player choices and outcomes. You will need to expand upon this by adding more story branches and mechanics.

```python
# Starter code for an interactive storytelling game

def start_game():
    print("Welcome to the Interactive Storytelling Game!")
    print("You find yourself in a dark forest. What do you want to do?")
    first_choice()

def first_choice():
    print("1: Explore the forest.")
    print("2: Go back home.")
    choice = input("Enter 1 or 2: ")
    
    if choice == '1':
        explore_forest()
    elif choice == '2':
        go_home()
    else:
        print("Invalid choice. Please try again.")
        first_choice()

def explore_forest():
    print("You venture deeper into the forest and encounter a mysterious creature.")
    print("What do you want to do?")
    print("1: Approach the creature.")
    print("2: Run away.")
    choice = input("Enter 1 or 2: ")
    
    if choice == '1':
        approach_creature()
    elif choice == '2':
        run_away()
    else:
        print("Invalid choice. Please try again.")
        explore_forest()

def go_home():
    print("You decide to go back home. The adventure ends here.")

def approach_creature():
    print("The creature turns out to be friendly! You become friends and continue your adventure together.")
    # Add more story branches here

def run_away():
    print("You run away and safely return home. The adventure ends here.")

# Start the game
start_game()
```

#### Detailed Instructions:
1. **Step 1: Expand the Story**
   - Add more branches to the `explore_forest()` function. For example, after approaching the creature, you could have additional choices that lead to different scenarios (e.g., fighting, befriending, or negotiating with the creature).

2. **Step 2: Implement Feedback Mechanics**
   - After each choice, provide feedback to the player about their decision. For example, if they choose to run away, you could add a message like, "You feel relieved but wonder what could have happened if you had approached the creature."

3. **Step 3: Create Multiple Endings**
   - Develop multiple endings based on the player's choices throughout the game. Use functions to represent different endings and call them based on the player's decisions.

4. **Step 4: Test Your Game**
   - Run your game multiple times to ensure all paths work correctly and that players receive appropriate feedback for their choices.

#### Criteria for Success and Evaluation:
- **Functionality**: The game should run without errors and allow players to make choices that lead to different outcomes.
- **Engagement**: The story should be engaging and provide meaningful choices that affect the narrative.
- **Code Quality**: The code should be clean, well-organized, and include comments explaining each part of the code.
- **User Feedback**: The game should provide clear feedback after each choice, enhancing player experience.

By completing this assignment, you will apply the concepts of game mechanics learned in Lecture 2 while developing your skills in Python game development. Good luck, and have fun creating your interactive storytelling game!