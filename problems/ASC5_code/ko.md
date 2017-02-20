그레이 코드에서 영감을 받아서, 승현이는 그만의 새로운 코드를 개발해 냈습니다. 그레이 코드와 다르게, Ainta Code에서는 인접한 두 단어의 서로 다른 비트가 많습니다.

더 자세하게 쓰자면, $s = 2^{n}$이라고 할 때 모든 $n$개 비트 문자열들의 순열 $a_{1}, a_{2}, \cdots, a_{s}$가 다음 조건을 만족한다면 *Ainta Code*라고 부릅니다: 모든 $1 \le k < s$에 대해 $a_{k}$와 $a_{k+1}$가 적어도 $\lfloor n/2 \rfloor$개의 다른 비트를 가지고 있고 $a_{1}$과 $a_{s}$ 역시 적어도 $\lfloor n/2 \rfloor$개의 다른 비트를 가지고 있습니다.

$n$이 주어질 때 여러분은 $n$비트 Ainta Code를 찾거나 없다는 것을 판정해야 합니다.

### 입력 형식

첫 번째 줄에 $n$이 주어집니다. ($2 \le n \le 12$)

### 출력 형식

$n$비트 Ainta Code에 등장하는 $2^{n}$개의 $n$비트 문자열을 한 줄에 하나씩 출력합니다. 만약 존재하지 않는다면, 첫 번째 줄에 "`none`"을 출력합니다.

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
   <td class="code-font">4</td>
   <td class="code-font">0000<br/>
1111<br/>
0001<br/>
1110<br/>
0010<br/>
1101<br/>
0011<br/>
1100<br/>
0101<br/>
1011<br/>
0100<br/>
1010<br/>
0110<br/>
1000<br/>
0111<br/>
1001</td>
  </tr>
 </tbody>
</table>
