$n \times n$ 행렬이 주어집니다. 각 열에서 $k$개의 원소가 선택되도록 각 행에서 $k$개의 원소를 선택하여, 선택된 원소들의 합이 최소화되도록 하세요.

### 입력 형식

첫 번째 줄에 $n$과 $k$가 주어집니다. ($1 \le k \le n \le 50$) 다음 $n$개 줄에는 각각 $n$개의 정수가 주어지며, 주어지는 행렬을 나타냅니다. 행렬의 각 원소는 절댓값이 $10^3$을 넘지 않습니다.

### 출력 형식

위에서 명시한 대로 원소들을 선택했을 때 가능한 원소들의 합의 최솟값을 출력합니다.

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
   <td class="code-font">4 2<br/>
1 2 3 4<br/>
2 3 4 5<br/>
1 3 5 7<br/>
5 7 2 4</td>
   <td class="code-font">22</td>
  </tr>
 </tbody>
</table>
