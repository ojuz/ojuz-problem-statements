출처: [http://koistudy.net/?mid=prob_page&NO=963&SEARCH=0](http://koistudy.net/?mid=prob_page&NO=963&SEARCH=0)

도넛을 매우 좋아하는 경곽이는 경희, 경숙이의 2명의 여동생이 있다. 경곽이는 두 여동생을 매우 아끼기로 유명하다.

오늘 간식으로 매우 큰 특이한 도넛이 준비되었다. 경곽이는 도넛을 매우 좋아하므로 되도록이면 많이 먹고자 하지만, 두 동생을 아끼는 마음이 더 커서 두 동생에게 더 많은 도넛을 주고자 한다. 

경곽이는 도넛을 자를 칼을 가지고 있다. 하지만 도넛이 특이해서 지정된 곳이 아닌 다른 곳을 자르면 다 부서져서 먹을 수 없는 상태가 된다.

경곽이는 아래 그림과 같이 도넛에 $n$개 군데 자를 수 있는 위치를 알고 있다. 

<center>
![]([[file:circle2.png]])
</center>

자를 수 있는 위치는 $[1, n]$으로, 이 중 3곳을 잘라야 3등분 할 수 있다.

자를 위치 $i$와 $i+1$ 사이에 위치한 부분의 크기를 $A_i$라 한다. 단 $n$번과 1번 위치 사이의 부분의 크기는 $A_n$이다.

경곽이는 두 동생들 각각에게 자신이 먹는 양 이상 많은 양의 도넛을 주면서 자신이 먹을 수 있는 양을 최대화하고자 한다. 이를 구하는 프로그램을 작성하시오.

### 입력

첫 번째 줄에 자를 수 있는 위치의 수 $n$ 이 주어진다. 두 번째 줄부터 $n$줄에 걸쳐서 각 부분의 크기 $a_i$가 주어진다.

### 출력

경곽이가 먹을 수 있는 최대량을 출력한다.

### 제약 조건

- $3 \le n \le 100\,000$
- $1 \le a_i \le 1\,000\,000\,000$ ($1 \le i \le n$)

### 부분문제

#### 부분문제 1 [5점]

$N \le 100$이다.

#### 부분문제 2 [15점]

$N \le 400$이다.

#### 부분문제 3 [30점]

$N \le 8\,000$이다.

#### 부분문제 4 [5점]

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
   <td class="code-font" style="width: 50%;">6<br>
1<br>
5<br>
4<br>
5<br>
2<br>
4</td>
   <td class="code-font">6</td>
  </tr>
 </tbody>
</table>

위의 그림과 같다. 1, 3, 5의 위치에서 자르면 된다.

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 2</th>
   <th>출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">30<br>
1<br>
34<br>
44<br>
13<br>
30<br>
1<br>
9<br>
3<br>
7<br>
7<br>
20<br>
12<br>
2<br>
44<br>
6<br>
9<br>
44<br>
31<br>
17<br>
20<br>
33<br>
18<br>
48<br>
23<br>
19<br>
31<br>
24<br>
50<br>
43<br>
15</td>
   <td class="code-font">213</td>
  </tr>
 </tbody>
</table>
