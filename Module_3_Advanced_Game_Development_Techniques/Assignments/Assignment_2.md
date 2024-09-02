# Assignment: Create a Branching Narrative Game with NPC Behavior

## Problem Statement:
Design and implement a branching narrative game in Python that features Non-Playable Characters (NPCs) whose behaviors change based on player choices. The game should have multiple endings determined by the player's decisions throughout the gameplay. This assignment focuses on applying the concepts of Finite State Machines (FSM) and Behavior Trees discussed in the lecture on NPC behavior.

## Starter Code:
Below is a basic framework for your branching narrative game. You will need to expand upon this code to implement your NPC behaviors and the branching narrative logic.

```python
class NPC:
    def __init__(self, name):
        self.name = name
        self.state = 'neutral'  # Possible states: neutral, happy, angry

    def interact(self, choice):
        if choice == 'greet':
            self.state = 'happy'
            print(f"{self.name} smiles at you.")
        elif choice == 'insult':
            self.state = 'angry'
            print(f"{self.name} glares at you.")
        else:
            print(f"{self.name} is confused by your choice.")

    def get_state(self):
        return self.state

def start_game():
    print("Welcome to the branching narrative game!")
    player_choice = input("Do you want to greet or insult the NPC? (greet/insult): ")
    
    npc = NPC("Alex")
    npc.interact(player_choice)

    # Branching narrative based on NPC state
    if npc.get_state() == 'happy':
        print("You made a new friend! The story continues happily.")
        # Add more branching narrative here
    elif npc.get_state() == 'angry':
        print("The NPC is upset with you. The story takes a dark turn.")
        # Add more branching narrative here
    else:
        print("The story ends abruptly.")

# Start the game
start_game()
```

## Detailed Instructions:
1. **Implement NPC States**: 
   - Modify the `NPC` class to include more states that reflect different moods or behaviors (e.g., curious, frightened).
   - Update the `interact` method to handle more choices and corresponding state changes.

2. **Branching Narrative Logic**:
   - After the interaction with the NPC, create additional choices for the player based on the NPC's current state.
   - Implement conditional statements to determine which narrative path the player will take based on their choices and the NPC's state.

3. **Expand the Game**:
   - Add more NPCs with unique names and behaviors.
   - Create a more complex storyline with multiple branches leading to different endings.
   - Consider using a simple text file or data structure to manage the narrative flow and choices.

4. **Testing**:
   - Test your game to ensure all paths lead to appropriate endings based on player choices.
   - Ensure that NPC behavior reflects changes accurately based on interactions.

## Criteria for Success and Evaluation:
- **Functionality**: The game should run without errors and allow players to make choices that influence the outcome.
- **NPC Behavior**: NPCs should exhibit different behaviors based on player interactions, demonstrating an understanding of FSM or Behavior Trees.
- **Narrative Depth**: The branching paths should provide meaningful choices that lead to diverse endings.
- **Code Quality**: The code should be well-organized, readable, and documented with comments explaining each part of the logic.
- **User Experience**: The game should be engaging, with clear prompts and feedback for player actions.

### Example Evaluation Rubric:
| Criteria                     | Excellent (5) | Good (4) | Fair (3) | Poor (2) | Unacceptable (1) |
|------------------------------|---------------|----------|----------|----------|------------------|
| Functionality                | Runs flawlessly; all paths work | Minor issues; most paths work | Some paths do not work | Major issues; few paths work | Does not run |
| NPC Behavior                 | Dynamic and responsive | Mostly responsive | Limited responsiveness | Little to no responsiveness | No behavior changes |
| Narrative Depth              | Rich with choices and endings | Good variety of choices | Some choices lead to different outcomes | Few choices; limited endings | No branching narrative |
| Code Quality                 | Clean, well-documented | Mostly clean; some comments | Some organization; few comments | Disorganized; hard to follow | Very poor quality |
| User Experience              | Highly engaging and intuitive | Mostly engaging; minor issues | Somewhat engaging; unclear prompts | Unengaging; confusing prompts | Very poor experience |

This assignment will help you apply the concepts learned in the lecture while allowing you to create a project that showcases your skills in Python game development and interactive storytelling. Good luck!