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

 print("Enter your option \n a - Rock \n b - Paper \n c - Scissors \n")

    # take the input from user

    option = int(input("Enter your option :"))

    # OR is the short-circuit operator
    # if any one of the condition is true
    # then return it True value

    # looping until user enter invalid input
    while option > c or option < a:
        option = int(input('Enter a valid option please ☺'))

        # initialize value of option_name variable
    # corresponding to the option value
    if option == a:
        option_name = 'Rock'
    elif option == b:
        option_name = 'Paper'
    else:
        option_name = 'Scissors'

        # print user option
    print('User choice is \n', option_name)
    print('Now its Computers Turn....')

    # Computer chooses randomly any number
    # among a , b and c. Using randint method
    # of random module
    comp_option = random.randint(a, c)

    # looping until comp_option value
    # is equal to the option value
    while comp_option == option:
        comp_option = random.randint(a, c)

    # initialize value of comp_option_name
    # variable corresponding to the option value
    if comp_option == a:
        comp_option_name = 'rocK'
    elif comp_option == b:
        comp_option_name = 'paper'
    else:
        comp_option_name = 'scissor'
    print("Computer option is \n", comp_option_name)
    print(option_name, 'Vs', comp_option_name)
    # we need to check of a draw
    if option == comp_option:
        print('Its a Draw', end="")
        result = "DRAW"

    # condition for winning
    if(option == a and comp_option == b):
        print('paper wins =>', end="")
        result = 'paper'
    elif (option == b and comp_option == a):
        print('paper wins =>', end="")
        result = 'Paper'

    if (option == a and comp_option == c):
        print('Rock wins =>\n', end="")
        result = 'Rock'
    elif (option == c and comp_option == a):
        print('Rock wins =>\n', end="")
        result = 'rock'

    if (option == b and comp_option == c):
        print('Scissors wins =>', end="")
        result = 'scissoR'
    elif (option == c and comp_option == b):
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
