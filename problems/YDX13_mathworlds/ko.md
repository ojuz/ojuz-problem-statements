승현이는 MathWorlds라는 게임에 들어갈 문제들을 만들고 있습니다. MathWorlds에서, 플레이어에게 "$x$ [연산자] $y = z$" 형태의 식이 주어지고, 참가자는 "`+`", "`-`", "`*`", "`/`" 중 이 식을 만족하는 연산자를 하나 골라내야 합니다. 승현이는 여러분에게 무작위로 만들어진 문제들을 검증하는 프로그램을 작성해 달라고 합니다.

여러분에게 세 개의 정수 $x, y, z$가 주어집니다. "$x$ [연산자] $y = z$"를 만족하는 연산자를 출력하세요. 이러한 연산자가 존재하지 않거나 여러 개 있다면, "`Invalid`"를 대신 출력합니다. "`/`"는 **정확한 나눗셈**입니다. (**몫만 취하는 정수 나눗셈이 아닙니다**)

### 입력 형식

세 개의 정수 $x, y, z$ ($0 \le x,y,z \le 10^{9}$)가 공백을 사이로 두고 주어집니다.

### 출력 형식

"`+`", "`-`", "`*`", "`/`", "`Invalid`" 중 하나를 출력합니다.

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
   <td class="code-font">3 2 1</td>
   <td class="code-font">-</td>
  </tr>
  <tr>
   <td class="code-font">2 2 4</td>
   <td class="code-font">Invalid</td>
  </tr>
 </tbody>
</table>