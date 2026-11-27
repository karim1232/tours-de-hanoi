# Tower of Hanoi

The Tower of Hanoi game in Python, with a Turtle graphics display and an animated automatic solver.

The goal is to move every disk from the left tower to the right one, one disk at a time, never placing a disk on a smaller one.

## Features

- Board and disks drawn with Turtle, one color per disk
- Moves typed in the terminal (source tower, then target tower); an illegal move is rejected with a message
- Undo the last move
- Give up at any time
- Timer and move counter. You win if you finish in at most `2ⁿ + n` moves (the minimum possible is `2ⁿ − 1`)
- Animated solution: the recursive algorithm solves the game in front of you
- End-of-game tables for each number of disks: best scores (in moves), best times, and ranking by average thinking time per move

## Running

Python 3 is enough; Turtle ships with it.

```bash
python tours_de_hanoi.py
```

Click in the window to start, then answer the questions in the terminal. The prompts are in French.

## The recursive algorithm

To move `n` disks from A to C:
1. move `n − 1` disks from A to B (recursively)
2. move the largest disk from A to C
3. move the `n − 1` disks from B to C (recursively)

This gives the optimal solution, in `2ⁿ − 1` moves.

## Code organization

| Part | Content |
|---|---|
| Board | board stored as lists, move and win checks |
| Graphics | drawing the board and disks, erasing |
| Game | move input, game loop, timer |
| Undo | position history, going back one move |
| Scores | saving and displaying the score, time and ranking tables |
| Solution | recursive solver and animation |

## Author

Karim Glelah
