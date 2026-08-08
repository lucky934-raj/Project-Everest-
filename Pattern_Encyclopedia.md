1) CF - Grid Game (Constructive)
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


#################


2) CF — Walking Between Houses

Topic: Constructive + Greedy

Observation

Each of the k moves has distance:

1 ≤ d_i ≤ n-1

Therefore:

k ≤ s ≤ k(n-1) → otherwise NO.

Construction 1 — Greedy jumps
Start at 1.
For each move take the maximum possible jump:
jump = min(n-1, s-(k-1))
Go right if possible, otherwise left.
Reserve 1 distance for every remaining move.

Construction 2 — Build distances ⭐

Instead of directly choosing positions:

Give every move minimum distance 1.
total = k
Remaining distance:
x = s-k
Distribute x among the k moves.
each move can receive at most n-2 extra
so d_i ≤ n-1
Now alternate directions:
move 1 → right
move 2 → left
move 3 → right
...

Why alternate?
A jump is at most n-1, so from either side we can always make it while staying inside [1,n].

Pattern ⭐
Exact sum + bounded values → start with minimum values, distribute the remaining amount, then construct positions from those values.
This second method is actually a very useful constructive pattern to remember:
"First construct the distances, then worry about the positions."

