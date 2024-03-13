//Intern NITI Internship
//Task 1 - Rock,Paper and Scissor Game

# import random module
import random

# print multiline instruction
# perform string concatenation of string
print('Winning rules of the game ROCK PAPER SCISSORS are :\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissor wins \n")

while True:

 print("Enter your option \n 1 - Rock \n 2 - Paper \n 3 - Scissors \n")

    # take the input from user

    option = int(input("Enter your option :"))

    # OR is the short-circuit operator
    # if any one of the condition is true
    # then return it True value

    # looping until user enter invalid input
    while option > 3 or option < 1:
        option = int(input('Enter a valid option please ☺'))

        # initialize value of option_name variable
    # corresponding to the option value
    if option == 1:
        option_name = 'Rock'
    elif option == 2:
        option_name = 'Paper'
    else:
        option_name = 'Scissors'

        # print user option
    print('User choice is \n', option_name)
    print('Now its Computers Turn....')

    # Computer chooses randomly any number
    # among 1 , 2 and 3. Using randint method
    # of random module
    comp_option = random.randint(1, 3)

    # looping until comp_choice value
    # is equal to the choice value
    while comp_option == option:
        comp_option = random.randint(1, 3)

    # initialize value of comp_choice_name
    # variable corresponding to the choice value
    if comp_option == 1:
        comp_option_name = 'rocK'
    elif comp_option == 2:
        comp_option_name = 'papeR'
    else:
        comp_option_name = 'scissor'
    print("Computer option is \n", comp_option_name)
    print(option_name, 'Vs', comp_option_name)
    # we need to check of a draw
    if option == comp_option:
        print('Its a Draw', end="")
        result = "DRAW"

    # condition for winning
    if(option == 1 and comp_option == 2):
        print('paper wins =>', end="")
        result = 'papeR'
    elif (option == 2 and comp_option == 1):
        print('paper wins =>', end="")
        result = 'Paper'

    if (option == 1 and comp_option == 3):
        print('Rock wins =>\n', end="")
        result = 'Rock'
    elif (option == 3 and comp_option == 1):
        print('Rock wins =>\n', end="")
        result = 'rocK'

    if (option == 2 and comp_option == 3):
        print('Scissors wins =>', end="")
        result = 'scissoR'
    elif (option == 3 and comp_option == 2):
        print('Scissors wins =>', end="")
        result = 'Rock'

# Printing either user or computer wins or draw
    if result == 'DRAW':
        print("<== Its a tie ==>")
    if result == option_name:
        print("<== User wins ==>")
    else:
        print("<== Computer wins ==>")
    print("Do you want to play again? (Y/N)")
    # if user input n or N then condition is True
    ans = input().lower()
    if ans == 'n':
        break
# after coming out of the while loop
# we print thanks for playing
print("thanks for playing")
