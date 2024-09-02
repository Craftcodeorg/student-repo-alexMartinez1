# Lecture Title: 4. Control Structures: If Statements, Loops

## 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and apply the concepts of control structures in Python, specifically if statements and loops.
- Write conditional statements to control the flow of their programs.
- Implement loops to automate repetitive tasks in game development.
- Recognize how these concepts are used in game mechanics and AI behaviors.

## 2. Introduction:
Control structures are fundamental building blocks in programming that dictate how a program executes its code. In Python, the most common control structures are **if statements** and **loops** (for and while). For a Python Developer focusing on game development, mastering these structures is crucial as they allow you to create dynamic game mechanics, manage game states, and develop intelligent NPC (Non-Player Character) behaviors.

For instance, using if statements can help determine how a character reacts to player actions, while loops can automate tasks like enemy movement or background animations. Understanding these concepts will empower you to create more engaging and interactive storytelling experiences in your games.

## 3. Core Concepts:
### A. If Statements:
- **Definition**: An if statement evaluates a condition and executes a block of code if the condition is true.
- **Syntax**:
  ```python
  if condition:
      # code to execute if condition is true
  ```
- **Example**:
  ```python
  player_health = 50
  if player_health < 100:
      print("Player needs health!")
  ```

### B. Elif and Else:
- **Elif**: Short for "else if", allows you to check multiple conditions.
- **Else**: Executes code when none of the previous conditions are true.
- **Syntax**:
  ```python
  if condition1:
      # code
  elif condition2:
      # code
  else:
      # code
  ```
- **Example**:
  ```python
  score = 85
  if score >= 90:
      print("Grade: A")
  elif score >= 80:
      print("Grade: B")
  else:
      print("Grade: C")
  ```

### C. Loops:
- **For Loops**: Used to iterate over a sequence (like a list).
- **Syntax**:
  ```python
  for item in sequence:
      # code to execute for each item
  ```
- **Example**:
  ```python
  enemies = ["Goblin", "Troll", "Dragon"]
  for enemy in enemies:
      print(f"Defeated {enemy}!")
  ```

- **While Loops**: Continues executing as long as a condition is true.
- **Syntax**:
  ```python
  while condition:
      # code to execute
  ```
- **Example**:
  ```python
  health = 100
  while health > 0:
      print("Fighting!")
      health -= 10
  print("Game Over!")
  ```

## 4. Practical Application:
In game development, control structures are essential for creating interactive experiences. For example, an if statement can determine whether a player has collected enough points to unlock a new level. Here's a simple scenario:

```python
points = 150
if points >= 100:
    print("Level Unlocked!")
else:
    print("Collect more points!")
```

Loops can be used to create enemy AI that moves towards the player until they are close enough to attack:

```python
while enemy_distance > attack_range:
    move_towards_player()
```

## 5. Summary:
Today, we explored control structures in Python, focusing on if statements and loops. Remember that if statements allow you to make decisions in your code, while loops help you automate repetitive tasks. These concepts are vital for developing engaging game mechanics and AI behaviors.

## 6. Next Steps:
In our next lecture, we will dive into functions and how they can help organize your code and make it reusable—an essential skill for any aspiring Python Developer in game development. To prepare, consider reviewing your previous lectures on basic syntax and data types, as these will be crucial when we start defining our own functions.