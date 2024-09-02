### Module Title: Advanced Game Development Techniques

### Exercise Requirements 

#### 1. Problem Statement:
Create a Python script that allows an NPC (Non-Player Character) to follow the player character as they move around the game environment. The NPC should be able to switch between patrolling and chasing states based on the distance from the player, demonstrating the concepts of AI learned in the lecture.

**Scenario**: You are developing a simple 2D game where the player can move freely within a defined area. The NPC should patrol this area and chase the player when they come within a certain distance. Your task is to implement this behavior using a finite state machine (FSM) approach.

#### 2. Fill-in-the-Blank Starter Code:
```python
# Starter code for implementing NPC behavior based on player distance

class NPC:
    def __init__(self):
        self.state = 'patrol'  # Initial state of the NPC

    def update(self, player_distance):
        # Update the NPC state based on the player's distance
        if player_distance < ____:  # Fill in the distance threshold for chasing
            self.state = 'chase'
        else:
            self.state = 'patrol'
        
        # Print the current state of the NPC
        print(f"NPC is currently in {self.state} state.")

# Simulating the NPC behavior
npc = NPC()

# Simulating player distances
npc.update(____)  # Fill in a value to simulate player being close
npc.update(____)  # Fill in a value to simulate player being far
```

#### 3. Hints:
- **Hint 1**: Think about how close the player should be for the NPC to start chasing them. This is usually a smaller number than the distance at which they will patrol.
- **Hint 2**: Use realistic distances that make sense in a game environment. For example, if your game is set in a small room, a distance of 5 units might be appropriate for switching states.
- **Hint 3**: Remember to consider what happens when the player moves away from the NPC. What should happen to the NPC's state then?
- **Hint 4**: When testing your code, try different values for player distances to see how the NPC responds.

#### 4. Expected Outcome:
The student should fill in the blanks correctly, demonstrating an understanding of how to implement AI behavior in games. The final solution should:
- Allow the NPC to switch between 'patrol' and 'chase' states based on player distance.
- Include error handling (if applicable) and be well-commented to explain each part of the code.
- Show clear output indicating the current state of the NPC as it reacts to changes in player distance.

### Integration 
- Ensure this exercise is structured with clear headings and sections for easy navigation.
- Use markdown formatting for clarity.
- Encourage students to test their code with various scenarios and share their results in a community forum for feedback and support.