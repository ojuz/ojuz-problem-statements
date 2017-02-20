승현이와 석환이는 산책을 나갔습니다. 그들은 긴 도로의 서쪽 끝에 있는 승현이의 집에서 출발하여 도로의 동쪽 끝에 있는 석환이의 집 근처에서 산책을 끝마쳤습니다. 걷는 동안, 이 두 사람은 자신들이 강을 $n$번 건넜다는 것을 알게 되었습니다.

안타깝게도, 두 사람 모두 강이 어떻게 흐르는지 기억하지 못했습니다. 승현이는 강이 남쪽에서 북쪽으로 흐른다고 주장하지만, 석환이는 북쪽에서 남쪽으로 흐른다고 합니다. 이렇게 시작한 분쟁(?)은 지학이를 만날 때가 되자 큰 싸움이 되었습니다. 지학이는 두 아이들의 이야기를 듣고, 강이 흐를 수 있는 배치 상태의 모든 경우의 수를 세어 보라고 제안했습니다.

하지만 이 문제는 그들이 풀기에 너무 어려워 보입니다. 승현이와 석환이를 도와주세요.

### 입력 형식

첫 번째 줄에 두 사람이 강을 건넌 횟수 $n$ ($1 \le n \le 16$)이 주어집니다.

### 출력 형식

첫 번째 줄에 가능한 모든 강의 배치 형태의 경우의 수를 출력합니다.

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
   <td class="code-font">1</td>
   <td class="code-font">2</td>
  </tr>
  <tr>
   <td class="code-font">2</td>
   <td class="code-font">4</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">4</td>
  </tr>
  <tr>
   <td class="code-font">4</td>
   <td class="code-font">12</td>
  </tr>
 </tbody>
</table>

마지막 예제에서 강이 흐를 수 있는 모든 경우의 수는 아래와 같습니다. 물이 흐르는 방향이 다르면 다른 상태로 간주된다는 것을 명심하세요.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC19_river/rivers.png"/>
</div>