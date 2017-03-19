Jack and Jill play a game called <i>Hotter, Colder</i>.
Jill has a number between 1 and N, and Jack makes 
repeated attempts to guess it.
<p>
Each of Jack's guesses is a number between 1 and N.  In
response to each guess, Jill answers <i>hotter</i>,
<i>colder</i> or <i>same</i>.  For Jack's first
guess, Jill answers <i>same</i>.  For the remaining
guesses Jill answers:
<ul><li> <i>hotter</i> if this guess
is closer to Jill's number than his previous guess
<li> <i>colder</i> if this guess
is farther from Jill's number than his previous guess
<li><i>same</i> if this guess is neither closer to nor further from
Jill's number than his previous guess.
</ul>
<p>
You are to implement a procedure <b>HC(N)</b> that plays Jack's role.
This implementation may repeatedly call <b>Guess(G)</b>,
with <b>G</b> a number between 1 and N.
<b>Guess(G)</b> will return 1 to indicate <i>hotter</i>,
-1 to indicate <i>colder</i> or 0 to indicate <i>same</i>.
<b>HC(N)</b> must return Jill's number.
<h3>Example</h3>
As example,
assume N=5, and Jill has chosen the number 2.
When procedure <b>HC</b> makes the following sequence of calls to <b>Guess</b>,
the results in the second column will be returned.

<table class="table table-bordered">
<tr><th>Call<th>Returned value<th>Explanation
<tr><td><b>Guess(5)</b><td>0<td>Same (first call)
<tr><td><b>Guess(3)</b><td>1<td>Hotter
<tr><td><b>Guess(4)</b><td>-1<td>Colder
<tr><td><b>Guess(1)</b><td>1<td>Hotter
<tr><td><b>Guess(3)</b><td>0<td>Same
</table>

At this point Jack knows the answer, and <b>HC</b> should return 2.
It has taken Jack 5 guesses to determine Jill's number.  You can do better.

<h3>Subtask 1 [25 points]</h3>
<b>HC(N)</b> must call <b>Guess(G)</b> at most 500 times.
There will be at most 125&thinsp;250 calls to <b>HC(N)</b>, with N between
1 and 500.
<h3>Subtask 2 [25 points]</h3>
<b>HC(N)</b> must call <b>Guess(G)</b> at most <b>18</b> times.
There will be at most 125&thinsp;250 calls to <b>HC(N)</b> with N
between 1 and 500.
<h3>Subtask 3 [25 points]</h3>
<b>HC(N)</b> must call <b>Guess(G)</b> at most <b>16</b> times.
There will be at most 125&thinsp;250 calls to <b>HC(N)</b> with N
between 1 and 500.
<h3>Subtask 4 [up to 25 points]</h3>
Let W be the largest integer, such that 2<sup>W</sup>&#8804;3N.
For this subtask your solution will score:
<ul>
  <li>0 points, if <b>HC(N)</b> calls <b>Guess(G)</b>  2W times or more,</li>
  <li>25&#945; points, where &#945; is the largest real number, such that 0&lt;&#945;&lt;1 and 
      <b>HC(N)</b> calls <b>Guess(G)</b> at most 2W-&#945;W times, </li>
  <li>25 points, if <b>HC(N)</b> calls <b>Guess(G)</b> at most W times.</li>
</ul>
<p>There will be at most 1&thinsp;000&thinsp;000 calls to <b>HC(N)</b>
with N between 1 and 500&thinsp;000&thinsp;000.
<p>
<i>Be sure to initialize any variables used by <b>HC</b> every time it is called.</i>
</p>

<h3>Implementation Details</h3>
<ul>
<li>Use the <a href="http://www.ioi2010.org/environment/runc.shtml">RunC programming and test environment</a>
<li>Implementation folder: <tt>/home/ioi2010-contestant/hottercolder/</tt> (prototype: <a href="hottercolder.zip">hottercolder.zip</a>)
<li>To be implemented by contestant: <tt>hottercolder.c</tt> or <tt>hottercolder.cpp</tt> or <tt>hottercolder.pas</tt>
<li>Contestant interface: <tt>hottercolder.h</tt> or <tt>hottercolder.pas</tt>
<li>Grader interface: <tt>grader.h</tt> or <tt>graderlib.pas</tt>
<li>Sample grader: <tt>grader.c</tt> or <tt>grader.cpp</tt> or <tt>grader.pas</tt> <i>and</i> <tt>graderlib.pas</tt>
<li>Sample grader input:  <tt>grader.in.1</tt> <tt>grader.in.2</tt>. <br><i>Note: The input file contains several lines, each containing N and Jill's number.</I>
<li>Expected output for sample grader input: the grader will create files <tt>grader.out.1</tt> <tt>grader.out.2</tt> etc.  
<ul>
<li>If the implementation correctly implements Subtask 1, one line of output will contain <tt>OK 1</tt>
<li>If the implementation correctly implements Subtask 2, one line of output will contain <tt>OK 2</tt>
<li>If the implementation correctly implements Subtask 3, one line of output will contain <tt>OK 3</tt>
<li>If the implementation correctly implements Subtask 4, one line of output will contain <tt>OK 4 alpha &alpha;</tt>
</ul>
<li>Compile and run (command line): <tt>runc grader.c</tt> or <tt>runc grader.cpp</tt> or <tt>runc grader.pas</tt>
<li>Compile and run (gedit plugin):  <i>Control-R</i>, while editing any implementation file.
<li>Submit (command line):  <tt>submit grader.c</tt> or <tt>submit grader.cpp</tt> or <tt>submit grader.pas</tt>
<li>Submit (gedit plugin):  <i>Control-J</i>, while editing any implementation or grader file.
</ul>
