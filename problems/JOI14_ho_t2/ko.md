출처: [http://koistudy.net/?mid=prob_page&NO=980&SEARCH=0](http://koistudy.net/?mid=prob_page&NO=980&SEARCH=0)

GSHS는 음식을 만드는 회사이다. 이번에 GSHS사에서는 매우 특별한 맛을 내는 만두를 만들어서 판매하기로 했다. GSHS사에서 $M$개의 종류의 만두를 1개씩 만들었다. 만들어진 $M$개의 만두는 모두 같은 크기지만, 맛이 모두 다르므로, 가격은 서로 다를 수 있다. $i$번째 만두의 가격은 $P_i$원이다. 

그런데 경곽이가 GSHS사에서 만든 만두를 담을 수 있는 상자를 만들고 있다. 경곽이가 만드는 상자는 모두 $N$개로, $j$번째 상자는 최대 $C_j$개의 만두를 담을 수 있는 크기이며 상자의 가격은 $E_j$원이다. 이들 $N$개의 상자들 중 몇 개($0$ 이상 $N$ 이하)를 GSHS사에서 만두를 판매하기 위하여 샀으며, GSHS사는 만두를 그 상자들 속에 넣어서 세트로 판매하도록 하고 있다. 

각 만두 세트의 가격은 상자에 담긴 각 만두 가격의 합이다. 세트로 제작한 모든 제품을 판다고 가정할 경우, GSHS사가 얻는 이득의 최댓값은 얼마나 될까? 여기서 이익이란 판매한 만두 세트의 가격의 합계로부터 경곽이에게 구입한 상자의 가격을 뺀 값을 의미한다. 또한, 상자에 넣지 않아 세트화 되지 않고 남은 만두는 GSHS사의 직원들이 맛있게 먹기 때문에 손해로 보지는 않는다.

### 문제

각 만두 가격과 각 상자의 크기와 가격이 주어졌을 때, GSHS사가 얻을 수 있는 이익의 최댓값을 구하는 프로그램을 작성하라.

### 입력

입력은 표준 입력으로 주어진다.

- 첫 번째 줄에 만두의 수 $M$과 상자의 수 $N$이 공백으로 구분되어 입력된다. 
- 두 번째 줄부터 $M$줄에 걸쳐서 각 만두의 가격 $P_i$가 입력된다.
- 그 다음 줄부터 $N$줄에 걸쳐서 상자의 크기 $C_i$와 각 상자의 가격 $E_i$가 공백으로 구분되어 입력된다.

### 출력

표준 출력에, GSHS사가 얻을 수 있는 이익의 최댓값을 출력한다.

### 제약 조건

* $1 \le M \le 10\,000$
* $1 \le N \le 500$
* $1 \le P_i \le 10\,000$ ($1 \le i \le M$)
* $1 \le C_j \le 10\,000$ ($1 \le j \le N$)
* $1 \le E_j \le 10\,000$ ($1 \le j \le N$)

### 부분문제

#### 부분 문제 1 (25점)

$N \le 10$이다.

#### 부분 문제 2 (35점)

$C_j \le 10$ ($1 \le j \le N$)이다.

#### 부분 문제 3 (40점)

추가 제약 조건이 없다.

### 입력 예제

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">4 3<br>
180<br>
160<br>
170<br>
190<br>
2 100<br>
3 120<br>
4 250</td>
   <td class="code-font">480</td>
  </tr>
 </tbody>
</table>

상자 1, 2을 구입하고, 1번 상자에 만두 2개, 2번 상자에 만두 2개를 넣으면, 총 판매 금액은 700원이고 상자의 가격이 220원이므로 총 이득은 700-220 = 480원이며 이보다 더 많은 이득을 볼 수 있는 경우는 없다.

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">2 2<br>
1000<br>
2000<br>
1 6666<br>
1 7777</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>

이 경우에는 상자를 안 사고 만두를 하나도 안파는 것이 가장 이득이다. 상자를 사서 이득을 볼 수 있는 경우가 없기 때문이다. 

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">10 4<br>
200<br>
250<br>
300<br>
300<br>
350<br>
400<br>
500<br>
300<br>
250<br>
200<br>
3 1400<br>
2 500<br>
2 600<br>
1 900</td>
   <td class="code-font">450</td>
  </tr>
 </tbody>
</table>
