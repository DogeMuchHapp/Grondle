## Welcome to Grondle

m&ms

### Ayo so basically right, my mans come up to me and go

Ay homesickle make me wordle but with grond so i go:

```
from colorama import init, Fore, Back
init()
word = "grond"
loop = True
while loop:
    print(Back.WHITE + Fore.BLACK + "Start a new game? (y/quit)")
    command = input()
    if command == "quit":
        loop = False
    elif command == "y":
        inner_loop = 0
        print("Enter a word")
        while inner_loop < 6:

            attempt = input()

            # Game logic
            output = ""
            for i in range(word.__len__()):
                if attempt[i] == word[i]:
                    output = output + Back.GREEN + attempt[i] + Back.RESET
                elif attempt[i] in word:
                    output = output + Back.YELLOW + attempt[i] + Back.RESET
                else:
                    output = output + attempt[i] + Back.RESET
            print(output)
            if word == attempt:
                print(Fore.WHITE + "Congrats")
                inner_loop = inner_loop + 6  # Reset game

            inner_loop = inner_loop + 1
