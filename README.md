# AI Player with Minimax Algorithm

This project implements an AI player for a board game using the Minimax algorithm with alpha–beta pruning. The AI evaluates the current board state, predicts future moves, and dynamically adjusts its strategy to play intelligently against an opponent.

---

## Features

- **Minimax Algorithm**  
  Uses the classic Minimax algorithm enhanced with alpha–beta pruning to efficiently search the game tree and choose optimal moves.

- **Dynamic Strategy Adjustment**  
  Automatically adjusts the target number of consecutive marks (`n_target`) based on the current state of the game.

- **Heuristic Evaluation**  
  Evaluates board positions using a heuristic scoring function to estimate how good a position is for a given player.

---

## Requirements

- Python **3.x**

---

## Usage

Import and use the AI player in your Python code:

```python
from player_ai_new import play

# Example board and choices
board = [
    [0, 1],
    [1, 0],
    [0, 1],
    []
]
choices = [0, 1, 2, 3]
player = 0
memory = None

best_move, memory = play(board, choices, player, memory)
print(f"Best move: {best_move}, Memory: {memory}")
