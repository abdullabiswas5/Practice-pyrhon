import random
print("Hi! welcome to the number Gussseing game.\nYou have 7 chances to guess the number.Let's Start!")
low = int(input("Enter the Lower Bound:"))
high = int(input("Enter the upper Bound:"))
print(f"\nYou have 7 chances to guess the number between{low} and {high}.\nLet's start!")
num = random.randint(low, high)
ch = 7
gc= 0
while gc<ch:
    gc+=1
    guess = int(input('Enter yout guess:'))
    if guess == num:
       print(f'Correct! The number is {num}. You gusseed it in {gc}attempts.')
       break
    elif gc>=ch and guess!=num:
        print(f'Sorry! The number was {num}. Better luck next time.')
    elif guess>num:
        print('Too high! Try a lower number.')
    elif guess<num:
        print('Too low! Try a higher number')
