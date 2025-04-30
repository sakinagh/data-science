Intro Data Science
Lab 4: Unsupervised Collective Learning System with Tic Tac Toe

This lab is coded using Python in lab4.ipynb.

There are 7 code cells in the Python notebook, which should be run in order.

Code cell 1: This cell imports all the libraries used in the program.

Code cell 2: This cell defines global variables that are referenced throughout the program. Many of them have their values changed or reassigned in different cells.
 - spaceMapping: a dictionary mapping the visual board spaces to the logical state space
 - state: the current state of the current game, represented as a 9-char String
 - turn: the number of moves that have been made by both sides in the current game
 - winStates: a dictionary of regex's representing states with 3-in-a-row for 'x' or 'o'
 - stateJournal: a log of encountered states and corresponding decisions by the program for the current game

Code cell 3: This cell defines all the functions for the program, which get called multiple times in other cells.
 - assignSpaces(): maps the visual board spaces to the logical state space by updating spaceMapping; called once per game when the first non-center move is made
 - showBoard(): prints the board with the current moves in an easily readable visual format; called each time the person has to make a move and at the end of the game
 - move(): defines the behavior of each player (computer and human) and calls the appropriate supporting functions
 - decide(): implements the move selection process for the computer, using the STM
 - learn(): implements the algedonic learning algorithm, updating move probabilities in the STM based on game results
 - checkWin(): determines if the current game state is a winning state
 - branch(): finds all the possible next states from a given state

Code cell 4: Other functions for the learning algorithm.
 - build_stm(): builds the entire State Transition Matrix for Tic Tac Toe before the game starts
 - print_stm(): prints the State Transition Matrix

Code cell 5: This cell defines the betaReward and betaPunish variables, and then calls playGame() to begin.

Code cell 6: This cell defines the playGame() function, which initializes all the variables for a new game, calls build_stm() to generate the complete STM, and runs the game loop until a win or tie.

Code cell 7: This cell defines the print_stm() function, which prints the entire State Transition Matrix (or a selected state, if desired)
