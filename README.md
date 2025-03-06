NAME:Yakkala Sri Vyshnavi
COMPANY:Aldidotech
ID:BS/REG/101623
DOMAIN:Python Developer
DURATION:5th febrauary to 5th march 2025
Here’s a simple overview of how to build one:


---

1. Game Objective

The player tries to guess a randomly generated number within a specified range. The program provides feedback on whether the guess is too high, too low, or correct.


---

2. Key Components

1. Importing Libraries: Use the random module to generate a random number.


2. Set Range: Define the range (e.g., 1 to 100).


3. Generate Random Number: Use random.randint() to select a number.


4. User Input: Prompt the player to enter guesses.


5. Comparison: Check if the guess is:

Correct (Win)

Too high (Hint: "Try a lower number")

Too low (Hint: "Try a higher number")



6. Loop Until Win: Continue until the correct guess is made.


7. Feedback: Display the number of attempts when the player wins.


8. Replay Option (Optional): Ask if the player wants to play again.




---

3. Sample Code:

import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    lower_bound = 1
    upper_bound = 100
    
    # Generate random number
    secret_number = random.randint(lower_bound, upper_bound)
    attempts = 0
    
    print(f"I have chosen a number between {lower_bound} and {upper_bound}. Can you guess it?")
    
    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            if guess < lower_bound or guess > upper_bound:
                print(f"Please guess a number between {lower_bound} and {upper_bound}.")
            elif guess < secret_number:
                print("Too low! Try again.")
            elif guess > secret_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number {secret_number} in {attempts} attempts.")
                break
        
        except ValueError:
            print("Invalid input. Please enter a valid number.")
    
    # Option to play again
    play_again = input("Do you want to play again? (yes/no): ").strip().lower()
    if play_again == 'yes':
        number_guessing_game()
    else:
        print("Thanks for playing!")

number_guessing_game()


---

4. Customization Ideas

Difficulty Levels: Let the user select a range (e.g., Easy: 1-50, Hard: 1-1000).

Attempt Limit: Restrict the number of guesses (e.g., 10 attempts max).

Score System: Award points based on fewer attempts.

Hints: Give hints like "The number is even/odd."

Multiplayer Mode: Allow two players to compete for fewer guesses.


Would you like help expanding the game or adding any extra features?
