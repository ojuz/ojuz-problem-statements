We call any sequence of points in the plane a plot. We intend to replace a given plot $(P_{1},\cdots,P_{n})$ with another that will have at most $m$ points ($m \le n$) in such a way that it "resembles" the original plot best.

The new plot is created as follows. The sequence of points $P_{1}, \cdots, P_{n}$ can be partitioned into $s$ ($s \le m$) contiguous subsequences:

$$(P_{k_{0}+1},\cdots,P_{k_{1}}), (P_{k_{1}+1},\cdots,P_{k_{2}}), \cdots, (P_{k_{s-1}+1},\cdots,P_{k_{s}})$$

where $0 = k_{0} < k_{1} < k_{2} < \cdots < k_{s} = n$, and afterwards each subsequence $(P_{k_{i-1}+1},\cdots,P_{k_{i}})$, for $i=1,\cdots,s$, is replaced by a new point $Q_{i}$. In that case we say that each of the points $P_{k_{i-1}+1},\cdots,P_{k_{i}}$ has been contracted to the point $Q_{i}$. As a result a new plot, represented by the points $Q_{1},\cdots,Q_{s}$, is created. The measure of such plot's resemblance to the original is the maximum distance of all the points  to the point it has been contracted to:

$$\max_{i=1,\cdots,s}\Big(\max_{j=k_{i-1}+1,\cdots,k_{i}}\big(d(P_j,Q_i)\big)\Big)$$

where $d(P_j, Q_i)$ denotes the distance between $P_j$ and $Q_i$, given by the well-known formula:

$$d\big(x_1,y_1),(x_2,y_2)\big)=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}$$

<center>
![]([[file:wykres.jpg]])

An exemplary plot $(P_{1},\cdots,P_{7})$ and the new plot $(Q_{1}, Q_{2})$, where  $(P_{1},\cdots,P_{4})$ are contracted to $Q_1$, whereas $(P_{5},P_{6},P_{7})$ to $Q_{2}$.
</center>

For a given plot consisting of $n$ points, you are to find the plot that resembles it most while having at most $m$ points, where the partitioning into contiguous subsequences is arbitrary. Due to limited precision of floating point operations, a result is deemed correct if its resemblance to the given plot is larger than the optimum resemblance by at most $0.000001$.

### Input

In the first line of the standard input there are two integers $n$ and $m$, $1 \le m \le n \le 100\,000$, separated by a single space. Each of the following $n$ lines holds two integers, separated by a single space. The $(i+1)$-th line gives $x_i$,$y_i$, $-1\,000\,000 \le x_i,y_i \le 1\,000\,000$, denoting the coordinates $(x_i,y_i)$ of the point $P_i$.

### Output

In the first line of the standard output one real number $d$ should be printed out, the resemblance measure of the plot found to the original one. In the second line of the standard output there should be another integer $s$, $1 \le s \le m$. Next, the following $s$ lines should specify the coordinates of the points $Q_1, \cdots , Q_s$, one point per line. Thus the $(i+2)$-th line should give two real numbers $u_i$ and $v_i$, separated by a single space, that denote the coordinates $(u_i,v_i)$ of the point $Q_i$. All the real numbers should be printed with at most 15 digits after the decimal point.

### Example

For the input data:

```
7 2
2 0
0 4
4 4
4 2
8 2
11 3
14 2
```

the correct result is:

```
3.00000000
2
2.00000000 1.76393202
11.00000000 1.99998199
```

*Task author: Jakub Pawlewicz.*