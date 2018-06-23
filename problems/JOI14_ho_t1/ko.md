일본정보올림피아드 위원회에서는, 대만대회에 가는 선수를 응원하기 위해 새로운 JOI깃발을 만들기로 했다.
JOI깃발은 정사각형이 세로로 $M$행, 가로로 $N$열이 있으며, 각 사각형에는 `J`, `O`, `I`중 하나의 문자가 하나씩 적혀있다.

<center>
![]([[file:img1.png]])
<p>JOI깃발의 예</p>
</center>

일본정보올림피아드 위원회는 JOI깃발과는 별개로 JOI문장이라는 것을 정하고 있다. JOI문장은, 정사각형이 세로로 2행, 가로로 2열 늘여져 있고, 각 사각형에는 `J`, `O`, `I`중 하나의 문자가 하나씩 적혀 있다.

<center>
![]([[file:img2.png]])

JOI문장의 예
</center>

JOI깃발에 포함된 JOI문장의 갯수는 JOI깃발에 포함 된, 세로 2행 가로 2열의 영역 중 영역의 `J`, `O`, `I` 배치가 JOI문장과 (회전이나 대칭 없이) 일치하는 것의 갯수이다. 조건을 만족하는 세로 2행과 가로 2열이 겹쳐 있어도, 각각을 따로 센다.

일본 정보올림피아드 위원회는 이전 JOI깃발과 1장의 백지를 가지고 있다. 백지 JOI깃발을 구성하는 것은 정사각형 1개 모양의 크기로, `J`, `O`, `I` 중 원하는 문자를 쓸 수 있다. 일본 정보올림피아드 위원회는 다음 중 하나의 작업을 하여서 새로운 JOI 깃발을 만들기로 했다.

- 이전 JOI 깃발에 아무것도 하지 않고, 그대로 새로운 JOI깃발을 만든다. 백지는 사용하지 않는다.
- 백지에 문자 하나를 쓰고, 이전 JOI 깃발 중 하나의 정사각형에 겹쳐 붙여서 오래 된 JOI 깃발의 정사각형 중 한 개를 변경한다. 변경 후의 JOI깃발이 새로운 JOI깃발이다.

일본 정보올림피아드 위원회는 새로운 JOI깃발에 포함된 JOI문장의 수를 최대로 하고 싶어 한다. 당신은 새로운 JOI깃발에 포함된 JOI문장의 갯수의 최댓값을 구해야 한다.

이전 JOI 깃발과 JOI문장에 대한 정보가 주어졌을 때, 새로운 JOI깃발에 포함된 JOI 문장의 갯수의 최댓값을 구하는 프로그램을 작성하여라.

### 입력

표준 입력으로 다음의 데이터가 들어온다.
- 첫째 줄에는 2개의 정수 $M$, $N$이 공백으로 구분되어 들어온다. 이것은 JOI 깃발이 세로로 $M$행, 가로로 $N$열 늘어져 있다는 것을 의미한다.
- 다음 $M$개의 각 줄에는 각각 N개의 문자로 된 문자열이 들어온다. 각 문자는 `J`, `O`, `I` 중 하나이고 $M$개의 행의 $i$번째 행에 쓰여있는 문자열의 $j$문자 째는 이전 JOI깃발의 위에서 $i$번째, 아래서 $j$번째 정사각형에 쓰여 있는 문자를 의미한다.
- 다음 2개의 각 줄에는 각각 2개의 문자로 된 문자열이 들어온다. 각 문자는 `J`, `O`, `I` 중 하나이고 2개의 행의 $i$번째 행에 쓰여있는 문자열의 $j$문자 째는 이전 JOI문장의 위에서 $i$번째, 아래서 $j$번째 정사각형에 쓰여 있는 문자를 의미한다.

### 출력

표준출력으로, 새로운 JOI깃발에 있는 JOI문장의 갯수의 최댓값을 출력하여라.

### 제한

모든 입력은 다음 조건을 만족한다.

- $2 \le M \le 1\,000$
- $2 \le N \le 1\,000$

#### Subtask 1 [30점]

이하의 추가 조건을 만족한다.

- $M \le 50$
- $N \le 50$

#### Subtask 2 [70점]

추가 제한조건은 없다.

#### 예제

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 1</th>
   <th>출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">3 5<br>
JOIJO<br>
IJOOO<br>
IIJIJ<br>
JO<br>
IJ</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>

이전 JOI깃발과 JOI문장은 문제중의 예와 같다. 위에서 2번째, 왼쪽에서 4번째의 정사각형을 백지를 사용해서 J로 변경한다. 그 후 다음 모양이 된다.

<center>
![]([[file:img3.png]])

JOI깃발에서 한 부분을 변경한 예
</center>

이렇게 변경한 후에는 JOI 깃발에는 다음 세 곳에 JOI문장과 같은 배치가 있다.
<center>
![]([[file:img4.png]])
</center>

JOI 문장과 같은 배열의 위치가 4개 이상이 되게 하는 새로운 JOI 깃발은 존재하지 않기 때문에, 새로운 JOI 깃발에 있는 JOI 문장의 최댓값은 3이다.


<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 2</th>
   <th>출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">2 6<br>
JOJOJO<br>
OJOJOJ<br>
OJ<br>
JO</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>

백지를 쓰지 않아도 최댓값이 나오는 경우가 있음에 주의하여라.

<table class="table table-bordered table-condensed">
 <thead>
  <tr>
   <th>입력 3</th>
   <th>출력 3</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font" style="width: 50%;">2 2<br>
JI<br>
IJ<br>
JJ<br>
JJ</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>

이 입출력 예제에서는, 모든 가능한 새로운 JOI 깃발에서, JOI 문장이 하나도 존재하지 않는다.