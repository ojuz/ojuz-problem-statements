상수는 어제 석환이로부터 거대한 저택을 매입했습니다. 상수는 이 저택을 지키는 경비원들이 필요하다고 생각하여 모집 공고를 올렸고, 그 결과 $n$명이 지원했습니다. 상수는 편의상 이들에게 1 이상 $n$ 이하의 번호를 붙였습니다. 

$i$ ($1 \le i \le n$)번 경비원에게는 가장 좋아하는 수 $a_{i}$가 있습니다. 이 값은 항상 양의 정수입니다. 상수는 $i$번 경비원과 $j$번 경비원이 같이 경비를 설 때, $a_{i}$와 $a_{j}$의 최대공약수가 2 이상이면, 서로 친밀감을 느껴서 대화하느라 경비를 제대로 서지 않는다고 생각합니다.

따라서 상수는 경비원들을 2명 이상 고용하되, 이들 중 두 명을 어떻게 골라도 좋아하는 수의 최대공약수가 1이 되도록 하려고 합니다. 이를 위해 상수는 고용할 수 있는 모든 경우의 수를 따져보고자 합니다. 상수를 도와주세요.

### 입력 형식

첫 번째 줄에 $n$이 주어집니다. 두 번째 줄에 $a_{1}, a_{2}, \cdots, a_{n}$이 공백을 사이로 두고 차례대로 주어집니다.

### 출력 형식

첫 번째 줄에 상수가 경비원들을 고용할 수 있는 모든 경우의 수를 1,000,000,007 ($= 10^9 + 7$)로 나눈 나머지를 출력합니다.

### 부분문제

<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
<thead>
 <tr>
  <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2">$n$　</th>
  <th class="col-sm-3 col-md-3 col-lg-3">$\max\{a_{1}, a_{2}, \cdots, a_{n}\}$</th>
  <th class="">추가 제약 사항</th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>8</td>
  <td>$2 \le n \le$ $20$</td>
  <td>$\le$ $2,222$</td>
  <td>-</td>
 </tr>
 <tr>
  <td>2</td>
  <td>13</td>
  <td>$2 \le n \le$ $44$</td>
  <td>$=$ $n$</td>
  <td>모든 $1 \le i \le n$에 대해 $a_{i} = i$</td>
 </tr>
 <tr>
  <td>3</td>
  <td>16</td>
  <td>$2 \le n \le$ $2,222$</td>
  <td>$\le$ $44$</td>
  <td>-</td>
 </tr>
 <tr>
  <td>4</td>
  <td>27</td>
  <td>$2 \le n \le$ $2,222$</td>
  <td>$\le$ $2,222$</td>
  <td>모든 $1 \le i < j \le n$에 대해 $a_{i} \neq a_{j}$</td>
 </tr>
 <tr>
  <td>5</td>
  <td>36</td>
  <td>$2 \le n \le$ $2,222$</td>
  <td>$\le$ $2,222$</td>
  <td>-</td>
 </tr>
</tbody>
</table>
</div>

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 1</th>
   <th style="width: 50%;">출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">4<br>1 2 3 4</td>
   <td class="code-font">7</td>
  </tr>
 </tbody>
</table>

이 예제에서 가능한 경우는 아래와 같습니다.

* {1, 2}
* {1, 3}
* {1, 4}
* {2, 3}
* {3, 4}
* {1, 2, 3}
* {1, 3, 4}

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 2</th>
   <th style="width: 50%;">출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">5<br>10 12 14 16 18</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>

각 경비원들이 가장 좋아하는 수가 모두 짝수이기 때문에 고용할 수 있는 경우가 없습니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 3</th>
   <th style="width: 50%;">출력 3</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">44<br>1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44</td>
   <td class="code-font">900563</td>
  </tr>
 </tbody>
</table>
	
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 4</th>
   <th style="width: 50%;">출력 4</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">5<br>3 21 7 45 15</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>
</table>
	
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 5</th>
   <th style="width: 50%;">출력 5</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">3<br>3 2 3</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>
