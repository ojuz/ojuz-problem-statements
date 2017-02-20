심심한 승현이는 너무 심심한 나머지 올바른 괄호열을 가지고 놀고 있었습니다. 

<div style="font-size: 20px; font-weight: bold; text-align:center;">
(()(()))()()
</div>

그러다가 어쩌다 보니 괄호열을 부러뜨렸습니다. 

<div style="font-size: 20px; font-weight: bold; text-align:center;">
(()&nbsp;&nbsp;&nbsp;&nbsp;((&nbsp;&nbsp;&nbsp;&nbsp;)))()&nbsp;&nbsp;&nbsp;&nbsp;()
</div>

크게 낙담한 승현이는 노력해 보았지만, 대부분이 부러져 버려 단 한 부분만 재사용할 수 있다는 것을 깨닫게 되었습니다.

<div style="font-size: 20px; font-weight: bold; text-align:center;">
)))()
</div>

승현이는 이 괄호열을 가지고 놀려고 했으나 올바른 괄호열이 아니기 때문에 행복하지 않았습니다. 이를 보던 지학이는 승현이에게 “그러면 앞과 뒤에 적절하게 괄호를 붙이면 올바른 괄호열이 되지 않을까?”라고 했고, 승현이는 조금 생각한 뒤 그렇게 하기로 했습니다. 예를 들어, 위의 올바르지 않은 괄호열의 경우 앞에 여는 괄호 3개를 붙이면 올바른 괄호열이 됩니다.

<div style="font-size: 20px; font-weight: bold; text-align:center;">
<span style="color: red">(((</span>)))()
</div>

그러나 괄호열을 사서 붙이는 데에는 돈이 들고 많이 붙일수록 놀기가 불편해지기 때문에, 승현이는 가능한 한 괄호열을 적게 추가하려고 합니다.

승현이가 망가뜨리고 사용 가능한 올바르지 않은 괄호열이 주어질 때, 올바른 괄호열으로 만들기 위해 앞과 뒤에 붙여야 할 괄호의 최소 개수를 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 올바르지 않은 괄호열  $S$가 주어집니다. $S$의 길이는 1 이상 50 이하입니다.

### 출력 형식

첫 번째 줄에 $S$를 올바른 괄호열으로 만들기 위해 앞과 뒤에 붙여야 할 괄호의 최소 개수를 출력합니다. 불가능한 경우는 주어지지 않습니다.

### 참고

괄호열이란 여는 괄호 ‘(’와 닫는 괄호 ‘)’로만 구성된 문자열을 말합니다.

올바른 괄호열은 아래와 같이 정의할 수 있습니다.

* "()"는 올바른 괄호열입니다.
*  A가 올바른 괄호열이라면 "(A)" 역시 올바른 괄호열입니다.
*  A와 B가 모두 올바른 괄호열이라면 "AB" 역시 올바른 괄호열입니다.

### 서브태스크

#### 서브태스크 1 (2점)

답은 2 이하입니다.

#### 서브태스크 2 (2점)

앞에만 괄호를 붙이거나 뒤에만 괄호를 붙이면 됩니다.

#### 서브태스크 3 (12점)

추가 제약 조건이 없습니다.

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
   <td class="code-font">)))()</td>
   <td class="code-font">3</td>
  </tr>
  <tr>
   <td class="code-font">)(()</td>
   <td class="code-font">2</td>
  </tr>
  <tr>
   <td class="code-font">))()((</td>
   <td class="code-font">4</td>
  </tr>
  <tr>
   <td class="code-font">)(()(()))</td>
   <td class="code-font">1</td>
  </tr>
 </tbody>
</table>
