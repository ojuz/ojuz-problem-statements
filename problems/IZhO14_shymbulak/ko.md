부자인 석환이는 넓은 땅을 사들여 리조트를 건설하고, 그 안에 $N$개의 관광지를 만들었습니다. 이들 관광지는 길이가 모두 같은 $N$개의 도로들로 연결되어 있습니다. 도로들은 양방향 통행이 가능하며, 어떤 두 관광지 사이도 도로를 통해 이동할 수 있도록 지어졌습니다. 하지만 가끔 이동하기 위해 너무 많은 시간이 들었습니다. 석환이는 이동 시간을 줄이기 위해 도로를 짓로 했습니다. 그 전에, 가장 멀리 떨어진 두 관광지의 쌍들 사이의 최단 경로가 몇 개나 되는지 알고자 합니다.

"두 관광지가 가장 멀리 떨어졌다"는 것은 두 관광지 사이의 최단 경로의 길이가 다른 모든 관광지 쌍 사이의 최단 경로의 길이보다 길거나 같다는 것입니다. 즉 가장 멀리 떨어진 관광지 쌍이 여러 개 있을 수도 있습니다.

### 입력 형식

첫 번째 줄에 $N$ ($3 \le N \le 200000$)이 주어집니다. 다음 $N$개 줄에는 각 도로가 잇는 두 도시의 번호가 주어집니다. 도로의 번호는 $1$부터 $N$까지의 자연수입니다. 중복된 도로가 없다는 것이 보장됩니다.

### 출력 형식

가장 멀리 떨어진 두 관광지들의 쌍들 사이의 최단 경로가 몇 개나 되는지 알고자 합니다.

### 채점

각 테스트 케이스마다 점수가 주어집니다.

* 30%의 테스트 케이스에 대해 $N \le 500.$
* 50%의 테스트 케이스에 대해 $N \le 5000.$

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
1 2<br/>
1 3<br/>
2 4<br/>
4 3<br/>
4 5<br/>
4 6</td>
   <td class="code-font">4</td>
  </tr>
  <tr>
   <td class="code-font">4<br/>
1 2<br/>
1 3<br/>
1 4<br/>
4 3</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>

### 참고

첫 번째 예제에서 가장 멀리 떨어진 두 관광지의 쌍들은 $(1, 5), (1, 6)$이며, 최단 경로들은

* $1 \rightarrow 2 \rightarrow 4 \rightarrow 5.$
* $1 \rightarrow 3 \rightarrow 4 \rightarrow 5.$
* $1 \rightarrow 2 \rightarrow 4 \rightarrow 6.$
* $1 \rightarrow 3 \rightarrow 4 \rightarrow 6.$

입니다.