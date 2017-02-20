$N$개의 정점과 $M$개의 간선으로 구성된 무방향 그래프 $G = (V,E)$를 봅시다. 이 그래프의 인접 행렬은 $N \times M$ 행렬 $A = \\{ a_{i,j} \\}$로, $a_{i,j}$가 1이면 $i$번째 정점은 $j$번 간선이 잇는 두 정점 중 하나이고, $a_{i,j}$가 0이면 그렇지 않습니다. 여러분이 해야 할 일은 행렬 $A^{T}A$의 모든 원소의 합을 구하는 것입니다.

### 입력 형식

첫 번째 줄에 두 개의 정수 $N$과 $M$ ($2 \le N \le 10 000, 1 \le M \le 100 000.$)이 주어집니다. 다음 $M$개 줄에 간선이 잇는 두 정점의 번호를 나타내는 두 개의 정수가 주어집니다. 모든 간선들은 서로 다르며 루프는 없습니다.

### 출력 형식

합을 출력합니다.

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
   <td class="code-font">4 4<br/>
1 2<br/>
1 3<br/>
2 3<br/>
2 4</td>
   <td class="code-font">18</td>
  </tr>
 </tbody>
</table>
