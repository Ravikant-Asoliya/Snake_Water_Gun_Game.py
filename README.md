# Snake_Water_Gun_Game.py
# This Game made by Ravikant Asoliya

import random

print("\t\t\t\tWelcome to Smake Water Gun Game\n")
print("Instructions : ------")
print("1. If you choose Snake and computer choose Gun then computer win because snake killed by gun")
print("2. If you choose Snake and computer choose Water then you win because snake will drink water")
print("3. If you choose Gun and computer choose Water then computer win because ")
print("\t1. Type snake for Snake \n\t2. Type water for Water \n\t3. Type gun for Gun")

computer_score = 0
chance = 1
user_score = 0
game_draw = 0
total_chances = 10

while total_chances >= 1:
    print(f"\nYou have remaining {total_chances} chance")
    computer_choice = random.choice(["snake", "water", "gun"])
    user_choice = input("Enter : ")
    if computer_choice == "snake" and user_choice == "water":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Loose")
        computer_score += 1

    elif computer_choice == "snake" and user_choice == "gun":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Win")
        user_score += 1

    elif computer_choice == "water" and user_choice == "snake":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Win")
        user_score += 1

    elif computer_choice == "water" and user_choice == "gun":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Loose")
        computer_score += 1

    elif computer_choice == "gun" and user_choice == "snake":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Loose")
        computer_score += 1

    elif computer_choice == "gun" and user_choice == "water":
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("You Win")
        user_score += 1

    elif computer_choice == user_choice:
        print(
            f"you choose {user_choice} and computer choose {computer_choice}")
        print("Game Draw")
        game_draw += 1

    else:
        print("Invalid choice!\nTry Again")
        computer_score += 1
    total_chances -= 1

if user_score < computer_score:
    print(
        f"\nyour score is {user_score} and computer score is {computer_score} and game draw {game_draw} times")
    print("Final score:-- You Loose")
    
elif user_score > computer_score:
    print(
        f"\nyour score is {user_score} and computer score is {computer_score} and game draw {game_draw} times")
    print("Final score:-- You win")
    
else:
    print(
        f"\nyour score is {user_score} and computer score is {computer_score} and game draw {game_draw} times")
    print("Final score:-- Match Draw")
