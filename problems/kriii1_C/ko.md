선인장이란 양방향 그래프의 일종인데, 모든 정점에 대해 자기 자신으로 돌아오는 경로(사이클)가 하나 이하인 그래프이다. 주어진 그래프가 선인장일까? 아닐까?

### 입력 형식

첫 번째 줄에 그래프의 정점의 개수와 간선의 개수를 나타내는 두 정수 $N, M$ $(1 \le N, M \le 100,000)$ 이 공백으로 구분되어 주어진다.

다음 $M$개의 줄에는 간선이 연결하고 있는 두 정점을 나타내는 두 정수 $x, y$ $(1  \le x, y \le N, x \neq y)$가 공백으로 구분되어 주어진다. 주어진 간선은 중복되지 않으며, 모든 임의의 두 정점에 대해 경로가 존재한다.

### 출력 형식

주어진 그래프가 선인장이면 "**`Cactus`**" 를 아니라면 "**`Not cactus`**" 를 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4 4<br/>
1 2<br/>
2 3<br/>
3 1<br/>
3 4</td>
   <td class="code-font">Cactus</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">5 6<br/>
1 2<br/>
2 3<br/>
3 1<br/>
3 4<br/>
4 5<br/>
5 3</td>
   <td class="code-font">Not cactus</td>
  </tr>
 </tbody>
</table>