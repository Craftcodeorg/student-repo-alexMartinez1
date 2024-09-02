# Assignment: Create a Simple Calculator

## Problem Statement
In this assignment, you will create a simple calculator using Python functions that can perform addition, subtraction, multiplication, and division. This project will help you apply the core concepts of Python programming, including function creation and basic arithmetic operations, which are fundamental skills in game development. Understanding how to implement these basic functionalities will also enhance your ability to automate game mechanics and create interactive experiences in your future projects.

## Starter Code
Below is a basic framework for your calculator. You will need to complete the functions for each arithmetic operation and implement a user interface to interact with the calculator.

```python
# Starter code for a simple calculator

def add(x, y):
    # Step 1: Implement addition
    pass

def subtract(x, y):
    # Step 2: Implement subtraction
    pass

def multiply(x, y):
    # Step 3: Implement multiplication
    pass

def divide(x, y):
    # Step 4: Implement division
    if y == 0:
        return "Error! Division by zero."
    return x / y

def calculator():
    print("Welcome to the Simple Calculator!")
    print("Select operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")

    choice = input("Enter choice (1/2/3/4): ")

    # Step 5: Get user input for numbers
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    # Step 6: Call the appropriate function based on user choice
    if choice == '1':
        print(f"{num1} + {num2} = {add(num1, num2)}")
    elif choice == '2':
        print(f"{num1} - {num2} = {subtract(num1, num2)}")
    elif choice == '3':
        print(f"{num1} * {num2} = {multiply(num1, num2)}")
    elif choice == '4':
        print(f"{num1} / {num2} = {divide(num1, num2)}")
    else:
        print("Invalid input")

# Uncomment the line below to run the calculator
# calculator()
```

## Detailed Instructions
1. **Step 1**: Implement the `add` function to return the sum of `x` and `y`.
   - Example: `return x + y`

2. **Step 2**: Implement the `subtract` function to return the difference between `x` and `y`.
   - Example: `return x - y`

3. **Step 3**: Implement the `multiply` function to return the product of `x` and `y`.
   - Example: `return x * y`

4. **Step 4**: Ensure the `divide` function handles division by zero by returning an error message when `y` is zero.

5. **Step 5**: In the `calculator` function, prompt the user for two numbers using `input()` and convert them to floats.

6. **Step 6**: Based on the user's choice, call the appropriate arithmetic function and display the result.

## Criteria for Success and Evaluation
- **Functionality**: The calculator must perform all four operations correctly (addition, subtraction, multiplication, division).
- **Error Handling**: The program should handle division by zero gracefully.
- **Code Quality**: Your code should be clean and well-documented with comments explaining each function's purpose.
- **User Experience**: The output should be clear and user-friendly, guiding users through their choices.

### Success Criteria:
- The calculator performs calculations accurately.
- The user interface is intuitive.
- Code is well-organized and follows Python best practices.

By completing this assignment, you will gain hands-on experience with Python functions and improve your coding skills, which are essential for your career goal of becoming a Python Developer in game development.