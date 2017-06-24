Byteasar lives in Byteburg, a city famous for its milk bars on every corner. One day Byteasar came up with an idea of a "milk multidrink": he wants to visit each milk bar for a drink exactly once. Ideally, Byteasar would like to come up with a route such that the next bar is always no further than two blocks (precisely: intersections) away from the previous one.

The intersections in Byteburg are numbered from $1$ to $n$, and all the streets are bidirectional. Between each pair of intersections there is a unique direct route, ie, one that does not visit any intersection twice. Byteasar begins at the intersection no. $1$ and finishes at the intersection no. $n$.

Your task is to find any route that satisfies Byteasar's requirements if such a route exists.

<center>
![](https://attach.oj.uz/problems/cp9k98rojklcbtzo2ej9ex5njtsu7bs7/rys1-crop.gif)
<p>An exemplary route satisfying the requirements is: $1, 11, 8, 7, 5, 9, 2, 10, 4, 6, 3, 12$.</p>
</center>

<center>
![](https://attach.oj.uz/problems/cp9k98rojklcbtzo2ej9ex5njtsu7bs7/rys2-crop.gif)
<p>There is no route that satisfies the requirements.</p>
</center>

### Input

In the first line of the standard input there is a single integer $n$ ($2 \le n \le 500,000$), denoting the number of intersections in Byteburg. Each of the following $n-1$ lines holds a pair of distinct integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le n$), separated by a single space, that represent the street linking the intersections no. $a_i$ and $b_i$.

In tests worth 65% of all points the condition $n \le 5,000$ holds.

### Output

If there is no route satisfying Byteasar's requirements, your program should print a single word "`BRAK`" (Polish for *none*), without the quotation marks to the standard output. Otherwise, your program should print $n$ lines to the standard output, the $i$-th of which should contain the number of the $i$-th intersection on an arbitrary route satisfying Byteasar's requirements. Obviously, in that case the first line should hold the number $1$, and the $n$-th line - number $n$.

### Example

For the input data:

```
12
1 7
7 8
7 11
7 2
2 4
4 10
2 5
5 9
2 6
3 6
3 12
```

the correct result is:

```
1
11
8
7
4
10
2
9
5
6
3
12
```

For the input data:

```
15
1 14
14 7
7 8
7 11
7 2
2 4
4 10
2 5
5 9
2 6
3 6
3 15
11 12
8 13
```

the correct result is:

```
BRAK
```