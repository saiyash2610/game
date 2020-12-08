# game Casino
def replay():
    
    return input('Do you want to play again? Enter Yes or No: ').lower().startswith('y')


import random
print("Welcom to casino!!!!!")
while True:
    no=random.randint(1,36)
    

    chips=int(input('enter chips do you want to bet:\n'))
    get_choice=''
    
    while not(get_choice=='1' or get_choice=='2' or get_choice=='3' or get_choice=='4' or get_choice=='5'):
            get_choice=input("Which Bet You Want to Place\nenter your bet\n1)Exact Number\n2)Number is EVEN\n3)Number is ODD\n4)Number is in between 1-18\n5)Number in between 19-36\n")
               
        
    if get_choice=='1':
            choice=int(input('enter your number do yo want to bet:\n '))
            if choice==no:
                print(f"Yes, Number is Exact you guess {no}\nYou Won the bet")
                chips=chips*36
                print(f'Now You have {chips} chips')
                
            else:
                print(f"Sorry, Number is {no}\nYou loss the bet")
                chips=chips*0
                print(f'Now You have {chips} chips')
            
            
    elif get_choice=='2':
            if no%2==0:
                print(f"Yes, Number {no} is EVEN\nYou won the bet")
                chips=chips*18
                print(f'Now You have {chips} chips')
            else:
                print(f"Sorry, Number {no} is ODD\nYou loss the bet")
                chips=chips*0
                print(f'Now You have {chips} chips')

    elif get_choice=='3':
            if no%2!=0:
                print(f"Yes, Number {no} is ODD\nYou won the bet")
                chips=chips*18
                print(f'Now have {chips} chips')
            else:
                print(f"Sorry, Number {no} is EVEN\nYou loss the bet")
                chips=chips*0
                print(f'Now You have {chips} chips')
        
    elif get_choice=='4':
            if no in range(1,18):
                print(f"Yes Number {no} in between 1-18\nYou won the bet")
                chips=chips*9
                print(f'Now You have {chips} chips')
            else:
                print(f"Sorry, Number {no} is not in between 1-18\nYou loss the bet")
                chips=chips*0
                print(f'Now You have {chips} chips')
    elif get_choice=='5':
            if no in range(19,36):
                print(f"Yes Number {no} is between 19-36\nYou won the bet")
                chips=chips*9
                print(f'You have {chips} chips')
            else:
                print(f"Sorry, Number {no} is not in between 19-36\nYou loss the bet")
                chips=chips*0
                print(f'You have {chips} chips')
    if not replay():
        break
