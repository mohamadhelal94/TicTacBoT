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

---
board: Current board state.
choices: List of valid moves (e.g., column indices).
player: The current player (e.g., 0 or 1).
memory: Optional state passed between turns (can be None initially).

---
Main Functions
play(board, choices, player, memory)
Determines the best move for the AI player and returns (best_move, updated_memory).
is_winning(board, player)
Checks whether the given player currently has a winning position on the board.
check_winning_move(board, col, player)
Tests if placing a mark in the specified column col results in a win for player.
minimax(board, depth, alpha, beta, maximizing_player)
Core Minimax algorithm with alpha–beta pruning. Explores possible moves up to a given depth and returns the best evaluated score.
heuristic_score(board, player)
Evaluates the board using a heuristic that estimates how favorable the position is for player.
adjust_n_target(board, n_target)
Adjusts the target number of consecutive marks needed to win based on the current game situation.

---


