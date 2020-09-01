
<h3>Description</h3>
<p>
  There are $N$ attractions in the biggest theme park in Jakarta, numbered from $0$ to
  $N - 1$. These attractions are connected by $N - 1$ bidirectional roads such that there is
  a unique path between any pair of attractions through the roads. The roads are numbered from
  $0$ to $N - 2$. The $i$-th road connects the $A[i]$-th attraction and the
  $B[i]$-th attraction and takes one hour to walk through. To avoid congestion, each attraction
  is an endpoint of at most three roads.
</p><p>
  You would like to create a tour visiting all attractions exactly once. Going through many roads
  when going from an attraction to another is boring. To create a fun tour, you would like to find
  an ordering of all attractions, such that the time required to visit the next attraction is not
  longer than the time required to visit the previous attraction. In other words, you would like to
  find a sequence $P[0], P[1], \ldots, P[N-1]$ containing all integers from $0$ to
  $N - 1$ exactly once such that the time required to go from the $P[i]$-th attraction to
  the $P[i+1]$-th attraction is not longer than the time required to go from the
  $P[i-1]$-th attraction to the $P[i]$-th attraction, for $0 \lt i \lt N - 1$.
</p><p>
  You do not have the complete map of the attractions. Therefore, you have to ask several questions
  to the information centre to create a fun tour. You can ask at most $Q$ questions, each with
  two parameters $X$ and $Y$, where $0 \le X, Y \lt N$. Each question is either of the
  following:
  <ul>
    <li>How many hours are required to go from the $X$-th attraction to the $Y$-th
        attraction? In particular, if $X = Y$, the answer is $0$.</li>
    <li>How many attractions $Z$ such that you have to visit the $Y$-th attraction to go
        from the $X$-th attraction to the $Z$-th attraction? The $Y$-th attraction will
        be counted as well. In particular, if $X = Y$, the answer is $N$.</li>
  </ul>
</p>

<h3>Task</h3>
<p>
  You have to implement <code>createFunTour</code> function:
</p>
<ul>
  <li>
    <code>createFunTour(N, Q)</code> - This function will be called by the grader exactly once.
    <ul>
      <li>$N$: An integer representing the number of attractions.</li>
      <li>$Q$: An integer representing the maximum number of questions.</li>
      <li>
          This function is allowed to call two grader functions:
          <ul>
            <li>
              <code>hoursRequired(X, Y)</code>
              <ul>
                <li>$X$: An integer representing the first attraction.</li>
                <li>$Y$: An integer representing the second attraction.</li>
                <li>This function returns an integer representing hours required to go from the
                    $X$-th attraction to the $Y$-th attraction.</li>
                <li>If either $X$ or $Y$ is not an integer between $0$ and $N - 1$,
                    then you will get a WA verdict.</li>
              </ul>
            </li>
            <li>
              <code>attractionsBehind(X, Y)</code>
              <ul>
                <li>$X$: An integer representing the first attraction.</li>
                <li>$Y$: An integer representing the second attraction.</li>
                <li>This function returns an integer representing the number of attractions $Z$
                    such that you have to visit the $Y$-th attraction to go from the $X$-th
                    attraction to the $Z$-th attraction.</li>
                <li>If either $X$ or $Y$ is not an integer between $0$ and $N - 1$,
                    then you will get a WA verdict.</li>
              </ul>
            </li>
          </ul>
      </li>
      <li>This function must return an array of $N$ integers representing the permutation of
          attractions in a fun tour.</li>
    </ul>
  </li>
</ul>

<h3>Example</h3>
<p>
  In the following example, $N = 7$, $Q = 400\,000$, $A = [0, 0, 0, 1, 1, 2]$, and
  $B = [1, 5, 6, 2, 4, 3]$. The example is illustrated by the following image:
</p>
<img src="https://sandalphon.tlx.toki.id/api/v2/problems/JIDPROGCEfV7IyJ183C9fPEUmJw/render/fun1.png" style="width: 300px"/>
<p>
  Grader will call <code>createFunTour(7, 400000)</code>.
</p>
<ul>
  <li>If the contestant queries <code>hoursRequired(3, 5)</code>, then the function will return
      $4$.</li>
  <li>If the contestant queries <code>hoursRequired(5, 4)</code>, then the function will return
      $3$.</li>
  <li>If the contestant queries <code>attractionsBehind(5, 1)</code>, then the function will return
      $4$. To go from the fifth attraction to the first, second, third, and fourth attractions,
      you will have to visit the first attraction.</li>
  <li>If the contestant queries <code>attractionsBehind(1, 5)</code>, then the function will return
      $1$.</li>
  <li>The contestant can return $[3, 6, 4, 5, 2, 0, 1]$ since the hours required to visit the
      next attractions are $[4, 3, 3, 3, 2, 1]$ in order.
</ul>

<h3>Constraints</h3>
<ul>
  <li>$2 \le N \le 100\,000$.</li>
  <li>$Q = 400\,000$.</li>
  <li>It is possible to travel between any pair of attractions through the roads.</li>
  <li>Each attraction is an endpoint of at most three roads.</li>
</ul>

<h4>Subtask 1 (10 points)</h4>
<ul>
  <li>$N \le 17$.</li>
</ul>

<h4>Subtask 2 (16 points)</h4>
<ul>
  <li>$N \le 500$.</li>
</ul>

<h4>Subtask 3 (21 points)</h4>
<ul>
  <li>There is a road connecting the $i$-th attraction and the $\left\lfloor\frac{i - 1}{2}
      \right\rfloor$-th attraction, for all $1 \le i \lt N$.</li>
</ul>

<h4>Subtask 4 (19 points)</h4>
<ul>
  <li>There is at least an attraction $T$ such that for all $0 \le i \lt N$,
    <code>hoursRequired(T, i)</code> $\lt 30$ and there exists an interval $[L[i], R[i]]$
    ($0 \le L[i] \le i \le R[i] \lt N$) satisfying the following conditions:
    <ul>
      <li>
          You have to visit the $i$-th attraction to go from the $T$-th attraction to the
          $j$-th attraction if and only if $L[i] \le j \le R[i]$.
      </li>
      <li>
          If $L[i] \lt i$, then there must be exactly one attraction $X$ such that:
          <ul>
            <li>$L[i] \le X \lt i$.</li>
            <li>There is a road connecting the $i$-th attraction and the $X$-th attraction.
                </li>
          </ul>
      </li>
      <li>
          If $i \lt R[i]$, then there must be exactly one attraction $Y$ such that:
          <ul>
            <li>$i \lt Y \le R[i]$.</li>
            <li>There is a road connecting the $i$-th attraction and the $Y$-th attraction.
                </li>
          </ul>
      </li>
    </ul>
  </li>
</ul>

<h4>Subtask 5 (34 points)</h4>
<ul>
  <li>No additional constraints.</li>
</ul>

<h3>Sample Grader</h3>
<p>
  The sample grader reads the input in the following format:
</p>
<pre>
N Q
A[0] B[0]
A[1] B[1]
.
.
.
A[N-2] B[N-2]
</pre>
<p>
  The sample grader writes the integers returned by <code>createFunTour</code> if it correctly
  returns an array of $N$ integers representing the permutation of attractions in a fun tour
  and calls both <code>hoursRequired</code> and <code>attractionsBehind</code> not more than
  $Q$ times combined. Otherwise, it prints a wrong answer message.
</p>

<h3>Attachment</h3>
<p>
  The public grader, sample cases, and skeleton files for this problem is   available <a href="https://sandalphon.tlx.toki.id/api/v2/problems/JIDPROGCEfV7IyJ183C9fPEUmJw/render/fun.zip">here</a>.
</p>
