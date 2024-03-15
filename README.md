rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
import random
# input function that lets the player choose rock, paper, or scissors
# 0 = rock, 1 = paper, 2 = scissors
# computer to generate random digit between 0 and 2, where the values are the same as above.
# if p choose 0 and computer choose 0, output draw, play again
# elif p choose 0 and computer choose 1, print computer wins
# elif p choose 0 and computer choose 2, print "you win"
# elif p choose 1
options = [rock, paper, scissors]

choose = int(
    input(
        "What do you choose? Type 0 for rock, 1 for paper, and 2 for scissors. \n"
    ))
if choose >= 3 or choose < 0:
    print("invalid input, try again")
else:
    print(options[choose])

computer = random.randint(0, 2)
print(f"computer chose " + options[computer])

if choose >= 3 or choose < 0:
    print("try again")
if choose == 0 and computer == 2:
    print("You win")
elif computer == 0 and choose == 2:
    print("you lose")
elif computer > choose:
    print("You lose")
elif choose > computer:
    print("you win")
elif computer == choose:
    print("Its a draw")
