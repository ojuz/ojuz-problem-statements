애커먼 함수는 계산복잡도 이론의 전문가들에게 잘 알려져 있습니다. 이는 두 개의 정수 인자를 가지는 함수로 아래와 같이 정의됩니다.

\\[
A(n,m) = \\left\\{ \\begin{array}{ll}
2m, & \\mbox{if} & n = 1 \\\\ 
2, & \\mbox{if} & n > 1, m = 1 \\\\
A(n-1, A(n, m-1)), & \\mbox{if} & n>1, m>1
\\end{array}\\right.
\\]

이 함수는 [원시 귀납적 함수](http://terms.naver.com/entry.nhn?docId=833406&cid=2959&categoryId=2959)가 아니며, 더욱이, $A(i, i)$는 어떤 원시 귀납적 함수보다 빨리 커집니다.

이 문제에서 여러분은 $t, n, m$이 주어질 때

\\[A(n,m) \\mod t\\]

를 계산해야 합니다. "$x \mod y$"는 $x$를 $y$로 나눈 나머지를 의미합니다. 다시 말해, $0 \le r < y$이고 $x = qy+r$를 만족하는 정수 $q$가 존재하는 $r$입니다.

### 입력 형식

첫 번째 줄에 $t$가 주어집니다. ($1 \le t \le 100$)

여러 줄에 테스트 케이스를 나타내는 $n$과 $m$이 주어집니다. ($1 \le m, n \le 100$) 두 개의 0이 주어지면 입력을 종료하면 됩니다.

### 출력 형식

각 테스트 케이스마다 아래 예제의 형식과 같이 $A(n, m) \mod t$의 값을 출력합니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">3<br/>
3 3<br/>
2 7<br/>
1 18<br/>
0 0</td>
   <td class="code-font">Case 1: 1<br/>
Case 2: 2<br/>
Case 3: 0</td>
  </tr>
 </tbody>
</table>
