JOI 마을에 있는 넓은 황무지에는 $N$명의 신성한 허수아비가 서 있어, 주민들은 일 년에 몇 번씩 허수아비를 둘러싸고 축제를 하고 있었습니다. JOI 마을의 촌장은 "허수아비들의 말씀을 들었다"고 주장하며 황무지에 밭을 하나 만들 계획을 세웠습니다. 허수아비들의 말에 따르면 밭은 다음 조건을 충족해야 한다고 합니다.

* 각 변이 동서 방향 또는 남북 방향으로 놓인 직사각형이어야 합니다.
* 남서쪽의 꼭짓점과 북동쪽의 꼭짓점에는 허수아비가 서 있어야 합니다.
* 경계를 제외한 밭의 내부에는 허수아비가 서 있으면 안 됩니다.

물론, 신성한 허수아비들을 옮기는 것은 허용되지 않습니다. 허수아비들의 말씀에 따라 세울 수 있는 밭으로 가능한 직사각형은 몇 개나 있을까요?

### 해야 할 일

허수아비들의 위치가 주어질 때, 허수아비들의 말씀에 따라 만들 수 있는 밭의 위치가 몇 개나 되는지 찾는 프로그램을 작성하세요.

### 입력 형식

표준 입력에서 아래 입력을 받습니다.

* 첫 번째 줄에 허수아비들의 수 $N$이 주어집니다.
* $N$개 줄이 주어집니다. 이 중 $i$($1 \le i \le N$)번째 줄에는 두 개의 정수 $X_{i}$와 $Y_{i}$가 주어집니다. JOI 마을의 황무지는 2차원 데카르트 평면 위에 표시되며, $x$축이 증가하는 방향이 동쪽 방향, $y$축이 증가하는 방향이 북쪽 방향입니다. $i$번째 허수아비는 좌표 $(X_{i}, Y_{i})$에 서 있습니다.

### 출력 형식

첫 번째 줄에 허수아비들의 말씀에 따라 만들 수 있는 밭의 위치가 몇 개나 되는지 출력합니다.

### 제한

모든 입력은 아래 조건을 만족합니다.

* $1 \le N \le 200,000$
* $0 \le X_{i} \le 1,000,000,000$ ($1 \le i \le N$)
* $0 \le Y_{i} \le 1,000,000,000$ ($1 \le i \le N$)
* $X_{i}$ ($1 \le i \le N$)는 서로 다릅니다.
* $Y_{i}$ ($1 \le i \le N$)는 서로 다릅니다.

### 서브태스크

#### 서브태스크 1 [5점]

* $N \le 400$

#### 서브태스크 2 [10점]

* $N \le 5,000$

#### 서브태스크 3 [85점]

추가 제약 조건이 없습니다.

### 입출력 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 예제 1</th>
   <th>출력 예제 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4<br>
0 0<br>
2 2<br>
3 4<br>
4 3</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>

이 예제에서 허수아비들의 말씀에 따라 밭이 될 수 있는 직사각형들은 아래 3개가 있습니다.

* 점 $(0, 0)$을 남서쪽의 꼭짓점으로, 점 $(2, 2)$를 북동쪽의 꼭짓점으로 하는 직사각형
* 점 $(2, 2)$을 남서쪽의 꼭짓점으로, 점 $(3, 4)$를 북동쪽의 꼭짓점으로 하는 직사각형
* 점 $(2, 2)$을 남서쪽의 꼭짓점으로, 점 $(4, 3)$를 북동쪽의 꼭짓점으로 하는 직사각형

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI14_scarecrows/scarecrow1.png">
</div>


<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 예제 2</th>
   <th>출력 예제 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">10<br>
2 1<br>
3 0<br>
6 3<br>
10 2<br>
16 4<br>
0 8<br>
8 12<br>
11 14<br>
14 11<br>
18 10</td>
   <td class="code-font">15</td>
  </tr>
 </tbody>
</table>

이 예제를 그림으로 나타내면 아래와 같습니다.
<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI14_scarecrows/scarecrow2.png">
</div>