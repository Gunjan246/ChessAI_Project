# Chess AI – Minimax Algorithm with Alpha-Beta Pruning

An AI-powered chess engine that uses the **Minimax Search Algorithm** and **Alpha-Beta Pruning** to evaluate possible moves, anticipate opponent strategies, and select the most promising move.

## Project Overview

This project implements an AI-powered chess engine using Minimax Search and Alpha-Beta Pruning to make strategic decisions in a two-player chess game.

This project implements a chess-playing AI that uses adversarial search to analyze future board positions and make intelligent decisions. It provides an interactive way to explore how AI makes decisions in chess.
The engine explores possible future game states, evaluates board positions using a heuristic evaluation function, and selects promising moves while accounting for the opponent's optimal responses.

Alpha-Beta Pruning optimizes the search process by eliminating branches that cannot influence the final decision, improving computational efficiency without compromising the result.

## Objectives

- Develop an AI capable of selecting promising chess moves.
- Implement adversarial search using the Minimax algorithm.
- Evaluate board positions using a scoring function.
- Optimize search performance using Alpha-Beta Pruning.
- Explore future game states while considering the opponent's best possible responses.

## Algorithms Used

### 1. Minimax Algorithm

Minimax is a decision-making algorithm used in two-player, zero-sum games.

It assumes that both players play optimally:
- **MAX (AI):** Selects the move with the highest evaluation score.
- **MIN (Opponent):** Selects the move with the lowest evaluation score for the AI.

The algorithm explores possible future board positions through a game tree, evaluates the leaf nodes, and propagates their scores backwards to determine the best move.

**Working:**
1. Generate all possible legal moves.
2. Explore future board positions up to a specified search depth.
3. Evaluate the resulting positions.
4. MAX selects the highest score.
5. MIN selects the lowest score.
6. Return the best move and its evaluation score.

### 2. Alpha-Beta Pruning

Alpha-Beta Pruning is an optimization of Minimax that reduces unnecessary computation without changing the final decision.

It maintains two values:

- **Alpha (α):** Best score MAX can guarantee so far.
- **Beta (β):** Best score MIN can guarantee so far.

**Pruning condition:**

`α ≥ β`

When this condition is satisfied, the remaining branches are skipped because they cannot affect the final decision.

**Advantages:**
- Reduces the number of nodes evaluated.
- Improves search efficiency.
- Allows deeper search within the same computational budget.
- Produces the same result as Minimax for the same search depth and move ordering.

## Board Evaluation Function

The evaluation function assigns a numerical score to a chess position.

It considers factors such as:

- **Material Advantage:** Relative value of pieces remaining on the board.
- **Piece Positioning:** Strategic placement of chess pieces.
- **King Safety:** Protection of the king.
- **Board Control:** Control over important squares and areas of the board.

The evaluation score helps the AI compare different possible board states.

## Implemented Features

- Board-state evaluation based on chess piece weights.
- Minimax search for determining the best move.
- Optional search-depth configuration.
- Alpha-Beta Pruning for search optimization.
- Game class supporting different player configurations.
- Game result statistics.

## Algorithm Complexity

Let:
- `b` = Average branching factor (approximately 35 moves).
- `d` = Search depth in plies.

| Algorithm | Time Complexity |
|---|---|
| Minimax | O(b^d) |
| Alpha-Beta (Worst Case) | O(b^d) |
| Alpha-Beta (Best Case) | O(b^(d/2)) |

**Space Complexity:** O(b × d)

Alpha-Beta Pruning can significantly reduce the number of evaluated nodes when moves are ordered effectively.

## Limitations

- Searching beyond depth 4 can become computationally expensive.
- The engine has limited endgame understanding.
- Some games may end in draws due to limitations in position evaluation.
- Deeper searches require additional optimization.

## Future Improvements

- Implement transposition tables and position caching.
- Improve the board evaluation heuristic.
- Introduce better move ordering strategies.
- Integrate endgame tablebases.
- Improve endgame decision-making.
- Explore deeper search with improved performance.

## Technology Stack

- **Programming Language:** Python
- **Algorithms:** Minimax, Alpha-Beta Pruning
- **Development Environment:** Visual Studio Code
- **Supporting Resources:** Python Chess documentation

## Project Structure

```text
ChessAI_Project/
│
├── chess_game/           # Chess game implementation
├── img/                  # Project images and visual assets
├── games_analysis.ipynb  # Game analysis notebook
├── requirements.txt      # Project dependencies
├── README.md             # Project documentation
└── LICENSE               # MIT License
```

## References

1. [Creating an AI that Plays Chess – Minimax and Alpha-Beta Pruning](https://youtu.be/-ivz8yJ4l4E)
2. [AI Chess Game Using Minimax and Alpha-Beta Pruning](https://youtu.be/W8JdJsGS2C4)
3. [The Fascinating Programming of a Chess Engine](https://youtu.be/w4FFX_otR-4)
4. [ChessAI – GitHub Learning Reference](https://github.com/aiatuci/ChessAI)
5. [Python-Chess Documentation](https://python-chess.readthedocs.io/)

## Project Team

| Team Member | Roll Number |
|---|---|
| Khanak Gupta | 2024UIT3011 |
| Vibhuti Gupta | 2024UIT3012 |
| Gayathri Ajith | 2024UIT3029 |
| Gunjan | 2024UIT3039 |
| Krati Gupta | 2024UIT3041 |

---

*An exploration of Artificial Intelligence through adversarial search, strategic decision-making, and game-tree optimization.*
