# Minesweeper AI Game

A Python-based implementation of the classic Minesweeper game featuring a logic-driven AI agent. Built with `pygame`, this project allows players to either interact with the game manually or watch an AI deduce mine locations using propositional logic.

---

## Features

- **Playable Interface**: Click cells to reveal them or right-click to place flags.
- **AI Agent**: Automatically makes safe or logical moves based on known information.
- **Game Logic**: Tracks mines, flags, safe moves, and supports full win/loss gameplay.
- **Inference Engine**: Uses logical sentences to deduce safe cells or mines via subset reasoning.

---

## AI Capabilities

The AI uses a knowledge base of logical sentences to:
- Infer cells that are guaranteed to be safe or mines.
- Add new logical sentences based on observations.
- Infer new knowledge using subset relations between sentences.

Example sentence:
> `{A, B, C} = 1` → One of A, B, or C is a mine.

If `{A, B, C} ⊆ {A, B, C, D}` and `{A, B, C} = 1`, `{D} = 1` can be inferred.

---

## Technologies

- Python 3
- pygame (GUI rendering)
- Object-Oriented Design

---

## Project Structure

```
├── minesweeper.py       # Game logic, board, and AI classes
├── runner.py            # GUI interface with pygame
├── requirements.txt     # Dependencies (pygame)
└── assets/              # Images and fonts
```

---

## Getting Started

### 1. Clone the repository

    git clone https://github.com/YOUR_USERNAME/minesweeper-ai.git
    cd minesweeper-ai
    
### 2. Install Dependencies

    pip install -r requirements.txt
    
### 3. Run the Game

    python runner.py

---

## How to Play

- **Left Click**: Reveal a cell.
- **Right Click**: Flag or unflag a suspected mine.
- **"AI Move" Button**: Lets the AI make a move using its knowledge base.
- **"Reset" Button**: Restarts the game.

The game begins with instructions and can be played manually or by allowing the AI to reason and play.

---

## AI Highlights

- Uses a rule-based inference system to identify safe moves and mines.
- Capable of deducing new information from overlapping logical sentences.
- Automatically marks mines and avoids revisiting known cells.

---

## License

This project is for educational and demonstration purposes. You are free to fork and modify it for personal use.

---

## Author

Developed by Silvia Tran.
https://github.com/silviatran

---
