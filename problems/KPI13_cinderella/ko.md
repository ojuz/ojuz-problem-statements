악랄한 승현이는 석환이를 비둘기들이 가득한 Pigeon World로 보냈습니다! Pigeon World는 $2n \times 2n$ 크기의 격자판이며, 각 격자에는 $1$마리 이상 $4n^{2}$ 이하의 비둘기들이 들어 있고, 임의의 서로 다른 두 격자에 들어 있는 비둘기의 수가 같을 수는 없습니다. 비둘기들은 인접한 칸에 비둘기들이 많이 보이면 더 많이 울어 석환이를 괴롭게 만들 겁니다. 따라서 똑똑한 석환이는 비둘기들의 수를 적절히 배열해서, 서로 인접한 두 칸에 있는 비둘기들의 수의 합 중 최댓값을 최소화하려고 합니다. 두 칸이 인접하다는 것은 접하는 변이 있다는 것입니다. 석환이를 도와 문제를 해결합시다.

### 입력 형식

첫 번째 줄에 Pigeon World의 크기를 결정하는 데에 필요한 정수 $n$ ($1 \le n \le 100$)이 주어집니다.

### 출력 형식

$2n$개의 줄을 출력하고 각 줄마다 $2n$개의 정수를 출력합니다. 이 중 $i$ ($1 \le i \le 2n$)번째 줄의 $j$ ($1 \le j \le 2n$)번째 숫자는 석환이가 배열한 Pigeon World의 $i$행 $j$열에 들어 있는 비둘기의 수가 되어야 합니다. 출력 가능한 경우가 여러 개 있다면 아무거나 출력하면 됩니다.

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
   <td class="code-font">1</td>
   <td class="code-font">2 3<br/>4 1</td>
  </tr>
 </tbody>
</table>