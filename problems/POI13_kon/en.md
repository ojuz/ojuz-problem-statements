You have the honor of serving as queen Bytelea's royal gardener. 
Splendid, you might think, but in such case you should think twice! It is a menial job, as you are beginning to realize. Next to the queen's castle, there is a huge garden with $n$ trees arranged in a line. One of your tasks is keeping the queen constantly informed on which of the trees are mature, i.e., are at least $k$ bytemeters tall.

This is not all: sometimes the queen asks you to water some of the trees with a magic watering can. When you do, each tree that has been watered grows by exactly one bytemeter.

Now prove your salt by quickly seeing to each queen's request!

### Communication

Write a library that will communicate with a grading program. It should contain at least the following three functions, to be called by the grading program:

* `inicjuj(n, k, D)` - this function is going to be called exactly once, in the very beginning of a test. You may used it to initialize your data structures. It takes the following parameters: the number of trees $n$, the minimum height of a mature tree $k$, and an array $D$ of size $n$ containing the initial heights of all the trees. The trees are numbered with successive integers from 0 to $n-1$.
  - **C/C++**: `void inicjuj(int n, int k, int *D);`
* `podlej(a, b)` - a call of this function means that the queen has requested that you water all the trees from the $a$-th one to the $b$-th one ($0 \le a \le b \le n-1$), including the two. Recall that all those trees grow by 1 bytemeter.
  - **C/C++**: `void podlej(int a, int b);`
* `dojrzale(a, b)` - the queen asks how many among the trees from $a$ to $b$ ($0 \le a \le b \le n-1$), including the two, are mature.
  - **C/C++**: `int dojrzale(int a, int b);`

Your library **must not** read any data (neither from the standard input, nor from any files). It must not write anything to any files or the standard output either. It may print to the standard error stream (`stderr`) - keep in mind though that this takes time.

If you are coding in C/C++, then your library **must not** contain the main function. 

Your solution is going to be awarded the points for a test if and only if it conforms to aforementioned technical specification and it answers all the queen's queries correctly.

### Constraints

The following hold in all the tests:

* $1 \le n \le 300\,000$
* $1 \le k \le 10^9$
* the total number of calls of the procedure/function `podlej` and the function `dojrzale` does not exceed $300\,000$
* the initial heights of all the trees are positive integers no larger than $10^9$.
 
In tests worth 20% of all points, the following additional conditions hold:

* $n \le 2\,000$
* the total number of calls of the procedure/function `podlej` and the function `dojrzale` does not exceed $10\,000$

In tests worth 50% of all points, every call of the procedure/function `podlej` is made before any call of the function `dojrzale`.

### Compiling

Your library - `kon.c`, `kon.cpp` - will be compiled together with the grading program with the following command(s):

* **C**: `gcc -O2 -static -lm kon.c kongrader.c -o kon`
* **C++**: `g++ -O2 -static -lm kon.cpp kongrader.cpp -o kon`
* UPD: For correct compile options used in real grading, check the "Compilation commands" in the top of this page.

### Sample execution

The following table presents a sample sequence of calls of the functions and the correct values returned by the function `dojrzale`.

<div class="table-responsive">
        <table class="table-bordered table-condensed">
        <thead>
        <tr><td><b>Call</b> </td><td> <b>Returns</b> </td><td><b>Explanation</b></td></tr>
        </thead>
        <tbody>
        <tr><td><tt>inicjuj(4, 6, D)</tt> </td><td>&nbsp; </td><td> There are $n = 4$ trees of heights 5, 4, 3, and 7, and $k = 6$.
        (<tt>D[0] = 5</tt>, <tt>D[1] = 4</tt>, <tt>D[2] = 3</tt>, <tt>D[3] = 7</tt>)</td></tr>
        <tr><td><tt>dojrzale(2, 3)</tt> </td><td> 1 </td><td> How many mature trees are there in the interval $[2, 3]$?</td></tr>
        <tr><td><tt>podlej(0, 2)</tt> </td><td>&nbsp; </td><td> Water the trees 0, 1 and 2.
        <tr><td><tt>dojrzale(1, 2)</tt> </td><td> 0 </td><td> How many mature trees are there in the interval $[1, 2]$?</td></tr>
        <tr><td><tt>podlej(2, 3)</tt> </td><td>&nbsp; </td><td> Water the trees 2 and 3.</td></tr>
        <tr><td><tt>podlej(0, 1)</tt> </td><td>&nbsp; </td><td> Water the trees 0 and 1.</td></tr>
        <tr><td><tt>dojrzale(0, 3)</tt> </td><td> 3 </td><td> How many mature trees are there in the interval $[0, 3]$?</td></tr></tbody>
    </table>
</div>

### Testing

In [this archive](https://attach.oj.uz/problems/5tl21xwzk2eyhu14qz8g1a3l1xubhmnr/konzaw.zip) you will find a sample grading program (`kongrader.c`, `kongrader.cpp`). To execute this program with your library, you should name the latter `kon.c`, `kon.cpp`, and place it in an appropriate directory (`c`, `cpp`). In the beginning of the competition, you will find (incorrect) sample solutions therein. The grading program can be compiled together with your library with the command

```
make kon
```

which executes the commands described in the section *Compiling*. Compiling a C/C++ solution requires a file `koninc.h`, which is already placed in an appropriate directory.

Compiled this way, the grading program reads from the standard input a description of a test, calls appropriate functions of your library, and prints the answers to the standard output.

A test description is formatted as follows. The first line of the test contains two integers, $n$ and $k$. The second line contains  integers that are the initial heights of the trees. The third line contains the number $q$. Then $q$ lines follow, each containing a single character, $p$ or $d$, and two non-negative integers. The character indicates which function should be called: `p` for `podlej` and `d` for `dojrzale`, whereas the numbers are the arguments for the function calls. The function `inicjuj` is going to be called immediately after reading the first two lines. Remember though that the sample grading program does not check if the data are in the right format, nor if they satisfy the constraints given in section *Constraints*.

In the archive, there is a file `kon0.in`, corresponding to aforementioned sample execution. To run the grading program on it, use the following command:

```
./kon < kon0.in
```

The values returned by the calls of the function `dojrzale` will be printed on the standard output. The correct result of this execution can be found in the file `kon0.out`.

To find out if your solution is correct, you can send it (i.e., your library) to the grading system.

*Task author: Bartłomiej Dudek.*