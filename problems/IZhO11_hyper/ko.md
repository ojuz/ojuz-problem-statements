인덱스가 $1$ 이상 $N$ 이하인 4차원 배열 $X$가 있습니다. 여러분이 해야 할 일은 새로운 4차원 배열 $Y$를 만드는 것입니다. $Y$의 각 원소는 이렇게 계산됩니다. $Y[i_{1}, i_{2}, i_{3}, i_{4}] = min(X[j_{1}, j_{2}, j_{3}, j_{4}])$ (단 $1 \le i_{k} \le N-M+1, i_{k} \le j_{k} \le i_{k} + M - 1$이며, $M$은 입력에서 주어집니다.)

### 입력 형식

첫 번째 줄에 두 개의 정수 $N$과 $M$이 주어집니다. ($1 \le M \le N$) 두 번째 줄에는 배열 $X$의 원소들이 주어집니다. 원소들의 개수는 150만개를 넘지 않으며, 각 원소는 절댓값이 $10^{9}$ 이하인 정수입니다. 이 배열은 아래 의사 코드와 같이 입력받는 것을 권장합니다.

<pre>
for i = 1 to N:
    for j = 1 to N:
        for k = 1 to N:
            for l = 1 to N:
                read X[i, j, k, l]
</pre>

### 출력 형식

배열 $X$가 주어졌던 것과 같은 방식으로 배열 $Y$의 각 원소를 출력합니다.

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
   <td class="code-font">1 1<br/>
1</td>
   <td class="code-font">1</td>
  </tr>
  <tr>
   <td class="code-font">3 2<br/>
3 1 4 -4 0 4 0 0 -3 0 -2 -5 5 3 5 -4 4 -3 -5 -4 -4 5 -1 0 -3 -2 -1 2 -5 -5 -1 1 1 -4 3 5 3 -3 -3 3 0 1 4 -1 -2 3 -2 5 4 -1 -5 3 -4 0 -3 -1 3 -1 4 4 -1 -5 -3 4 -4 5 1 5 -4 3 2 2 -2 -2 4 2 -4 -3 1 3 1</td>
   <td class="code-font">-5 -5 -4 -3 -5 -5 -4 -5 -5 -5 -5 -5 -4 -5 -4 -5</td>
  </tr>
 </tbody>
</table>