*출처: [http://koistudy.net/?mid=prob_page&NO=964&SEARCH=0](http://koistudy.net/?mid=prob_page&NO=964&SEARCH=0)*

날다람쥐란 나무에서 나무로 점프하여 글라이더 처럼 날아서 이동하는 특이한 다람쥐이다.

GSHS의 날다람쥐 서식처에는 $n$개의 나무가 있으며 각 나무는 번호가 1부터 $n$까지 부여되어 있으며, $i$번째 나무의 높이는 각각 $h_i$이다.

날다람쥐는 나무를 오르거나 내릴 수 있고, 나무의 임의의 위치에서 점프하여 날아갈 수 있다.

날다람쥐가 나무를 $x$미터 오르거나 내리는데 $x$초가 걸린다. (정수 단위로만 이동 가능하다.)

날다람쥐가 한 나무에서 다른 나무로 날아가는데 걸리는 시간 $t$가 주어지며, 날다람쥐가 날아가는 $t$초 동안 $t$미터만큼 고도가 떨어진다.(정수 거리로만 날아갈 수 있다.)

즉 날다람쥐가 어떤 나무의 $h$ 높이에서 $t$미터 떨어진 나무로 날아간다면, 그 나무의 $h-t$미터의 위치에 도착한다. (단, 날아가는 동안 고도가 $0$이 되면, 이동 불가능한 것으로 본다.)

각 $n$개의 나무의 높이와, 각 나무에서 나무로 날아서 이동가능한 나무의 쌍 $m$개와 날아가는데 걸리는 시간 $t$가 주어진다.

다람쥐는 처음에 나무 1의 $x$ 위치에 있으며, 최종적으로 자기의 집이 있는 나무 $n$의 꼭대기로 가고자 한다.

주어진 정보를 이용하여 날다람쥐가 목적지까지 가는데 디는 최소시간을 구하는 프로그램을 작성하시오.

### 입력

첫 번째 줄에 나무의 수 $n$과, 이동 가능한 경로의 수 $m$, 처음 다람쥐가 나무 1에 위치한 높이 $x$가 공백으로 구분되어 입력된다.

두 번째 줄부터 $n$줄에 걸쳐서 각 나무의 높이가 주어진다.

다음 줄부터 $m$줄에 걸쳐서 이동 가능한 나무 $a, b$와 두 나무 간의 비행시간 $t$가 공백으로 구분되어 입력된다.

### 출력

조건을 만족하는 최소 시간을 출력한다. 만약 도달 불가능하다면 `-1`을 출력한다.

### 제약 조건

* $2 \le N \le 100\,000$
* $1 \le M \le 300\,000$
* $1 \le H_i \le 1\,000\,000\,000$ ($1 \le i\le N$)
* $1 \le T_j \le 1\,000\,000\,000$ ($1 \le j\le M$)
* $0 \le X \le H_1$

### 부분문제

#### 부분문제 1 [25점]

* $N \le 1\,000$
* $M \le 3\,000$
* $H_i \le 100$ ($1 \le i \le N$)
* $T_j \le 100$ ($1 \le j \le M$)

#### 부분문제 2 [25점]

* $X = 0$

#### 부분문제 3 [50점]

추가 제약 조건이 없다.

### 예제

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 1</th>
   <th>출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">5 5 0<br>
50<br>
100<br>
25<br>
30<br>
10<br>
1 2 10<br>
2 5 50<br>
2 4 20<br>
4 3 1<br>
5 4 20</td>
   <td class="code-font">110</td>
  </tr>
 </tbody>
</table>

예로, 아래와 같이 이동하면 된다.

1. 나무 1을 50미터 올라간다.
2. 나무 1에서 나무 2로 날아간다.
3. 나무 2에서 나무 4로 날아간다.
4. 나무 4에서 나무 5로 날아간다.
5. 나무 5를 10미터 올라간다.

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 2</th>
   <th>출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">2 1 0<br>
1<br>
1<br>
1 2 100</td>
   <td class="code-font">-1</td>
  </tr>
 </tbody>
</table>

나무 1에서 나무 2로 날아갈 수 없다.

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 3</th>
   <th>출력 3</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">4 3 30<br>
50<br>
10<br>
20<br>
50<br>
1 2 10<br>
2 3 10<br>
3 4 10</td>
   <td class="code-font">100</td>
  </tr>
 </tbody>
</table>
