The Xedef Courier Company provides air package
delivery among several cities.  Some of these
cities are Xedef <i>hubs</i> where special
processing facilities are established.
Each of Xedef's aircraft shuttles 
back and forth between
one pair of cities, carrying packages in either
direction as required.
<p>
To be shipped from one city to another, a 
package must be transported by a sequence of hops,
where each hop carries the package between
a pair of cities served by one of the
aircraft.  Furthermore, the sequence must
include at least one of Xedef's hubs.
</p><p>To facilitate routing, Xedef wishes to encode
the length of the shortest sequence of hops from every city to every hub on the
shipping label of every package.  
(The length of the shortest sequence leading from a hub to itself is zero.)
Obviously, a compact representation of this information is required.
</p><p>
You are to implement two procedures,
<b>encode(N,H,P,A,B)</b> and <b>decode(N,H)</b>.
<b>N</b> is the number of cities and <b>H</b> is the number of hubs.  
Assume that the cities are numbered from 0 to N-1, and that the hubs are
the cities with numbers between 0 and H-1. 
Further assume that N &#8804; 1000 and H &#8804; 36.
<b>P</b> is the number of pairs of cities connected by aircraft.  
All (unordered) pairs of cities will be distinct.
<b>A</b> and <b>B</b> are arrays of size P, such that
the first pair of connected cities is (A[0],B[0]), the
second pair is (A[1],B[1]), and so on.
</p><p>
<b>encode</b> must compute a sequence of bits
from which <b>decode</b> can determine the number of hops
from every city to every hub.  <b>encode</b> will
transmit the sequence of bits to the grading
server by a sequence of calls to <b>encode_bit(b)</b>
where <b>b</b> is either 0 or 1.  <b>decode</b>
will receive the sequence of bits from the grading server
by making calls to <b>decode_bit</b>.
The <i>i</i>-th call to <b>decode_bit</b> will return
the value of <b>b</b> from the <i>i</i>-th call to
<b>encode_bit(b)</b>. 
Note that you must ensure that the number of 
times <b>decode</b> calls <b>decode_bit</b> will 
always be at most equal to the number of times
<b>encode</b> previously called <b>encode_bit(b)</b>.
</p><p>
After decoding the numbers of hops,
<b>decode</b> must call <b>hops(h,c,d)</b> for
every hub <b>h</b> and every city <b>c</b> 
(including every hub, that is, also for <b>c</b>=<b>h</b>), giving the
minimum number <b>d</b> of hops necessary to ship a package
between <b>h</b> and <b>c</b>.  That is, there must be
N*H calls to <b>hops(h,c,d)</b>.  The order does not matter.
You are guaranteed that it is always possible to ship a package
between every hub and every city.
</p><p>
<i>Note: <b>encode</b> and <b>decode</b>
must communicate only through the specified interface.
Shared variables, file access and network access are prohibited.
In C or C++, you may declare persistent variables to
be <tt>static</tt> to retain information for <b>encode</b> or <b>decode</b>,
while preventing them from being shared.  In Pascal, you may declare 
persistent variables in the <tt>implementation</tt> part of
your solution files.</i>

</p><h3>Example</h3>
<p>
As an example,
consider the diagram on the right.
It shows five cities (N=5) connected by seven aircraft (P=7).
Cities 0, 1 and 2 are hubs (H=3).
One hop is needed to ship a package between hub 0 and city 3,
whereas 2 hops are needed to ship a package between hub 2 and city 3.
The data for this example are in <tt>grader.in.1</tt>.
</p><p>
The entries in the following table are all <b>d</b>-values
that <b>decode</b> must deliver by calling <b>hops(h,c,d)</b>:
</p>
<table class="table table-bordered">
<tbody><tr><th colspan="2" rowspan="2">d</th><th colspan="5">City c
</th></tr><tr><th>0</th><th>1</th><th>2</th><th>3</th><th>4
</th></tr><tr><th rowspan="3">Hub h</th><th>0</th><td>0</td><td>1</td><td>1</td><td>1</td><td>1
</td></tr><tr><th>1</th><td>1</td><td>0</td><td>1</td><td>1</td><td>1
</td></tr><tr><th>2</th><td>1</td><td>1</td><td>0</td><td>2</td><td>2
</td></tr></tbody></table>


<h3>Subtask 1 [25 points]</h3>
<b>encode</b> must make no more than 16&#8201;000&#8201;000 calls to <b>encode_bit(b)</b>.
<h3>Subtask 2 [25 points]</h3>
<b>encode</b> must make no more than 360&#8201;000 calls to <b>encode_bit(b)</b>.
<h3>Subtask 3 [25 points]</h3>
<b>encode</b> must make no more than 80&#8201;000 calls to <b>encode_bit(b)</b>.
<h3>Subtask 4 [25 points]</h3>
<b>encode</b> must make no more than 70&#8201;000 calls to <b>encode_bit(b)</b>.

<h3>Implementation Details</h3>
<ul>
<li>To be implemented by contestant:<ul><li> <tt>encoder.c</tt> or <tt>encoder.cpp</tt> or <tt>encoder.pas</tt>
</li><li> <tt>decoder.c</tt> or <tt>decoder.cpp</tt> or <tt>decoder.pas</tt></li></ul>
</li><li>Contestant interface: <ul><li><tt>encoder.h</tt> or <tt>encoder.pas</tt>
</li><li><tt>decoder.h</tt> or <tt>decoder.pas</tt></li></ul>
</li><li>Grader interface: <tt>grader.h</tt> or <tt>graderlib.pas</tt>
</li><li>Sample grader: <tt>grader.c</tt> or <tt>grader.cpp</tt> or <tt>grader.pas</tt> <i>and</i> <tt>graderlib.pas</tt>
</li><li>Sample grader input:  <tt>grader.in.1</tt> <tt>grader.in.2</tt> etc.
<br>
<i>Note: The first line of each file contains <tt>N</tt> <tt>P</tt> <tt>H</tt>.
The next <tt>P</tt> lines contain
the pairs of cities <tt>A[0] B[0]</tt>, <tt>A[1] B[1]</tt>, etc.
The next <tt>H*N</tt> lines contain
the numbers of hops from each hub to each city (including itself and all other hubs); 
that is, the number of hops from a hub <tt>i</tt> to a city <tt>j</tt> is in the <tt>i</tt>*<tt>N</tt>+<tt>j</tt>+1 -st of these lines. 
</i>
</li><li>Expected output for sample grader input: 
<ul><li>If the implementation is correct for subtask 1, the output will contain <tt>OK 1</tt>
</li><li>If the implementation is correct for subtask 2, the output will contain <tt>OK 2</tt>
</li><li>If the implementation is correct for subtask 3, the output will contain <tt>OK 3</tt>
</li><li>If the implementation is correct for subtask 4, the output will contain <tt>OK 4</tt>
</li></ul>
</ul>
