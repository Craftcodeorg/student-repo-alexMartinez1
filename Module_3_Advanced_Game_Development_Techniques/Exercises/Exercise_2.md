### Module Title: Advanced Game Development Techniques

### Exercise Requirements

#### 1. Problem Statement
You are tasked with creating an interactive dialogue system for an NPC in a stealth-based game. The dialogue system should allow players to choose responses that affect the NPC's behavior and the outcome of the interaction. The NPC should have different states (e.g., calm, suspicious, hostile) that change based on the player's choices. This exercise will require you to apply the concepts learned in Lecture 2 about NPC behavior algorithms, particularly Finite State Machines (FSM) and how they can be used to manage dialogue interactions.

#### 2. Fill-in-the-Blank Starter Code
Below is the starter code for implementing the interactive dialogue system. You will need to fill in the blanks to complete the functionality.

```python
class NPC:
    def __init__(self):
        self.state = 'calm'  # Initial state of the NPC
        self.dialogue_options = {
            'calm': ["Hello there!", "What brings you here?"],
            'suspicious': ["Why are you here?", "I don't trust you."],
            'hostile': ["Get away from me!", "I won't let you pass!"]
        }

    def interact(self, player_choice):
        # Update NPC state based on player choice
        if player_choice == 'greet':
            self.state = 'calm'
        elif player_choice == 'question':
            self.state = 'suspicious'
        elif player_choice == 'threaten':
            self.state = 'hostile'
        
        # Display current dialogue options based on state
        print("NPC says: " + _______)

# Example interaction
npc = NPC()
player_choice = input("Choose your action (greet/question/threaten): ")
npc.interact(player_choice)
```

#### 3. Hints
- Think about how the `state` variable of the NPC can be used to select which dialogue options to display.
- Remember that the `dialogue_options` dictionary holds the different responses based on the NPC's state. You will need to access this dictionary using the current state.
- Consider using a print statement to show the available options after updating the NPC's state.

#### 4. Expected Outcome
By completing this exercise, you should be able to:
- Implement a simple interactive dialogue system where the NPC's responses change based on player choices.
- Demonstrate an understanding of how to use Finite State Machines to manage different states and behaviors of an NPC.
- Ensure that your code is well-commented, explaining the logic behind each part of your implementation, and follows best practices for error handling.

### Integration
This exercise is structured to facilitate your learning through project-based tasks, which aligns with your preferred learning format. Make sure to test your code thoroughly and consider sharing your completed project in community forums for feedback and support.