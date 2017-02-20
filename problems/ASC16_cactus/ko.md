*선인장 그래프*는 무방향 연결 그래프로서 모든 정점이 많아야 하나의 사이클에 속해 있어야 합니다.

트리에 0개 이상의 간선을 추가하면 선인장 그래프를 만들 수 있습니다. 트리를 선인장 그래프로 만드는 경우는 여러 가지가 있을 수 있습니다.

예로 들어 아래 왼쪽에 있는 트리에 간선을 추가해서 선인장 그래프로 만들 수 있는 경우의 수는 12가지입니다. 이 12가지의 선인장 그래프는 오른쪽에 있습니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC16_cactus/cactuses.png"/>
</div>

트리가 주어질 때, 0개 이상의 간선을 추가해서 선인장 그래프를 만들 수 있는 경우의 수를 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 노드의 수 $n$ ($1 \le n \le 200$)이 주어집니다. 다음 $n-1$개 줄에 트리의 간선이 잇는 두 정점의 번호가 주어집니다. 트리의 각 정점은 $1$부터 $n$까지의 자연수 번호가 붙어 있습니다.

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
   <td class="code-font">6<br/>
1 3<br/>
2 3<br/>
3 4<br/>
4 5<br/>
4 6</td>
   <td class="code-font">12</td>
  </tr>
 </tbody>
</table>