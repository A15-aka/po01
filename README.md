import random

def guess_the_number():
    # Generate a random number between 1 and 100
    target = random.randint(1, 100)
    
    # Number of attempts
    attempts = 0
    
    print("Welcome to the Guess the Number game!")
    print("I have selected a number between 1 and 100.")
    print("Can you guess what it is?")
    
    while True:
        try:
            # Prompt the user to enter their guess
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            if guess < target:
                print("Too low! Try again.")
            elif guess > target:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the number {target} correctly in {attempts} attempts.")
                break
        except ValueError:
            print("Invalid input. Please enter a number.")

# Run the game
guess_the_number()
