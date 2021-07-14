import random
print("Welcome to the Dice Roller!")
for row in range(9):  # Printing Dice formation
    for col in range(14):
        if row in {0, 8} and col in range(14):
            print("-", end=" ")
        elif col in {0, 13} and row in range(9):
            print("|", end=" ")
        elif col == 6 and row == 4:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()
while True:
    a = [1, 2, 3, 4, 5, 6]
    nod = random.choice(a)  # nod = number on dice
    for row in range(5):  # Printing Dice formation
        for col in range(7):
            if row in {0, 4} and col in range(7):
                print("-", end=" ")
            elif col in {0, 6} and row in range(5):
                print("|", end=" ")
            elif col == 3 and row == 2:
                print(nod, end=" ")
            else:
                print(" ", end=" ")
        print()
# taking input to check user want to roll or not
    st = input("If you want to roll again press 'y' else press 'any key': ")
    if st.lower()[0] not in "y":  # for exiting loop
        break
