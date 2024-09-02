# Assignment: Develop a Number Guessing Game

## Problem Statement
Create a simple number guessing game that prompts the user to guess a randomly generated number within a specified range. This assignment will help you apply your knowledge of user input, loops, and conditionals, as discussed in Lecture 2: Setting up the Python Environment. The game should provide feedback on whether the user's guess is too high, too low, or correct, and it should keep track of the number of attempts taken by the user.

## Starter Code
Below is a basic framework for the number guessing game. Your task is to build upon this code by adding the necessary logic to make the game functional.

```python
import random

def number_guessing_game():
    # Step 1: Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    attempts = 0
    guessed = False
    
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 100.")
    
    # Step 2: Create a loop that continues until the user guesses correctly
    while not guessed:
        # Step 3: Get user input
        guess = int(input("Enter your guess: "))
        attempts += 1
        
        # Step 4: Provide feedback on the guess
        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            guessed = True
            print(f"Congratulations! You've guessed the number {secret_number} in {attempts} attempts.")

# Call the function to start the game
number_guessing_game()
```

## Detailed Instructions
1. **Generate a Random Number**: The starter code already includes a line to generate a random number between 1 and 100. Ensure that this line remains in your final implementation.

2. **User Input**: Make sure that you handle user input correctly. Use the `input()` function to prompt the user for their guess and convert it to an integer.

3. **Loop Logic**: The game should continue to prompt the user for guesses until they correctly identify the secret number. You can use a `while` loop for this purpose.

4. **Feedback Mechanism**: Implement conditional statements (`if`, `elif`, `else`) to provide feedback based on the user's guess:
   - If the guess is lower than the secret number, print "Too low! Try again."
   - If the guess is higher than the secret number, print "Too high! Try again."
   - If the guess is correct, print a congratulatory message along with the number of attempts taken.

5. **Count Attempts**: Keep track of how many guesses the user has made by incrementing an `attempts` variable each time they make a guess.

## Criteria for Success and Evaluation
- **Functionality**: The game correctly generates a random number, accepts user input, provides appropriate feedback, and tracks the number of attempts.
- **Code Quality**: The code is clean, well-organized, and includes comments explaining each part of the process.
- **User Experience**: The game provides clear instructions and feedback to the user, ensuring an engaging experience.

### Success Criteria:
- The program runs without errors and successfully completes all game functionality.
- The output is clear and user-friendly, guiding the player through their guesses.
- The code follows best practices in terms of readability and structure.

By completing this assignment, you will gain practical experience in using loops, conditionals, and user input in Python, which are essential skills for your journey into game development. Good luck, and have fun coding your number guessing game!