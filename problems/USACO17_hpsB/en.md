You have probably heard of the game "Rock, Paper, Scissors".  The cows like to
play a similar game they call "Hoof, Paper, Scissors". 

The rules of "Hoof, Paper, Scissors" are simple.  Two cows play against
each-other.  They both count to three and then each simultaneously makes a
gesture that represents either a hoof, a piece of paper, or a pair of scissors. 
Hoof beats scissors (since a hoof can smash a pair of scissors), scissors beats
paper (since scissors can cut paper), and paper beats hoof (since the hoof can
get a papercut).   For example, if the first cow makes a "hoof" gesture and the
second a "paper" gesture, then the second cow wins.  Of course, it is also
possible to tie, if both cows make the same gesture.

Farmer John watches in fascination as two of his cows play a series of $N$
games of "Hoof, Paper,  Scissors" ($1 \leq N \leq 100$).  Unfortunately, while
he can see that the cows are making three distinct types of gestures, he can't
tell which one represents "hoof", which one represents "paper" and which one
represents "scissors" (to Farmer John's untrained eye, they all seem to be
variations on "hoof"...)

Not knowing the meaning of the three gestures, Farmer John assigns them numbers
1, 2, and 3. Perhaps gesture 1 stands for "hoof", or maybe it stands for
"paper"; the meaning is not clear to him.  Given the gestures made by both cows
over all $N$ games, please help Farmer John determine the maximum possible
number of games the first cow could have possibly won, given an appropriate
mapping between numbers and their respective gestures.

<div class='prob-in-spec'><h4>INPUT FORMAT (standard input):</h4>
The first line of the input file contains $N$. 

Each of the remaining $N$ lines contain two integers (each 1, 2, or 3),
describing a game from Farmer John's perspective.
</div>

<div class='prob-out-spec'><h4>OUTPUT FORMAT (standard output):</h4>
Print the maximum number of games the first of the two cows could possibly have
won.
</div>

<h4>SAMPLE INPUT:</h4><pre class='in'>
5
1 2
2 2
1 3
1 1
3 2
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
2
</pre>

One solution (of several) for this sample case is to have 1 represent
"scissors", 2 represent "hoof", and 3 represent "paper".  This assignment gives
2 victories to the first cow ("1 3" and "3 2"). No other assignment leads to
more victories.

Problem credits: Brian Dean