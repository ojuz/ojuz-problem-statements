여러분에게 $N$행 $M$열의 격자판이 있다고 합시다. 각 격자는 알파벳 소문자를 포함합니다. 동쪽 또는 남쪽으로만 움직일 수 있을 때, 좌측 상단 격자에서부터 우측 하단 격자까지의 아무 경로나 생각해 봅시다. 이 경로를 지나면서 각 격자에 적힌 알파벳을 읽으면 문자열이 됩니다. 이 문자열을 *경로의 값*이라고 정의합니다. 이제 모든 가능한 경로들을 구한 뒤 사전 순서대로 정렬합니다. 여러분이 할 일은 정렬된 목록에서 $K$번째 경로를 구하는 것입니다.

### 입력 형식

첫 번째 줄에 행의 수 $N$과 열의 수 $M$이 주어집니다. ($1 \le N, M \le 30$) 다음 $N$개 줄에는 정확히 $M$개의 알파벳 소문자가 주어집니다. 마지막 줄에는 정수 $K$가 주어집니다. ($1 \le K \le 10^{18}$) 목록의 길이가 $K$보다 길거나 $K$와 같다는 것은 보장됩니다.

### 출력 형식

답을 출력합니다.

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
   <td class="code-font">3 4<br/>
abcd<br/>
efdg<br/>
hijk<br/>
4</td>
   <td class="code-font">abfdgk</td>
  </tr>
 </tbody>
</table>

목록은 아래와 같습니다.

<div class="code-font">
abcdgk, abcdgk, abcdjk, abfdgk, abfdjk, abfijk, aefdgk, aefdjk, aefijk, aehijk
</div>