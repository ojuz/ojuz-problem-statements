Having become bored with standard 2-dimensional artwork (and also frustrated at
others copying her work), the great bovine artist Picowso has decided to switch
to a more minimalist, 1-dimensional style.

Although, her paintings can now be described by a 1-dimensional array of colors
of length $N$ ($1 \leq N \leq 100,000$), her painting style remains unchanged:
she starts with a blank canvas and layers upon it a sequence of "rectangles" of
paint, which in this 1-dimensional case are simply intervals.  She uses each of
the colors $1 \ldots N$ exactly once, although just as before, some colors might
end up being completely  covered up by the end.

To Picowso's great dismay, her competitor Moonet seems to have figured out how
to copy even these 1-dimensional paintings, using a similar strategy to the
preceding problem: Moonet will paint a set of disjoint intervals, wait for them
to dry, then paint another  set of disjoint intervals, and so on.  Moonet can
only paint at most one interval of each color over the entire process.  Please compute
the number of such rounds needed for Moonet to copy a given 1-dimensional
Picowso painting.

<div class='prob-in-spec'><h4>INPUT FORMAT (standard input):</h4>
The first line of input contains $N$, and the next $N$ lines contain an integer
in the range $0 \ldots N$ indicating the color of each cell in the 1-dimensional
painting (0 for a blank cell).
</div>

<div class='prob-out-spec'><h4>OUTPUT FORMAT (standard output):</h4>
Please output the minimum number of rounds needed to copy this painting, or -1
if this could not have possibly been an authentic work of Picowso (i.e., if she
could not have painted it using a layered sequence of intervals, one of each
color).
</div>

<h4>SAMPLE INPUT:</h4><pre class='in'>
7
0
1
4
5
1
3
3
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
2
</pre>

In this example, the interval of color 1 must be painted in an earlier round
than the intervals of colors 4 and 5, so at least two rounds are needed.


Problem credits: Brian Dean