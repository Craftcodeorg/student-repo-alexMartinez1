### Assignment: Build an AI-driven NPC that Reacts to Player Actions in Real-Time

#### Problem Statement:
Create an AI-driven Non-Player Character (NPC) that patrols a designated area and reacts to the player's actions. The NPC should switch between different states (patrol, chase, and idle) based on the player's proximity. This assignment will help you apply the concepts of Finite State Machines (FSM) and basic AI behavior learned in the lecture, reinforcing your understanding of how AI can enhance gameplay.

#### Starter Code:
Below is a basic framework for your NPC. You will need to expand upon this code to implement the desired behaviors.

```python
# Starter code for AI-driven NPC behavior

class NPC:
    def __init__(self):
        self.state = 'patrol'  # Initial state of the NPC
        self.patrol_area = [(0, 0), (5, 0), (5, 5), (0, 5)]  # Define patrol area corners
        self.position = self.patrol_area[0]  # Start at the first corner of the patrol area

    def update(self, player_distance):
        # Step 1: Update NPC state based on player distance
        if player_distance < 5:  # If player is within 5 units
            self.state = 'chase'
        elif player_distance > 10:  # If player is further than 10 units
            self.state = 'patrol'
        else:
            self.state = 'idle'  # If player is between 5 and 10 units
        
        # Step 2: Print current state
        print(f"NPC is currently in {self.state} state.")

    def patrol(self):
        # Step 3: Implement patrol behavior
        # Move to the next corner in the patrol area
        current_index = self.patrol_area.index(self.position)
        next_index = (current_index + 1) % len(self.patrol_area)
        self.position = self.patrol_area[next_index]
        print(f"NPC moved to position: {self.position}")

# Simulating the NPC behavior
npc = NPC()
npc.update(3)  # Simulate player being close
npc.patrol()    # NPC should patrol to the next position
npc.update(7)   # Simulate player being at a medium distance
npc.patrol()    # NPC should continue patrolling
npc.update(12)  # Simulate player being far away
```

#### Detailed Instructions:
1. **Step 1: Modify the `update` method** to include a print statement that outputs the player's distance. This will help you understand how the NPC's state changes based on player proximity.

2. **Step 2: Implement the `patrol` method**. In this method, make the NPC move between defined corners of its patrol area. Use the `self.position` attribute to track where the NPC currently is.

3. **Step 3: Enhance the `update` method** to include logic for transitioning between states more smoothly. For example, if the player moves away from close proximity, ensure that the NPC transitions back to 'patrol' or 'idle' appropriately.

4. **Step 4: Add a main loop** that simulates player movements. Create a simple simulation where you randomly change the player's distance from the NPC and call `npc.update()` and `npc.patrol()` accordingly.

5. **Step 5: Test your code** thoroughly to ensure that all transitions between states work as expected. Make sure to print out the NPC's position and state after each update to verify its behavior.

#### Criteria for Success and Evaluation:
- **Functionality**: The NPC correctly transitions between states based on player distance.
- **Code Quality**: The code is clean, well-structured, and includes comments explaining each part.
- **Robustness**: The program handles various scenarios of player movement effectively.
- **User Feedback**: The output is clear and provides useful information about the NPC's actions and state changes.

By completing this assignment, you will gain hands-on experience with AI concepts in game development and enhance your coding skills in Python, aligning with your career goals in gaming.