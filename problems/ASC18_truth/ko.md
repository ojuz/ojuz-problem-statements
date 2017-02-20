어떤 변수들로 이루어진 논리식이 주어졌을 때, 이 논리식이 참이 되는 변수값이 존재하는지 찾는 문제인 충족 가능성 문제(satisfiability problem, SAT)는 잘 알려진 NP-완전 문제입니다. 대부분의 사람들은 이 문제를 다항 시간 안에 푸는 알고리즘이 존재하지 않는다고 생각합니다.

이 문제는 충족 가능성 문제의 대안입니다. 여러분에게 상수 '`0`', '`1`', 부정(NOT) '`!`', 논리곱 '`&`', 논리합 '`|`' (우선 순위가 높은 순에서 낮은 순으로 나열했습니다)로 구성된 논리식이 주어집니다. 이 논리식은 괄호를 포함하지 않습니다. 여러분은 이 논리식에 괄호를 추가해서 논리식의 값이 참이 되도록 할 수 있는지를 결정하는 프로그램을 작성해야 합니다.

### 입력 형식

첫 번쨰 줄에 괄호를 포함하지 않는 논리식이 주어집니다. 논리식의 길이는 500글자를 넘지 않습니다.

### 출력 형식

논리식에 괄호를 적절히 넣어 참을 만들 수 없다면 "`Impossible`"을 출력합니다. 참을 만들 수 있다면 괄호를 추가한 논리식을 출력합니다. 다만 출력한 논리식의 길이가 10000글자보다 길다면 오답 처리됩니다. (자비롭죠..)

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
   <td class="code-font">1|1&0</td>
   <td class="code-font">1|(1&0)</td>
  </tr>
  <tr>
   <td class="code-font">0&0</td>
   <td class="code-font">Impossible</td>
  </tr>
  <tr>
   <td class="code-font">!0&0</td>
   <td class="code-font">!(0&0)</td>
  </tr>
 </tbody>
</table>