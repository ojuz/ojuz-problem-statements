물리학자들은 $x$, $y$, $z$ 3가지 종류의 입자를 다루고 있습니다. 그들은 충돌형 가속기 안에 $n$개의 입자를 넣었습니다. 실험 중에 $i$번째 위치에 있던 입자가 사라져서 $j$번째 위치에 갑자기 나타납니다. 입자가 사라지는 순간 그 입자 오른쪽에 있던 모든 입자들의 번호는 1씩 감소하고, 입자가 다시 나타나면 그 입자 오른쪽에 있던 모든 입자들의 번호는 1씩 증가합니다. 이러한 상황에서 과학자들은 $k$번째 위치에 어떤 종류의 입자가 있는지 알고자 합니다. 그들을 도와줄 수 있는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 입자의 수 $n$과 이동과 질의의 수 $m$이 주어집니다. ($1 \le n \le 1 000 000, 1 \le m \le 15 000$)

두 번째 줄에 $x, y, z$로 구성된 길이 $n$의 문자열이 주어집니다. 다음 $m$개 줄에는 입자의 이동이나 과학자들의 질의가 주어집니다. 입자가 이동할 시, 이 줄에는 문자 `a`와 공백이 주어진 뒤 $[1, n]$ 구간 안에 있는 두 개의 정수가 주어집니다. 첫 번째 정수는 사라지는 입자의 위치이고, 두 번째 정수는 입자가 다시 나타날 위치입니다. 과학자들이 질의를 할 시, 이 줄에는 문자 `q`와 공백이 주어진 뒤 $[1, n]$ 구간 안에서 과학자들이 입자의 종류를 알고자 하는 위치가 주어집니다.

### 출력 형식

각 질의마다 그 답을 출력합니다.

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
   <td class="code-font">15 6<br/>
xzxyyzxxzxyyzyx<br/>
a 2 10<br/>
a 15 4<br/>
q 3<br/>
a 12 2<br/>
q 14<br/>
q 2</td>
   <td class="code-font">y<br/>
z<br/>
y</td>
  </tr>
 </tbody>
</table>

<div class="code-font" style="font-size: 15px;">
x<u>z</u>xyyzxxzxyyzyx -> xxyyzxxzx<b>z</b>yyzy<u>x</u> -> xxy<b>x</b>yzxxzxz<u>y</u>yzy -> x<b>y</b>xyxyzxxzxzyzy
</div>