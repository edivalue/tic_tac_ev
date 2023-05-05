# Tic_tac_ev
A Command Line implementation of the classic two-player game with a user-friendly interface."

## INTRODUCTION

This is a simple implementation of the classic Tic Tac Toe board game written in Python version 3.x. The game is played on a 3x3 board, where players takes turns placing their marks (X or O) on an empty cell until one player gets three marks in a row (Horzontally, Vertically or Diagonally) or all the cells are filled up.

## HOW TO PLAY

Run the script in an IDE or CLi. 

The game will start by projecting a prompt: 'Do you want to be X or O?'
Pick a letter either: X or O, then the 1st player to start is selected at random.
The game will start by projecting an clean 3x3 board with numbered cells:

    1|2|3
    -+-+-
    4|5|6
    -+-+-  
    7|8|9
    
[+] Player 1 will be prompted to enter a cell number to place their mark.

[+] Player 2 will be prompted to enter a cell number to place their mark.

[+] Steps 3 and 4 will be repeated until one player gets three marks in a row or all cells are filled.

[+] If a player gets three marks in a row, they win the game. If all cells are filled and no player has won, the game comes to a tie.

## CODE STRUCTURE
The script consists of the following functions:

[+] drawBoard() : This function prints out the `board` that it was passed and print the current state of the `board`.	

[+] inputPlayerLetter() : Lets the player type which `letter` they want to be. Randomises a list with the player's `letter` as one item, and the computer's `letter` as the other.

[+] whoGoesFirst() : Randomly chooses the `player` who goes first.

[+] makeMove() : Contains the attributes of `board`, `letter` and `move`

[+] isWinner() : Given a `board` and a player's `letter`, this function returns True if that player has won.

[+] getBoardCopy() : Make a copy of the `board` list and return it.

[+] isSpaceFree() : Return true if the passed move is free on the passed `board`.

[+] getPlayerMove() : Let the `player` type in their move.

[+] chooseRandomMoveFromList() : Returns a valid move from the passed list on the passed `board` and returns None if there is no valid move.

[+] getComputerMove() : Given a `board` and the computer's `letter`, determine where to move and return that move.

[+] isBoardFull() : Checks if the `board` is full via the `isSpaceFree()` function


## FUNCTIONALITY

The script uses only `if-else` statements and `while` loops to implement the game logic. Each player's move is validated by checking that the selected cell is empty and within the valid range of 1 to 9. If the move is valid, the `board` is updated with the player's mark and the `player` variable is toggled. After each move, the script checks for winning conditions by checking all possible combinations of three marks in a row. If a winning condition is found, the `winner` variable is updated with the winning player's mark, and the game loop is exited. `board`, `player`, and `winner` to keep track of the state of the game.

`while loop` repeatedly prompts players to enter a cell number and update the `board` until a `winner` is found or all cells are filled.
`if-else statements` to check for winning conditions and update the `winner` variable.

## LIMITATIONS

[+] It only allows a single player to play.

[+] It does not include any AI algorithm.

[+] It does not have any graphical user interface (GUI) and is played entirely in the console/terminal.
