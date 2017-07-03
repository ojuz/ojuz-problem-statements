Progressive climate change has forced the Byteburg authorities to build a huge lightning conductor that would protect all the buildings within the city. These buildings form a row along a single street, and are numbered from $1$ to $n$.

The heights of the buildings and the lightning conductor are non-negative integers. Byteburg's limited funds allow construction of only a single lightning conductor. Moreover, as you would expect, the higher it will be, the more expensive.

The lightning conductor of height $p$ located on the roof of the building $i$ (of height $h_i$) protects the building $j$ (of height $h_j$) if the following inequality holds:

$$h_j \le h_i + p - \sqrt{|i - j|},$$

where $|i-j$ denotes the absolute value of the difference between $i$ and $j$.

Byteasar, the mayor of Byteburg, asks your help. Write a program that, for every building $i$, determines the minimum height of a lightning conductor that would protect all the buildings if it were put on top of the building $i$.

### Input

In the first line of the standard input there is a single integer $n$ ($1 \le n \le 500\,000$) that denotes the number of buildings in Byteburg. Each of the following $n$ lines holds a single integer $h_i$ ($0 \le h_i \le 1\,000\,000$) that denotes the height of the $i$-th building.

### Output

Your program should print out exactly $n$ lines to the standard output. The $i$-th line should give a non-negative integer pi denoting the minimum height of the lightning conductor on the $i$-th building.

### Example

For the input data:

```
6
5
3
2
4
2
4
```

the correct result is:

```
2
3
5
3
5
4
```

*Task author: Piotr Niedzwiedz.*