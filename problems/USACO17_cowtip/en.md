Farmer John occasionally has trouble with bored teenagers who visit his farm at
night and tip over his cows.  One morning, he wakes up to find it has happened
again -- his $N^2$ cows  began the night grazing in a perfect $N \times N$
square grid arrangement ($1 \leq N \leq 10$), but he finds that some of them are
now tipped over.  

Fortunately, Farmer John has used parts from his tractor and forklift to build a
glorious machine, the Cow-Untipperator 3000, that can flip over large groups of
cows all at once, helping him put all his cows back on their feet as quickly as
possible.  He can apply the machine to any "upper-left rectangle" in his grid of
cows -- a rectangular sub-grid that contains the upper-left cow.  When he does
so, the machine flips over every cow in this rectangle,  placing tipped cows
back on their feet, but unfortunately also tipping over cows that were already
on their feet!  In other words, the machine "toggles" the state of each cow in
the rectangle.

Farmer John figures that by applying his machine sufficiently many times to the
appropriate collection of rectangles, he can eventually restore all the cows to
their rightful, un-tipped states.  Please help him determine the minimum number
of applications of his machine needed to do this.  

Note that applying the machine to the same rectangle twice would be pointless,
since this would have no net impact on the cows in the rectangle.  Therefore,
you should only consider applying the machine to each upper-left rectangle
possibly only once.

<div class='prob-in-spec'><h4>INPUT FORMAT (standard input):</h4>
The first line of the input is the integer $N$.

Each of the $N$ subsequent lines contains a string of $N$ characters, each
either 0 (representing an up-tipped cow) or 1 (representing a tipped cow).
</div>

<div class='prob-out-spec'><h4>OUTPUT FORMAT (standard output):</h4>
Please output the minimum number of times Farmer John needs to apply the
Cow-Untipperator 3000 to restore all his cows to their feet.
</div>

<h4>SAMPLE INPUT:</h4><pre class='in'>
3
001
111
111
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
2
</pre>

In this example, if FJ applies his machine to the entire herd of cows (which is
a valid upper-left rectangle), he will
toggle their state to the following:

<pre>
110
000
000
</pre>

All that remains is to apply the machine to the upper-left rectangle containing
the two 1s, and he is finished.  In total, this is just 2 applications.


Problem credits: Nathan Pinsker