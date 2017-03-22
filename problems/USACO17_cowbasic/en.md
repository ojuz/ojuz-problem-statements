Bessie has invented a new programming language, but since there is no compiler
yet, she needs your help to actually run her programs. 

COWBASIC is a simple, elegant language. It has two key features: addition and
MOO loops. Bessie has devised a clever solution to overflow: all addition is
done modulo $10^9+7$. But Bessie's real achievement is the MOO loop, which runs
a block of code a fixed number of times. MOO loops and addition can, of course,
be nested.

Given a COWBASIC program, please help Bessie determine what number it returns.

<div class='prob-in-spec'><h4>INPUT FORMAT (standard input):</h4>
You are given a COWBASIC program at most 100 lines long, with each line being at
most 350 characters long. A COWBASIC program is a list of statements.

There are three types of statements:
<pre>
&lt;variable&gt; = &lt;expression&gt;

&lt;literal&gt; MOO {
  &lt;list of statements&gt;
}

RETURN &lt;variable&gt;
</pre>

There are three types of expressions:
<pre>
&lt;literal&gt;

&lt;variable&gt;

( &lt;expression&gt; ) + ( &lt;expression&gt; )
</pre>

A literal is a positive integer at most 100,000.

A variable is a string of at most 10 lowercase English letters.

It is guaranteed that no variable will be used or RETURNed before it is defined.
It is guaranteed that RETURN will happen exactly once, on the last line of the
program.
</div>

<div class='prob-out-spec'><h4>OUTPUT FORMAT (standard output):</h4>
Output a single positive integer, giving the value of the RETURNed variable.
</div>

<div class='prob-section'><h4>Scoring</h4>
<ul><li>
In 20 percent of all test cases - MOO loops are not nested.
</li><li>
In another 20 percent of all test cases - The program only has 1 variable. MOO
loops can be nested.
</li><li>
In the remaining test cases, there are no further restrictions.
</li></ul>
</div>

<h4>SAMPLE INPUT:</h4><pre class='in'>
x = 1
10 MOO {
  x = ( x ) + ( x )
}
RETURN x
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
1024
</pre>
This COWBASIC program computes $2^{10}$.
<h4>SAMPLE INPUT:</h4><pre class='in'>
n = 1
nsq = 1
100000 MOO {
  100000 MOO {
    nsq = ( nsq ) + ( ( n ) + ( ( n ) + ( 1 ) ) )
    n = ( n ) + ( 1 )
  }
}
RETURN nsq
</pre><h4>SAMPLE OUTPUT:</h4> <pre class='out'>
4761
</pre>
This COWBASIC program computes $(10^5*10^5+1)^2$ (modulo $10^9 + 7$).

Problem credits: Jonathan Paulson