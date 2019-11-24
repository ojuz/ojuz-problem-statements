JOIOJI-san is JOI-san's uncle. The name "JOIOJI" is made of the characters-"J", "O", "I". Recently, JOIOJI-san has a new child. JOIOJI-san wants his child's name to consist of only of the characters "J", "O", "I" and also wants the name to have an equal number of  "J", "O" and "I".

JOIOJI-san's house has an ancestral scroll. On the scroll, there is a poem of $N$ characters where each character is either "J", "O" or "I".

JOIOJI-san wants to name his child with the longest subsequence of the poem that satisfies the condition mentioned above.

(Translator note: ojisan is an honorific in Japanese to refer to one's uncle)
### Task

JOIOJI-san gives you the poem that is written on the scroll. Help him find the longest substring that contains an equal number of "J", "O" and "I".

### Input Format

Input will be given from the standard input.

* The first line will contain one integer, $N$, which is the number of characters the poem has.
* The following line will contain a string $S$ of length $N$, which represents the poem. It is guaranteed that $S$ will only contain the characters "J", "O" and "I" only.

### Output Format

Print output to the standard output.

Print a single integer, the maximum length of the longest subsequence of the poem that contains an equal number of "J", "O" and "I". If there are no substrings that fit the criteria for naming JOIOJI-san's child, print $0$.

### Constraints

For all test cases, the input will satisfy the following conditions.

* $1 \le N \le 200,000$

### Subtasks

#### Subtask 1 [5 Marks]

* $N \le 200$

#### Subtask 2 [15 Marks]

* $N \le 4,000$

#### Subtask 3 [80 Marks]

* $N \le 200,000$

### Sample Testcases

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>Sample Input</th>
   <th>Sample Output</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">10<br/>
JOIIJOJOOI</td>
   <td class="code-font">6</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">8<br/>
IOIIJIIO
</td>
   <td class="code-font">0</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">20<br/>
JJIOOIJIJOIOJIOJOOIJ</td>
   <td class="code-font">15</td>
  </tr>
 </tbody>
</table>
