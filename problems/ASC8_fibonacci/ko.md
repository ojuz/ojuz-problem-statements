정수들로 구성된 수열

\\[ {\mathcal{F}}\_{r} = {a}\_{0}, {a}\_{1}, \cdots, {a}\_{n}, \cdots, \\]

가 $a_{0} = 1, a_{1} = 1, a_{i} = (a_{i-2} + a_{i-1}) \mod r$ ($i \ge 2$)를 만족할 때, 이 수열은 법 $r$ 피보나치 수열이라고 부릅니다.

숫자 $p > 0$은 어떤 $i_{0}$이 존재해서 모든 $i \ge i_{0}$에 대해 $a_{i} = a_{i+p}$이 성립한다면 *수열의 주기*라고 부릅니다. 수열에 주기가 있다면 이 수열은 *주기적*이라고 합니다. 당연히, 만약 어떤 수열이 주기적이라면, 이 주기들에는 짧은 주기도 있고 긴 주기도 있겠죠..

$r$이 주어질 때 ${\mathcal{F}}\_{r}$에 주기가 존재하는지 알아내고, 만약 존재한다면 가장 짧은 주기가 무엇인지 찾는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 $r$이 주어집니다. ($2 \le r \le 2 \times 10^{9}$)

### 출력 형식

만약 ${\mathcal{F}}\_{r}$이 주기적이라면, 가장 짧은 주기를 출력합니다. 그렇지 않다면, 0을 출력합니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2</td>
   <td class="code-font">3</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">3</td>
   <td class="code-font">8</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">5</td>
   <td class="code-font">20</td>
  </tr>
 </tbody>
</table>