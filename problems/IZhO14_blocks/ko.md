길이가 $N$인 수열 $A$가 주어집니다. 수열의 "분할 값"을 수열을 $K$개의 묶음으로 분할했을 때 각 묶음의 최댓값들의 합으로 정의합시다. (각 묶음은 연속해야 합니다) $K$가 주어질 때 최소한의 분할 값을 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 두 개의 정수 $N$과 $K$가 주어집니다. 두 번째 줄에 $N$개의 정수 $A_{1}, A_{2}, \cdots, A_{N}$ ($1 \le A_{i} \le 10^{6}$)가 주어집니다.

### 출력 형식

최소한의 분할 값을 출력합니다.

### 서브태스크

#### 서브태스크 1 (14점)

* $1 \le N \le 100, 1 \le K \le \min(N,5).$

#### 서브태스크 2 (18점)

* $1 \le N \le 20, 1 \le K \le \min(N,20).$

#### 서브태스크 3 (21점)

* $1 \le N \le 100, 1 \le K \le \min(N,100).$

#### 서브태스크 4 (47점)

* $1 \le N \le 100 000, 1 \le K \le \min(N,100).$

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
   <td class="code-font">5 1<br/>
1 2 3 4 5</td>
   <td class="code-font">5</td>
  </tr>
  <tr>
   <td class="code-font">5 2<br/>
1 2 3 4 5</td>
   <td class="code-font">6</td>
  </tr>
 </tbody>
</table>