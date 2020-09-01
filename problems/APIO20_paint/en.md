<h3>Description</h3>
<p>
  It has been a while since the last time Pak Dengklek painted the wall on his house, so he wants to
  repaint it. The wall consists of $N$ segments, numbered from $0$ to $N - 1$. For this
  problem, we assume that there are $K$ different colours, represented by an integer from
  $0$ to $K - 1$ (e.g., red is represented by $0$, blue is represented by $1$, and
  so on). Pak Dengklek wants to paint the $i$-th segment of his wall using the colour $C[i]$.
</p><p>
  To paint the wall, Pak Dengklek hires a contractor company with $M$ contractors, numbered
  from $0$ to $M - 1$. Unfortunately for Pak Dengklek, contractors are only willing to paint
  the colours that they like. Specifically, the $j$-th contractor only likes $A[j]$ colours
  and only wants to paint a segment to be coloured with either of the following colour: colour
  $B[j][0]$, colour $B[j][1]$, $\ldots$, or colour $B[j][A[j] - 1]$.
</p><p>
  Pak Dengklek can give several instructions to the contractor company. In a single instruction, Pak
  Dengklek will give two parameters $x$ and $y$, where $0 \le x \lt M$ and $0 \le y
  \le N - M$. The contractor company will instruct the ($(x + l) \bmod M$)-th contractor to
  paint the ($y + l$)-th segment, for $0 \le l \lt M$. If there exists a value of $l$
  such that the ($(x + l) \bmod M$)-th does not like colour $C[y + l]$, then the instruction
  is invalid.
</p><p>
  Pak Dengklek has to pay for each instruction he gives, thus he would like to know the minimum
  number of instructions he has to give to paint all segments with their intended colour or identify
  if it is impossible to do so. The same segment can be painted multiple times, but it must always
  be painted with its intended colour.
</p>

<h3>Task</h3>
<p>
  You have to implement <code>minimumInstructions</code> function:
</p>
<ul>
  <li>
    <code>minimumInstructions(N, M, K, C, A, B)</code> - This function will be called by the
    grader exactly once.
    <ul>
      <li>$N$: An integer representing the number of segments.</li>
      <li>$M$: An integer representing the number of contractors.</li>
      <li>$K$: An integer representing the number of colours.</li>
      <li>$C$: An array of $N$ integers representing the intended colour of the segments.
          </li>
      <li>$A$: An array of $M$ integers representing the number of colours that the
          contractors like.</li>
      <li>$B$: An array of $M$ array of integers representing the colours that the
          contractors like. </li>
      <li>This function must return an integer representing the minimum number of instructions Pak
          Dengklek has to give to paint all segments with their intended colour, or $-1$ if it
          is impossible to do so.</li>
    </ul>
  </li>
</ul>

<h3>Example</h3>
<p>
  In the first example, $N = 8$, $M = 3$, $K = 5$, $C = [3, 3, 1, 3, 4, 4, 2, 2]$,
  $A = [3, 2, 2]$, $B = [[0, 1, 2], [2, 3], [3, 4]]$. Pak Dengklek can give the following
  instructions:
</p>
<ol>
  <li>$x = 1$, $y = 0$. This is a valid instruction since the first contractor can paint
      the zeroth segment, the second contractor can paint the first segment, and the zeroth
      contractor can paint the second segment.</li>
  <li>$x = 0$, $y = 2$. This is a valid instruction since the zeroth contractor can paint
      the second segment, the first contractor can paint the third segment, and the second
      contractor can paint the fourth segment.</li>
  <li>$x = 2$, $y = 5$. This is a valid instruction since the second contractor can paint
      the fifth segment, the zeroth contractor can paint the sixth segment, and the first
      contractor can paint the seventh segment.</li>
</ol>
<p>
  It is easy to see that Pak Dengklek cannot give less than $3$ instructions to paint all
  segments with their intended colour, thus
  <code>minimumInstructions(8, 3, 5, [3, 3, 1, 3, 4, 4, 2, 2], [3, 2, 2], [[0, 1, 2], [2, 3], [3, 4]])</code>
  should return $3$.
</p>
<p>
  In the second example, $N = 5$, $M = 4$, $K = 4$, $C = [1, 0, 1, 2, 2]$,
  $A = [2, 1, 1, 1]$, $B = [[0, 1], [1], [2], [3]]$. Since the third contractor only like
  colour $3$ and none of the segment is to be painted with colour $3$, it is impossible
  for Pak Dengklek to give any valid instruction. Therefore,
  <code>minimumInstructions(5, 4, 4, [1, 0, 1, 2, 2], [2, 1, 1, 1], [[0, 1], [1], [2], [3]])</code>
  should return $-1$.
</p>

<h3>Constraints</h3>
For $0 \le k \lt K$, let $f(k)$ be the number of $j$ such that the $j$-th contractor
likes colour $k$. For example, if $f(1) = 2$, then there are two contractors who like the
colour $1$.
<ul>
  <li>$1 \le N \le 100\,000$.</li>
  <li>$1 \le M \le \min(N, 50\,000)$.</li>
  <li>$1 \le K \le 100\,000$.</li>
  <li>$0 \le C[i] \lt K$.</li>
  <li>$1 \le A[j] \le K$.</li>
  <li>$0 \le B[j][0] \lt B[j][1] \lt \ldots \lt B[j][A[j] - 1] \lt K$.</li>
  <li>Sum of $f(k)^2 \le 400\,000$.</li>
</ul>

<h4>Subtask 1 (12 points)</h4>
<ul>
  <li>$f(k) \le 1$.</li>
</ul>

<h4>Subtask 2 (15 points)</h4>
<ul>
  <li>$N \le 500$.</li>
  <li>$M \le \min(N, 200)$.</li>
  <li>Sum of $f(k)^2 \le 1\,000$.</li>
</ul>

<h4>Subtask 3 (13 points)</h4>
<ul>
  <li>$N \le 500$.</li>
  <li>$M \le \min(N, 200)$.</li>
</ul>

<h4>Subtask 4 (23 points)</h4>
<ul>
  <li>$N \le 20\,000$.</li>
  <li>$M \le \min(N, 2\,000)$.</li>
</ul>

<h4>Subtask 5 (37 points)</h4>
<ul>
  <li>No additional constraints.</li>
</ul>

<h3>Sample Grader</h3>
<p>
  The sample grader reads the input in the following format:
</p>
<pre>
N M K
C[0] C[1] ... C[N-1]
A[0] B[0][0] B[0][1] ... B[0][A[0]-1]
A[1] B[1][0] B[1][1] ... B[1][A[1]-1]
.
.
.
A[M-1] B[M-1][0] B[M-1][1] ... B[M-1][A[M-1]-1]
</pre>
<p>
  The sample grader prints the value returned by the <code>minimumInstructions</code> function.
</p>

<h3>Attachment</h3>
<p>
  The public grader, sample cases, and skeleton files for this problem is available as `paint.zip`.
</p>