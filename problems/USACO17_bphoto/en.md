Farmer John is arranging his $N$ cows in a line to take a photo
($1 \leq N \leq 100,000$).  The height of the $i$th cow in sequence is $h_i$,
and the heights of all cows are distinct.

As with all photographs of his cows, FJ wants this one to come out looking as
nice as possible.  He decides that cow $i$ looks "unbalanced" if $L_i$ and $R_i$
differ by more than factor of 2, where $L_i$ and $R_i$ are the number of cows
taller than $i$ on her left and right, respectively.  That is, $i$ is unbalanced
if the larger of $L_i$ and $R_i$ is strictly more than twice the smaller of
these two numbers.  FJ is hoping that not too many of his cows are unbalanced.

Please help FJ compute the total number of unbalanced cows.

<div class='prob-in-spec'><h4>INPUT FORMAT (standard input):</h4>
The first line of input contains $N$.  The next $N$ lines contain
$h_1 \ldots h_N$, each a nonnegative integer at most 1,000,000,000.
</div>

<div class='prob-out-spec'><h4>OUTPUT FORMAT (standard output):</h4>
Please output a count of the number of cows that are unbalanced.
</div>

<h4>SAMPLE INPUT:</h4><pre class='in'>
7
34
6
23
0
5
99
2
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
3
</pre>

In this example, the cows of heights 34, 5, and 2 are unbalanced.


Problem credits: Brian Dean