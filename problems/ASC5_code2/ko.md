*참고: 이 문제는 실제 대회에 출제된 문제를 변형한 것입니다.*

심심한 승현이는 Ainta Code에 이어서 Ainta Code II도 만들었습니다.

더 자세하게 쓰자면, $s = 2^{n}$이라고 할 때 모든 $n$개 비트 문자열들의 순열 $a_{1}, a_{2}, \cdots, a_{s}$가 다음 조건을 만족한다면 *Ainta Code II*라고 부릅니다: 모든 $1 \le k < s$에 대해 $a_{k}$와 $a_{k+1}$가 적어도 $n-1$개의 다른 비트를 가지고 있고 $a_{1}$과 $a_{s}$ 역시 적어도 $n-1$개의 다른 비트를 가지고 있습니다.

$n$이 주어질 때 여러분은 $n$비트 Ainta Code II를 찾거나 없다는 것을 판정해야 합니다.

### 입력 형식

첫 번째 줄에 $n$이 주어집니다. ($2 \le n \le 12$)

### 출력 형식

$n$비트 Ainta Code II에 등장하는 $2^{n}$개의 $n$비트 문자열을 한 줄에 하나씩 출력합니다. 만약 존재하지 않는다면, 첫 번째 줄에 "`none`"을 출력합니다.

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
   <td class="code-font">2</td>
   <td class="code-font">00<br/>
01<br/>
10<br/>
11</td>
  </tr>
 </tbody>
</table>
