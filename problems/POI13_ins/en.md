Inspector Byteasar is investigating a crime that took place on the premises of a software development company. He is trying to establish the chain of events. Unfortunately, the programmers are rather scatterbrained. Statements of the kind "Well, when I checked at 14:42, there were five other programmers logged in on the server." are the most informative of those that Byteasar could get.

It is known that every programmer came to office at some point during that day, spent some time in there without going out, and then left for good, never coming back on the same day.

Byteasar, confused by the programmers' statements, is not sure if he should rely on them. In fact, he is wondering whether it is at all possible that they all tell the truth. He asks you for help in finding that out.

### Input

In the first line of the standard input, there is an integer $z$ ($1 \le z \le 50$), the number of data sets. The lines that follow contain the $z$ data sets.

The first line of each data set holds two integers, $n$ and $m$, separated by a single space ($1 \le n,m \le 100,000$). These are the number of programmers working in the office and the number of statements recorded by Byteasar. The programmers are numbered from $1$ to $n$.

Each of the $m$ lines that follow describes a single statement. Each such line contains three integers $t$, $j$, and $i$, separated by single spaces ($1 \le t \le m$, $1 \le j \le n$, $0 \le i \le n$). These indicate that the programmer no. $j$ confessed that at time $t$ he was in the office and there were i more programmers apart from him. We assume that the programmers came in to the office and left it at times different from those appearing in the statements, i.e., either before, after or in between them.

In tests worth 7% of the total number of points, the additional condition $n, m \le 5$ holds. Moreover, in tests worth 28% of the total number of points it holds that $n, m \le 101$.

### Output

For each data set, your program should print a single positive integer to the standard output. Printing out the number $k$ ($1 \le k \le m$) indicates that the first $k$ statements given on the input can be true but the first $k+1$ statements cannot. In particular, if $k=m$, then all the statements given as input can be true.

### Example

For the input data:

```
2
3 5
1 1 1
1 2 1
2 3 1
4 1 1
4 2 1
3 3
3 3 0
2 2 0
1 1 0
```

the correct result is:

```
4
3
```

**Explanation of the example**: In the first data set, the statements given by programmers cannot all be true. The programmers 1 and 2 stated that they were in the office between times 1 and 4 but the programmer 3 stated that at time 2 there was only a single person apart from him there. If we discount that last statement, the remaining ones can be true.

In the second data set, all the statements on record can be true.

*Task author: Jakub Wojtaszczyk.*