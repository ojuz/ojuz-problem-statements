Byteasar intends to throw up a party. Naturally, he would like it to be a success. Furthermore, Byteasar is quite certain that to make it so it suffices if all invited guests know each other. He is currently trying to come up with a list of his friends he would like to invite.

Byteasar has $n$ friends, where $n$ is divisible by 3. Fortunately, most of Byteasar's friends know one another. Furthermore, Byteasar recalls that he once attended a party where there were $\frac{2}{3}n$ of his friends, and where everyone knew everyone else. Unfortunately, Byteasar does not quite remember anything else from that party... In particular, he has no idea which of his friends attended it.

Byteasar does not feel obliged to throw a huge party, but he would like to invite at least $\frac{n}{3}$ of his friends. He has no idea how to choose them, so he asks you for help.

### Input

In the first line of the standard input two integers, $n$ and $m$ ($3 \le n \le 3\,000$, $\frac{\frac{2}{3}n(\frac{2}{3}n−1)}{2} \le m \le \frac{n(n−1)}{2}$), are given, separated by a single space. These denote the number of Byteasar's friends and the number of pairs of his friends who know each other, respectively. Byteasar's friends are numbered from $1$ to $n$. Each of the following $m$ lines holds two integers separated by a single space. The numbers in line no. $i+1$ (for $i=1,2,\ldots,m$) are $a_i$ and $b_i$ ($1 \le a_i < b_i \le n$), separated by a single space, which denote that the persons $a_i$ and $b_i$ know each other. Every pair of numbers appears at most once on the input.

### Output

In the first and only line of the standard output your program should print $\frac{n}{3}$ numbers, separated by single spaces, in increasing order. These number should specify the numbers of Byteasar's friends whom he should invite to the party. As there are multiple solutions, pick one arbitrarily.

### Example

For the input data:
```
6 10
2 5
1 4
1 5
2 4
1 3
4 5
4 6
3 5
3 4
3 6
```

![]([[file:impzad1.gif]])

the correct result is:
```
2 4
```

**Explanation of the example:** Byteasar's friends numbered 1, 3, 4, 5 know one another. However, any pair of Byteasar's friends who know each other, like 2 and 4 for instance, constitutes a correct solution, i.e., such a pair needs not be part of aforementioned quadruple.

*Task author: Jakub Onufry Wojtaszczyk.*