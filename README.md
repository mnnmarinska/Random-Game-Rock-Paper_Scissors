# Random-Game-Rock-Paper_Scissors
import random

computer_counter = 0
player_counter = 0

#player_options = ['rock', 'paper', 'scissors']

computer_options = ['rock', 'paper', 'scissors']

while True:
    if computer_counter < 4 or player_counter < 4:
        player_choice = input("Your choice is: ")
        if player_choice != ['rock', 'paper', 'scissors']:
            print("Wrong command! Try again!")
            continue
        computer_choice = random.choice(computer_options)
        print(f"Computer choice is: {computer_choice}")

        if player_choice == computer_choice:
            print("Draw! Try again!")


        elif player_choice == 'rock' and computer_choice == 'paper':
            print("Computer won!")
            computer_counter += 1
        elif player_choice == 'rock' and computer_choice == 'scissors':
            print("You won!")
            player_counter += 1
        elif player_choice == 'scissors' and computer_choice == 'paper':
            print("You won!")
            player_counter += 1
        elif player_choice == 'scissors' and computer_choice == 'rock':
            print("Computer won!")
            computer_counter += 1
        elif player_choice == 'paper' and computer_choice == 'rock':
            print("Computer won!")
            computer_counter += 1
        elif player_choice == 'paper' and computer_choice == 'scissors':
            print("You won!")
            player_counter += 1

        if computer_counter == 3:
            print("Sorry! Computer won the game!")
        elif player_counter == 3:
            print("Congratulations! You won the game!")
            break


