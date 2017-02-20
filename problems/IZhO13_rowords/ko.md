승현이는 세상의 종말이 찾아오자 마침내 두 문자열의 최장 공통 부분 수열 (Longest Common Subsequence)에 대해서 배웠습니다. 이제 그는 두 원형 문자열의 최장 공통 부분 수열을 찾고자 합니다.

원형 문자열에서, 이 문자열을 어느 위치, 어느 방향으로 읽든 차이가 없습니다. 예로 들어, 원형 문자열 "algorithm"은 "rithmalgo", "oglamhtir" 등으로 읽힐 수 있습니다.

자주 쓰이는 단어인 "algorithm"과 "grammar"의 최장 공통 부분 수열의 길이는 3 ("grm")이고, 원형 문자열이라면 최장 공통 부분 수열의 길이는 4("grma")입니다.

똑똑한 승현이는 단순한 방법으로는 두 원형 문자열의 최장 공통 부분 수열의 길이를 찾을 수 없다는 것을 깨달았다고 합니다. 궁금해하는 승현이를 위해 정답을 찾아주는 프로그램을 작성해주세요.

### 입력 형식

입력은 두 줄로 이루어지며, 각 줄에 하나의 원형 문자열이 주어집니다. 이 문자열은 1글자 이상 2000글자 이하입니다.

### 출력 형식

첫 번째 줄에 주어진 두 원형 문자열의 최장 공통 부분 수열의 길이를 출력합니다.

### 입출력 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">algorithm<br/>
grammar</td>
   <td class="code-font">4</td>
  </tr>
 </tbody>
</table>