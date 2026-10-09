# 🎰 Slot Machine

A command-line slot machine simulator written in Python and built in a Jupyter Notebook. Deposit some money, choose how many lines to bet on, spin the reels, and see how much you win.

## Features

- Deposit validation (whole numbers greater than zero)
- Choose how many lines to bet on (1 to 3)
- Set the bet per line (between $1 and $100)
- Check that the total bet does not exceed your balance
- Random 3x3 reel generation with weighted symbols (rarer symbols appear less often)
- Winning line detection and payout calculation
- Clean grid output in the console

## How it works

1. You deposit an initial balance.
2. You choose the number of lines to bet on. Line 1 is the top row, line 2 is the middle row and line 3 is the bottom row.
3. You choose how much to bet on each line. The total bet is `bet x lines`.
4. The machine spins a 3x3 grid. Each symbol has a limited number of appearances per reel:

   | Symbol | Count | Multiplier |
   |--------|-------|------------|
   | X      | 2     | 5x         |
   | Y      | 4     | 4x         |
   | Z      | 6     | 3x         |
   | W      | 8     | 2x         |

5. A line wins when all the symbols in that row match. The payout is `symbol multiplier x bet per line`.

### Example

```
W | W | Y
W | W | W
W | Z | Z
```

With a bet of $20 on 3 lines, the second line wins and pays `2 x 20 = $40`.

## Getting started

### Requirements

- Python 3.9 or higher
- [Jupyter Notebook](https://jupyter.org/install) or JupyterLab

### Installation

```bash
git clone https://github.com/YOUR_USERNAME/slot-machine.git
cd slot-machine
pip install notebook
jupyter notebook
```

### Running the game

1. Open `maquina_tragaperras.ipynb`.
2. Select **Kernel → Restart & Run All**.
3. Follow the instructions in the console.

## Project structure

```
slot-machine/
├── maquina_tragaperras.ipynb   # Game code
├── README.md
└── .gitignore
```

## Main functions

| Function | Description |
|----------|-------------|
| `deposit()` | Asks the player for the initial deposit |
| `get_number_of_lines(X`x^XX^^X
