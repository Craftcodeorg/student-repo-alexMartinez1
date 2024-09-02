# Module Title: Introduction to Python Programming

## Example 5: Defining a Function

### 1. Introduction
In this section, we will delve into the concept of defining functions in Python, as covered in Lecture 5: Functions and Modules. Functions are essential building blocks in programming that allow developers to encapsulate code into reusable segments. This is particularly significant in game development, where functions can automate repetitive tasks, manage game mechanics, and enhance code organization. By mastering functions, you will be able to create more efficient and maintainable game code.

### 2. Code Snippet
Here’s a simple code snippet demonstrating how to define and use a function in Python for a game scenario:

```python
# score_module.py

def calculate_score(items_collected, level):
    """
    Calculate the score based on items collected and the level of difficulty.
    
    Parameters:
    items_collected (int): The number of items collected by the player.
    level (int): The current level of difficulty.

    Returns:
    int: The total score calculated.
    """
    try:
        # Ensure inputs are positive integers
        if items_collected < 0 or level < 0:
            raise ValueError("Items collected and level must be non-negative.")
        
        score = items_collected * level
        return score

    except TypeError:
        print("Invalid input type. Please enter integers only.")
        return 0

# main.py
import score_module

# Example usage
items = 5
difficulty_level = 3
total_score = score_module.calculate_score(items, difficulty_level)
print(f"Total Score: {total_score}")  # Output: Total Score: 15
```

### 3. Explanation
Let’s break down the code snippet step-by-step:

- **Function Definition**: 
  - The function `calculate_score` is defined to take two parameters: `items_collected` and `level`. 
  - It includes a docstring that explains what the function does, its parameters, and its return value.

- **Error Handling**:
  - The function checks if the inputs are non-negative integers. If they are not, it raises a `ValueError` with an appropriate message.
  - A `try-except` block is used to catch `TypeError`, ensuring that only integers are processed.

- **Score Calculation**:
  - The score is calculated by multiplying the number of items collected by the level of difficulty.
  - The calculated score is then returned.

- **Module Importing**:
  - In `main.py`, we import the `score_module` and call the `calculate_score` function with example values for items and difficulty level.

- **Output**:
  - The total score is printed, demonstrating how the function works in a real-world scenario.

### 4. Application
In gaming, functions like `calculate_score` are commonly used to manage scoring systems. They allow developers to create a structured approach to calculating scores based on various game mechanics, such as collecting items or completing levels. This modular approach not only improves code readability but also allows for easier updates and maintenance.

For example, if you want to change how scores are calculated (e.g., adding bonuses for certain achievements), you can simply modify the function without affecting other parts of the game code. This flexibility is crucial in game development, where mechanics often evolve during the development process.

### Summary
By understanding how to define and use functions in Python, you will be equipped with a powerful tool for creating organized and efficient game code. Functions enhance your ability to tackle complex problems in game development while promoting code reuse and maintainability.

### Next Steps
As you continue your learning journey, focus on practicing these concepts through interactive tutorials and community projects. In our next lecture, we will explore Object-Oriented Programming (OOP) in Python, which will further enhance your ability to design complex game systems and characters. Prepare by reviewing the basics of classes and objects!