CF - Grid Game (Constructive)

Key Idea:

Don't simulate the board.
Find a fixed repeating pattern.

Invariant:

Never reuse a position before its row/column is deleted.

Pattern:

Vertical (0) → Use one column, cycle through 4 rows → column clears.
Horizontal (1) → Use one row, alternate between 2 positions → row clears.

Recognition:

If rows/columns automatically disappear, think "Can I force periodic clearing with a fixed pattern?"
