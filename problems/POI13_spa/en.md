The names of towns in Byteotia are unique sequences of exactly $n$ bits. There are $2^{n}-k$ towns in Byteotia, and thus, only $k$ sequences of $n$ bits do not correspond to any town.

Some pairs of towns are connected with roads. Specifically, two towns are directly linked by a road if and only if their names differ in a single bit. The roads do not cross outside of towns.

Byteasar intends to take a stroll - he intends to walk from the town $x$ to the town $y$, taking the existing roads. Your task is to write a program that will determine if such a walk is possible.

### Input

In the first line of the standard input, there are two integers, $n$ and $k$ ($1 \le n \le 60$, $0 \le k \le 1,000,000$, $k \le 2^n-1$, $n \cdot k \le 5,000,000$), separated by a single space. These are the length of town names in bits and the the number of $$-bit sequences that do not correspond to any town, respectively. In the second line, there are two strings, separated by a single space, each consisting of $n$ characters `0` and/or `1`. These are the names of the towns $x$ and $y$. In the $k$ lines that follow, all the sequences of $n$ bits that do not correspond to any town are given, one sequence per line. Each such sequence is a string of $n$ characters `0` and/or `1`. You may assume that $x$ and $y$ are not among those $k$ sequences.

In tests worth 25% of total points the additional condition $n \le 22$ holds.

### Output

Your program should print to the standard output the word `TAK` (Polish for *yes*) if walking from the town $x$ to the town $y$ is possible, and the word `NIE` (Polish for *no*) otherwise.

### Example

For the input data:

```
4 6
0000 1011
0110
0111
0011
1101
1010
1001
```

the correct result is:

```
TAK
```

For the input data:

```
2 2
00 11
01
10
```

the correct result is:

```
NIE
```

**Explanation of the first example**: The following are two examples of a walk from 0000 to 1011:

* $0000 \rightarrow 1000 \rightarrow 1100 \rightarrow 1110 \rightarrow 1111 \rightarrow 1011$
* $0000 \rightarrow 0100 \rightarrow 1100 \rightarrow 1110 \rightarrow 1111 \rightarrow 1011$.

*Task author: Wojciech Rytter*