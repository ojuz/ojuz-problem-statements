육각형 모양의 타일로 이루어진 벌집 모양의 판이 있다. 타일에는 빨강색, 녹색, 파란색 중 하나의 색을 칠할 수 있는데, 변이 인접한 타일끼리는 같은 색을 칠할 수 없다. 우리는 앞의 조건을 만족하는 판들 중 아래의 판을 사용하도록 하겠다.

<p><center><img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii1_H/pic1.png?dl=1" alt="판" style="width: 400px;" /></center></p>

이 판의 어느 **파란** 타일의 정 중앙에 **오른쪽**을 바라보는 로봇이 올려져 있다. 로봇에게는 세가지 명령이 있는데, `LEFT`, `RIGHT`, `MOVE` 이다. 각 명령을 자세히 정의하기 위해 칸의 중앙에 위치한 로봇이 보고 있는 방향을 숫자로 나타내보자. (처음에 로봇은 오른쪽 방향인 **0**을 바라보고 있는 것이다.)

<p><center><img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii1_H/pic2.png?dl=1" alt="방향" style="width: 150px;" /></center></p>

그리고 이제 로봇의 세가지 동작을 정의하면 아래와 같다.

* `LEFT` : 현재 로봇이 바라보는 방향이 $x$라면 `LEFT` 동작이 수행되고 난 후에는 바라보는 방향이 $x - 1$이 된다. $x$가 $0$이었던 경우 방향은 $5$가 된다.
* `RIGHT` : 현재 로봇이 바라보는 방향이 $x$라면 `RIGHT` 동작이 수행되고 난 후에는 바라보는 방향이 $x + 1$이 된다. $x$가 $5$였던 경우 방향은 $0$이 된다.
* `MOVE` : 현재 바라보고 있는 방향으로 변을 한 번 넘어 다른 타일의 정중앙으로 간다. 로봇이 바라보고 있는 방향은 그대로 유지된다.

로봇이 어떤 동작을 할지는 아직 정해져 있지 않지만, `LEFT` 동작을 $L$번, `RIGHT` 동작을 $R$번, `MOVE` 동작을 $M$번 할 것임은 정해져 있다. 그러므로 로봇은 총

<div style="text-align: center; font-size: 22px; margin-bottom: 10px;">$\frac{(L + R + M)!}{L! R! M!}$</div>

가지의 서로 순서가 다른 동작을 수행할 수 있는 것이다. $L, R, M$이 주어질 때 로봇이 각 색깔의 타일에 멈출 경우의 수를 구하는 프로그램을 작성하라.

### 입력 형식

로봇이 `LEFT` 동작을 할 횟수 $L$, `RIGHT` 동작을 할 횟수 $R$, `MOVE` 동작을 할 횟수 $M$이 공백으로 구분되어 주어진다. $(0 \le L, R, M \le 2,000)$

### 출력 형식

세 줄에 걸쳐서 출력을 한다. 첫 번째 줄에는 로봇이 멈춘 타일의 색이 빨강색일 경우 의 수, 두 번째 줄에는 로봇이 멈춘 타일의 색이 초록색일 경우의 수, 세 번째 줄에는 로 봇이 멈춘 타일의 색이 파란색일 경우의 수를 출력한다. 답이 매우 커질 수 있으므로 답을 $1,000,000,007$로 나눈 나머지를 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">1 1 2</td>
   <td class="code-font">2<br/>6<br/>4</td>
  </tr>
 </tbody>
</table>