Byteasar wants to take a taxi from the town Bytehole to the town Bytepit, which is $m$ kilometres away from Bytehole. Exactly $d$ kilometres along the way from Bytehole to Bytepit, there is a base of $n$ taxis, numbered from $1$ to $n$. The taxi no. $i$ has enough fuel to drive exactly $x_i$ kilometres.

Byteasar can change taxis at any point. All the taxis start at their base but need not return there. Your task is to determine whether Byteasar can be driven from Bytehole to Bytepit, and if so, what it the minimum number of taxis required for such a journey.

### Input

The first line of the standard input holds three integers, $m$, $d$, and $n$ ($1 \le d \le m \le 10^{18}$, $1 \le n \le 500,000$), separated by single spaces. Those denote, respectively: the distance from Bytehole to Bytepit, the distance from Bytehole to the taxi base, and the number of taxis at the base. The second line of input contains $n$ integers, $x_{1}, x_{2}, \cdots, x_{n}$ ($1 \le x_{i} \le 10^{18}$), separated by single spaces. The number $x_{i}$ denotes the maximum distance (in kilometres) that the $i$-th taxi can travel.

In tests worth 40% of all points an additional condition $n \le 5,000$ holds.

### Output

Your program should print a single integer to the standard output: the minimum number of taxis Byteasar has to take to get from Bytehole to Bytepit. If getting there is impossible, your program should print the number $0$.

### Example

For the input data:

```
42 23 6
20 25 14 27 30 7
```

the correct result is:

```
4
```