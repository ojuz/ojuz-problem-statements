Byteasar bought his son Bytie a set of blocks numbered from $1$ to $n$ and arranged them in a row in a certain order. Bytie's goal is to rearrange the blocks so that they are ordered naturally, from the smallest number to the largest. However, the only moves Bytie is allowed to make are:

* putting the last block at the very beginning (move `a`), and
* putting the third block at the very beginning (move `b`).

Help Bytie by writing a program that tells whether a given arrangement of blocks can be properly reordered, and tells the right sequence of moves if it is.

### Input

In the first line of the standard input there is a single integer $n$, $1 \le n \le 2\,000$. In the second line there are $n$ integers from the range $1$ to $n$, separated by single spaces. No number appears twice, and thus they represent the initial arrangement of the blocks.

### Output

If there is no sequence of moves leading to an arrangement with increasing blocks' numbers, your program should print out "`NIE DA SIE`" (*there is no way* in Polish), without the quotation marks.

Otherwise there should be a single integer $m$ ($m \le n^2$), denoting the number of operations, in the first line. An operation is a $k$-fold execution of either `a` or `b` move.

If $m > 0$, then there should be a sequence of $m$ integers with either `a` or `b` appended in the second line. Thus $k$`a` (for $0 < k < n$) denotes the $k$-fold execution of the move `a`. Analogously, $k$`b` (for $0 < k < n$) denotes the -fold execution of the move `b`.

Furthermore, the characters appended to the numbers in the second line have to alternate.

Should there be more than one solution, your program is free to pick one arbitrarily.

Example

For the input data:

```
4
1 3 2 4
```

the correct result is:

```
4
3a 2b 2a 2b
```

whereas for the input data:

```
7
1 3 2 4 5 6 7
```

the correct output is:

```
NIE DA SIE
```

and for the input data:

```
3
1 2 3
```

the correct output is:

```
0
```

*Task authors: Krzysztof Diks & Wojciech Rytter.*