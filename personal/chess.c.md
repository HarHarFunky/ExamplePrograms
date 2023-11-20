# chess.c
  A C Chess Program
  
  - [x] [Representing](#Representing)
  - [ ] [Interactions](#Interactions)
  - [ ] [Moveset](#Moveset)
  - [ ] [Interpretations](#Interpretations)





## Representing
  In C, one of the most important things is memory management, so we must find a minimal way to represent all 32 pieces on the chess board in a manner that is small, but the computer can still work with.
  
  ### Representing the chess board
  The easiest method to represent a chess board in C would be to list out the position of the two kings, followed by 2 flags for if the game is still playable and whose turn it is, finally followed by all the pieces coordinates and, if they are not pawns, what pieces they are.
  
  This method will take up—at most—270 bits, and will start out as 238 bits in size.


  
  ### Representing the playbook
  A playbook in chess is the moves that one may use given the opponent doing various moves

  Given the goal of having a look-up table esque a "history reduction" formula has been devised:
  For any given string of moves, set a flag to show the turn and an unsigned short to show the history length. Iterate through every move on the board—collapsing boards already made into pointers to their predecessors and removing them from the iteration queue—until either a board is found that mirrors the desired board, or the move span has reached the history length.  

  The size that the playbook may reach is unknown, but is likely to be the determining factor for this project.





## Interactions





## Moveset





## Interpretations
