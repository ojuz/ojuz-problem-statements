Little Edna has received the *take-out* game as a present. Take-out is a single player game, in which the player is given a sequence of $n$ adjacent blocks, numbered from $1$ to $n$. Each block is either black or white, and there are $k$ times as many white blocks as there are black ones.

The player's goal is to remove all the blocks by certain permissible moves.

A single move consists in removing exactly $k$ white blocks and a single black block without changing the positions of other blocks. The move is permissible if there is no "gap" (a space left by a previously taken out block) between any two blocks being removed.

Help poor little Edna in finding any sequence of permissible moves that remove all the blocks.

### Input

In the first line of the standard input there are two integers, $n$ and $k$ ($2 \le n \le 1,000,000$, $1 \le k \le n-1$), separated by a single space, that denote the total number of blocks used in the game, and the number of white blocks per black node (to be removed in every move). In all the tests the condition $k+1|n$ holds.

In the second line there is a string of $n$ letters `b` or `c`. These tell the colours of successive blocks (in Polish): `b` (for *biały*) - white, `c` (for *czarny*) - black. You may assume that in all the tests there exists a sequence of permissible moves that takes out all the blocks.

In tests worth 40% of all points there holds an additional condition $n \le 10,000$.

### Output

Your program should print $\frac{n}{k+1}$ lines to the standard output. Successive lines should describe successive moves. Each line should contain $k+1$ integers, in increasing order, separated by single spaces, that denote the numbers of blocks to be removed in the move.

### Example

For the input data:

```
12 2
ccbcbbbbbbcb
```

the correct result is:

```
1 8 12
2 6 7
3 4 5
9 10 11
```

**Explanation of the example**: Let  denote the empty space after a block that was taken out (the gap). By executing the sequence of moves given above, we obtain the following configurations of blocks, in this order: Wykonując podane powyżej ruchy, uzyskujemy kolejno następujące układy klocków:

<center>
![](https://attach.oj.uz/problems/7hxxrk5t4c7rhkw9kvgap3sswjw3cq4d/usu1-crop.gif)
</center>

*Task authors: Jakub Pachocki, Wojciech Rytter.*