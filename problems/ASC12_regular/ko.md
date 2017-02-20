세 종류의 알파벳 $\\{A, B, C\\}$로 구성된 길이가 $3n$인 단어를 생각해 봅시다. 단어 $\alpha$에서 $A$가 나타나는 횟수를 $A(\alpha)$, $B$가 나타나는 횟수를 $B(\alpha)$, $C$가 나타나는 횟수를 $C(\alpha)$로 정의해 봅시다.

단어 $\omega$가 아래 조건을 만족할 때 *규칙적*이라고 합니다.

* $A(\omega) = B(\omega) = C(\omega)$
* $\gamma$가 $\omega$의 접두사일 때, $A(\gamma) \ge B(\gamma) \ge C(\gamma)$

예로 들어, $n = 2$일 때 규칙적인 단어는 5개 있습니다. $AABBCC, AABCBC, ABABCC, ABACBC, ABCABC.$

$n$이 주어질 때, 규칙적인 단어가 몇 개나 되는지 구하는 프로그램을 작성하세요.

### 입력 형식

$n$ ($0 \le n \le 60$)이 주어집니다.

### 출력 형식

길이가 $3n$인 규칙적인 단어의 개수를 출력합니다.

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
   <td class="code-font">2</td>
   <td class="code-font">5</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">42</td>
  </tr>	
 </tbody>
</table>