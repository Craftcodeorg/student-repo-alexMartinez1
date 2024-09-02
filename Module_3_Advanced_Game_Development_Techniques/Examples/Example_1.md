# Module Title: Advanced Game Development Techniques

## Example 1: Implementing Basic NPC Movement

### 1. Introduction
In this example, we will explore the implementation of basic Non-Player Character (NPC) movement using concepts introduced in the lecture "Introduction to AI in Games." Understanding NPC movement is a foundational skill for any game developer, as it enhances the interactivity and realism of gameplay. By implementing simple AI behaviors, such as patrolling and chasing the player, you will gain practical experience in coding NPC actions, which is crucial for your journey in game development.

### 2. Code Snippet
Here is a well-commented Python code snippet that demonstrates basic NPC movement using a Finite State Machine (FSM):

```python
class NPC:
    def __init__(self):
        # Initialize the NPC's state to 'patrol'
        self.state = 'patrol'
    
    def update(self, player_distance):
        """
        Update the NPC's state based on the distance to the player.
        
        Parameters:
        player_distance (float): The distance between the NPC and the player.
        """
        try:
            # Check if the player is within a certain distance
            if player_distance < 5:  # If player is close
                self.state = 'chase'  # Change state to chase
            else:
                self.state = 'patrol'  # Change state to patrol
            
            # Print the current state of the NPC
            print(f"NPC is currently in '{self.state}' state.")
        
        except Exception as e:
            print(f"An error occurred: {e}")

# Simulating the NPC behavior
npc = NPC()
npc.update(3)  # Simulate player being close
npc.update(10) # Simulate player being far
```

### 3. Explanation
Let's break down the code step-by-step:

- **Class Definition**: We define a class `NPC` to represent our non-player character. This encapsulates all properties and methods related to the NPC.

- **Initialization**: The `__init__` method initializes the NPC's state to 'patrol'. This sets the default behavior of the NPC when it is created.

- **Update Method**: The `update` method takes `player_distance` as an argument, which represents how far the player is from the NPC. Inside this method:
  - We use a `try` block to handle any potential exceptions that may arise during execution.
  - We check if `player_distance` is less than 5. If true, it changes the state to 'chase', indicating that the NPC will pursue the player.
  - If the player is farther away, it reverts back to 'patrol'.
  - Finally, it prints the current state of the NPC.

- **Error Handling**: The `try-except` block ensures that if an error occurs (for example, if a non-numeric value is passed), it will be caught and a message will be printed instead of crashing the program.

### 4. Application
In real-world gaming scenarios, implementing basic NPC movement is crucial for creating engaging gameplay experiences. For instance, consider a stealth game where players must avoid detection by patrolling guards. By using simple AI like FSMs, developers can create realistic behaviors where guards switch between patrolling and chasing players based on proximity. This not only enhances immersion but also challenges players to strategize their movements effectively.

Moreover, such implementations can be extended with more complex behaviors, such as adding animations or sound effects when transitioning states, thereby enriching the overall gameplay experience.

### Conclusion
In this example, we have demonstrated how to implement basic NPC movement using Python. By understanding and applying these fundamental AI concepts, you are taking significant steps toward achieving your goal of becoming a proficient Python Developer in game development. Remember to practice by creating your own variations of this code and experimenting with different states and behaviors for your NPCs!