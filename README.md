
##Number Guessing Game:


import random
# Function to start the game
def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 100.")
    print("Can you guess what it is?")

    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    
    # Variable to track the number of attempts
    attempts = 0
    
    # Loop until the user guesses the correct number
    while True:
        # Get the player's guess
        guess = input("Enter your guess (between 1 and 100): ")
        
        # Check if the input is a valid number
        if not guess.isdigit():
            print("Please enter a valid number.")
            continue
        
        # Convert the input to an integer
        guess = int(guess)
        
        # Increase the attempt count
        attempts += 1
        
        # Check the guess and provide feedback
        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You guessed the correct number {secret_number} in {attempts} attempts.")
            break

# Call the function to start the game
number_guessing_game()
