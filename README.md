# Solitaire Game

## Overview
This is a C++ console-based implementation of the popular **Solitaire** card game (Klondike variant). The game involves a 52-card deck, and the objective is to build up four foundation piles, each representing one suit, in ascending order (Ace to King). The game offers two levels of difficulty, undo/redo functionality, a time limit, and a scoring system based on moves. 

## Features
- **Standard 52-Card Deck**: The deck consists of four suits (Hearts, Diamonds, Clubs, Spades) with 13 ranks in each (Ace to King).
  - Red suits: Hearts, Diamonds
  - Black suits: Spades, Clubs
- **Shuffling**: The deck is shuffled at the start of each game.
  
### Tableau (7 Columns)
- Seven columns are dealt, where:
  - The first pile has 1 card, the second pile has 2 cards, and so on up to the seventh pile (7 cards).
  - The top card in each pile is face-up, while the others are face-down.
  - Only Kings can fill empty piles.
  - Cards can be moved between tableau piles following alternating colors (red on black, black on red) and descending rank (one lower than the destination pile's top card).
  - If a face-down card is revealed after a move, it is flipped face-up.

### Foundation Piles (4 Piles)
- The goal is to build each foundation pile in ascending order from Ace to King for each suit.
  
### Stockpile
- The remaining cards are placed in a stockpile after dealing the tableau.
- Two levels of difficulty:
  - **Easy Level**: One-card draw from the stockpile.
  - **Hard Level**: Three-card draw, where only the top card is playable, and the next card can be accessed after the next draw cycle.

### Interface
- The game features an acceptable console interface displaying the tableau, stockpile, and foundation piles.

### Undo/Redo
- Players can undo and redo moves, with scoring adjustments for each action.

### Time Limit
- The game enforces a time limit for completion.

### Scoring System
- **Stockpile to Tableau**: +5 points
- **Sub-Deck to Foundation**: +10 points
- **Stockpile to Foundation**: +10 points
- **Three-card draw cycle (Hard level)**: -10 points per cycle
- **Undo a move**: -5 points

### Winning Condition
- The game ends when all four foundation piles are completed (Ace to King for each suit).

## How to Play
- **Moving Cards**: Cards can be moved between tableau piles, to the foundation piles, and from the stockpile according to the game rules described above.
- **Undo/Redo**: You can undo or redo moves, with points deducted for each undo.
- **Score**: The score is updated based on the player's moves, with penalties for cycles in three-card draw mode and for undoing moves.

