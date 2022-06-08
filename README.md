# GAME
from pickle import TRUE
import random

OPTIONS = ["R","P", "S"]

while True:
    print("Play")
    user_choice = input (" Type R, P, or S: ")
    if user_choice in OPTIONS:
         computer_choice= random.choice(OPTIONS)
         print(
             f"\nYou threw '{user_choice}', the computer threw '{computer_choice}'"
             )
    else:
        print(f"\nYou typed '{user_choice}' not valid")

    if user_choice == computer_choice:
        print(f"Both players selected {user_choice}. It's a tie!")
    elif user_choice == "R":
        if computer_choice == "S":
            print("R smashes S! You win!")
        else:
            print("P covers rock! You lose.")
    elif user_choice == "P":
        if computer_choice == "R":
            print("P covers R! You win!")
        else:
            print("S cuts P! You lose.")
    elif user_choice == "S":
        if computer_choice == "P":
            print("S cuts paper! You win!")
    else:
        print("R smashes S! You lose.")

    again = input("\nWhat to play again? (yes or no): ")
    if again.lower()== "no":
        break
    
    print()

print("\nThank you for playing")

