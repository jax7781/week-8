# week-8
Scripts for Week 8
import math

def newton(number):
    """
    Approximates the square root of a given number using Newton's method.
    """
    guess = number / 2  # Start with an initial guess
    
    while True:
        new_guess = (guess + number / guess) / 2  # Update the guess using the Newton's method formula
        if abs(new_guess - guess) < 0.0001:  # Check for convergence
            return new_guess
        guess = new_guess

def main():
    """
    Allows the user to compute square roots using Newton's method.
    """
    while True:
        user_input = input("Enter a number to compute its square root (or press Enter/Return to quit): ")
        if user_input == "":
            break
        
        number = float(user_input)
        if number < 0:
            print("Error: Square root of a negative number is not defined.")
        else:A
            result = newton(number)
            print(f"The square root of {number} is approximately {result:.4f}")

# Run the main function
if __name__ == "__main__":
    main()

def newton(number, estimate):
    """
    Recursive function that approximates the square root of a given number using Newton's method.
    """
    new_estimate = (estimate + number / estimate) / 2  # Update the estimate using the Newton's method formula
    
    if abs(new_estimate - estimate) < 0.0001:  # Check for convergence
        return new_estimate
    else:
        return newton(number, new_estimate)  # Recursively call the function with the updated estimate

def main():
    """
    Allows the user to compute square roots using Newton's method.
    """
    while True:
        user_input = input("Enter a number to compute its square root (or press Enter/Return to quit): ")
        if user_input == "":
            break
        
        number = float(user_input)
        if number < 0:
            print("Error: Square root of a negative number is not defined.")
        else:
            result = newton(number, number / 2)  # Start with an initial estimate of number / 2
            print(f"The square root of {number} is approximately {result:.4f}")

# Run the main function
if __name__ == "__main__":
    main()

def newton(number, estimate=None):
    """
    Recursive function that approximates the square root of a given number using Newton's method.
    """
    if estimate is None:
        estimate = number / 2  # Default estimate value if not provided
        
    new_estimate = (estimate + number / estimate) / 2  # Update the estimate using the Newton's method formula
    
    if abs(new_estimate - estimate) < 0.0001:  # Check for convergence
        return new_estimate
    else:
        return newton(number, new_estimate)  # Recursively call the function with the updated estimate

def main():
    """
    Allows the user to compute square roots using Newton's method.
    """
    while True:
        user_input = input("Enter a number to compute its square root (or press Enter/Return to quit): ")
        if user_input == "":
            break
        
        number = float(user_input)
        if number < 0:
            print("Error: Square root of a negative number is not defined.")
        else:
            result = newton(number)  # Call the function without a second argument
            print(f"The square root of {number} is approximately {result:.4f}")

# Run the main function
if __name__ == "__main__":
    main()
