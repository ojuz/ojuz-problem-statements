승현이 앞에 두 수 $N$, $x$와 길이가 $N$인 수열이 놓여 있습니다. 똑똑한 승현이는 연속되는 원소들의 논리적 배타합(XOR)이 $x$보다 작지 않은 가장 긴 구간을 찾고자 합니다. 다시 말해서, 아래 식을 만족하는 $i$와 $k$들 중 $k$의 값이 가장 큰 경우를 찾아내면 됩니다.

<div style="text-align: center; font-size: 20px;">
$a_{i} \oplus a_{i+1} \oplus \cdots \oplus a_{i+k-1} \ge x, 1 \le i \le i+k-1 \le N$
</div>

주어지는 데이터에서 이러한 구간이 존재한다는 것은 보장됩니다.

배타적 논리합(XOR, $\oplus$) 연산이란 이진법으로 표현된 수들에 적용되는 연산으로, 각 비트 쌍에 대해 아래 식을 만족합니다.

* $0 \oplus 0 = 0$
* $0 \oplus 1 = 1$
* $1 \oplus 0 = 1$
* $1 \oplus 1 = 0$

이 연산은 교환 법칙이 성립하고 ($a \oplus b = b \oplus a$), 각 원소의 역원이 자기 자신입니다. $(a \oplus (a \oplus b)) = b$입니다.

C/C++에서 `^`로 표현됩니다. (즉 $a \oplus b$ = `a ^ b`)

### 입력 형식

첫 번째 줄에 수열의 길이 $N$ ($1 \le N \le 250,000$)과 $x$ ($0 \le x \le 1,000,000,000$)가 주어집니다.  두 번째 줄에는 $10^9$를 넘지 않는 $N$개의 양의 정수가 공백을 사이로 두고 주어집니다.

### 출력 형식

첫 번째 줄에 $i$와 $k$를 출력합니다. $k$가 최대화되는 경우가 여러 개 있다면 $i$가 가장 작은 경우를 출력하면 됩니다.

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
   <td class="code-font">4 6<br/>
6 1 2 4</td>
   <td class="code-font">2 3</td>
  </tr>
 </tbody>
</table>

### 참고

40%의 데이터에 대해 $N \le 35,000.$
80%의 데이터에 대해 $N \le 100,000.$