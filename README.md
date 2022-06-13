import random
print(" ****** ROCK PAPER SCISSORS  ******\n") 
#starting

while True:
    print("Enter Your choice \n 1. Rock \n 2. paper \n 3.scissors\n")
    c = int(input("User turn: "))
    while c > 3 or c< 1:
        c= int(input("Enter choice(1,2,3: "))
    if c == 1:
        name = 'Rock'
    elif c == 2:
        name = 'Paper'
    else:
        name = 'Scissors'
    print("User choice is: " + name)

    print("\n* Computer's choice *")
    cc = random.randint(1,3)
    while cc == c:
        cc = random.randint(1,3)
    if cc == 1:
        ccname = 'Rock'
    elif cc == 2:
        ccname = 'Paper'
    else:
        ccname = 'Scissors'
    print("Computer choice is: " + ccname)
    print("\n", name + " V/s " + ccname)
    if ((cc == 1 and cc == 2) or 
       ( c == 2 and cc == 1 )):
        print("Paper ", end = " wrap rock" )
        winner = "Paper"
    elif ((cc == 1 and cc == 3) or
          (c == 3 and cc ==1 )):
          print("Rock ", end = "smashes scissors")
          winner = "Rock"
    elif (cc == 1 and cc == 1 ):
         print("It's a tie")
    else:
        print('Scissors ', end = " cuts paper")
        winner = "Scissors"

    if winner == name:
        print(" User wins ")
    else:
        print(" computer wins ")
    print ("Do you want to play again? (Y/N)")
    sel = input()
    if sel == 'n' or sel == 'N':
        break
print("\nThank you for playing")
