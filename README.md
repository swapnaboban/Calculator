# Calculator
First python code


import os
import platform
import time


def clear_screen():
    if platform.system() == "Windows":
        os.system('cls')

    else:
        os.system('clear')


while True:
    clear_screen()
    print("\nHello Welcome to Home Made Calculator")
    print("******What would you like to do******")
    print("1. To Add Two Values")
    print("2. To Subtract Two values")
    print("3. To Multiply Two values")
    print("4. To Divide Two values")
    print("5. To Find Percentage")
    print("6. Exit")
    choice = int(
        input("Enter the corresponding number next to you dicided choice: "))

    if choice == 6:
        clear_screen()
        print("\nThank You For using the calculator.")
        time.sleep(2)
        break

    elif choice in [1, 2, 3, 4, 5]:
        clear_screen()
        while True:
            if choice == 1:
                print("You Are Adding!")
            if choice == 2:
                print("You Are Subtracting!")
            if choice == 3:
                print("You Are Multiplying!")
            if choice == 4:
                print("You Are Dividing!")
            if choice == 5:
                print("You Are Finding Percentage!")

            x = float(input("First Number: "))
            y = float(input("Second Number: "))

            if choice == 1:
                (z) = x + y
                print("Result:", z)

            elif choice == 2:
                (z) = x - y
                print("Result:", z)

            elif choice == 3:
                z = x * y
                print("Result:", z)

            elif choice == 4:
                if y == 0:
                    print("You cannot Divide By zero :{")
                else:
                    z = x / y
                if z == 3.142857142857143:
                    print("Result:", z, "\n****HEYY ITS A PIEEE*****")
                else:
                    print("Result: ", z)

            elif choice == 5:
                z = x/100*y
                print("Results: ", z)
            go_back = input(
                "Whould You Like To Continue...(y/n): ").strip().lower()

            if go_back == 'n':
                break

            elif go_back == 'y':
                print("Repeating The Operation...")

            else:
                print("Invalid Choice,Repeating the opertation by defult\n")

    else:
        print("\nInvalid Choice, Choose the numbers 1-5 for operations")
        time.sleep(2)
        clear_screen()
