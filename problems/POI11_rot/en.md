Byteasar the gardener is growing a rare tree called *Rotatus Informatikus*. It has some interesting features:

* The tree consists of straight branches, bifurcations and leaves. The trunk stemming from the ground is also a branch.
* Each branch ends with either a bifurcation or a leaf on its top end.
* Exactly two branches fork out from a bifurcation at the end of a branch - the left branch and the right branch.
* Each leaf of the tree is labelled with an integer from the range $1\ldots n$. The labels of leaves are unique.
* With some gardening work, a so called rotation can be performed on any bifurcation, swapping the left and right branches that fork out of it.

*The corona of the tree* is the sequence of integers obtained by reading the leaves' labels from left to right.

Byteasar is from the old town of Byteburg and, like all true Byteburgers, praises neatness and order. He wonders how neat can his tree become thanks to appropriate rotations. The neatness of a tree is measured by the number of *inversions* in its corona, i.e. the number of pairs $(i,j)$, $1 \le i < j \le n$ such that $a_i > a_j$ in the corona $a_1, a_2, \ldots, a_n$.

<center>
![]([[file:rys-crop.gif]])

The original tree (on the left) with corona 3,1,2 has two inversions. A single rotation gives a tree (on the right) with corona 1,3,2, which has only one inversion. Each of these two trees has 5 branches.
</center>

Write a program that determines the minimum number of inversions in the corona of Byteasar's tree that can be obtained by rotations.

### Input

In the first line of the standard input there is a single integer $n$ ($2 \le n \le 200\,000$) that denotes the number of leaves in Byteasar's tree. Next, the description of the tree follows. The tree is defined recursively:

* if there is a leaf labelled with $p$ ($1 \le p \le n$) at the end of the trunk (i.e., the branch from which the tree stems), then the tree's description consists of a single line containing a single integer $p$,
* if there is a bifurcation at the end of the trunk, then the tree's description consists of three parts:
  - the first line holds a single number $0$,
  - then the description of the left subtree follows (as if the left branch forking out of the bifurcation was its trunk),
  - and finally the description of the right subtree follows (as if the right branch forking out of the bifurcation was its trunk).

In tests worth at least 30% of the points it additionally holds that $n \le 5\,000$.

### Output

In the first and only line of the standard output a single integer is to be printed: the minimum number of inversions in the corona of the input tree that can be obtained by a sequence of rotations.

### Example

For the input data:
```
3
0
0
3
1
2
```
the correct result is:
```
1
```

**Explanation of the example:** Figure 1 illustrates the tree given in the example.

*Task authors: Tomasz Walen.*