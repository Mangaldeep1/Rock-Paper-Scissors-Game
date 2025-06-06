# Rock-Paper-Scissors-Game
import random

choices = ["rock", "paper", "scissors"]
user_score = comp_score = 0

while True:
    user = input("Choose rock, paper, or scissors: ").lower()
    comp = random.choice(choices)
    
    print(f"You chose {user}, computer chose {comp}")
    
    if user == comp:
        print("It's a tie!")
    elif (user == "rock" and comp == "scissors") or \
         (user == "scissors" and comp == "paper") or \
         (user == "paper" and comp == "rock"):
        print("You win!")
        user_score += 1
    else:
        print("You lose!")
        comp_score += 1

    print(f"Score - You: {user_score}, Computer: {comp_score}")
    
    again = input("Play again? (y/n): ")
    if again.lower() != 'y':
        break

