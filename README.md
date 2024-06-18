import random

def guess_number_game():
    print("Welcome to the Guess the Number game!")
    print("I have picked a number between 1 and 100. Try to guess it!")
    
    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    
    # Initialize the number of attempts taken
    attempts = 0
    
    while True:
        try:
            # Ask the user to guess the number
            guess = int(input("Enter your guess (between 1 and 100): "))
            attempts += 1
            
            # Compare the guess with the secret number
            if guess < secret_number:
                print("Too low! Try guessing a higher number.")
            elif guess > secret_number:
                print("Too high! Try guessing a lower number.")
            else:
                print(f"Congratulations! You guessed the number {secret_number} correctly!")
                print(f"It took you {attempts} attempts.")
                break  # Exit the loop once the correct number is guessed
        
        except ValueError:
            print("Invalid input! Please enter a valid number.")

# Run the game
guess_number_game()


