# Python Number Guessing Game
A user friendly command-line guessing game built with python functions.No imports.
The challenge: Guess the secret number '3' in as few tries as possible.
## Features
-**Secret Number**: The number is set to '3' for this version
-**Try Counter**: Tracks how may guesses it took you to win
-**Play Again Loop**: Restart a new round without restarting the program
-**Input Validation**: Handles letters and symbols so the game does not crash or stop working
# Built With
-**Language**: Python 3
- **Tool**: Visual Studio Code
- **Concepts**: Functions, While loops, If/Else statements, Input validation, Code organization
# How to run

def number_guessing_game():
    # the function runs one round of the number guessing game.The number is set to 3. The player keeps guessing until correct.
    
    number_to_guess = 3
    tries =0
    print("=== Number Guessing Game ===")
    print("I'm thinking of a number between 1 and 10\n")

    while True:
        guess =input("Enter your guess:")
        #check if input is a number
        if not guess.isdigit():
            print("Please enter a number between 1-10")
            continue
        guess = int(guess)
        tries += 1
        if guess < number_to_guess:
            print("Too Low!")
        elif guess > number_to_guess:
            print("Too High!")
        else:
            print(f"\n CORRECT!You got it in {tries} tries!")
            break
def main():
    # this function handles playing again or quitting#
    while True:
        number_guessing_game()
        play_again = input("\nPlay again? y/n:").lower()
        if play_again !="y":
            print("Thanks for playing!")
            break
main()
