승현이는 트리의 차수 수열에 관심을 가지고 있습니다. 승현이는 길이가 $N$인 수열 $d$를 만들었습니다. 승현이는 $N$개의 정점을 가졌으며 $i$번 정점의 차수 (정점과 인접한 간선의 수)가 $d_{i}$인 트리가 존재하는지 궁금합니다.

이러한 트리가 존재하지 않는다면 "`None`"을 출력하세요. 만약 트리가 동형(isomorphism)을 제외하고 유일하게 결정된다면 (다른 말로, 조건을 만족하는 트리들이 모두 같은 모양이라면) "`Unique`"를 출력하세요. 그렇지 않다면 "`Multiple`"을 출력하세요.

두 트리 $T_{1}$과 $T_{2}$는 아래 조건을 만족할 때 '동형'이라고 부릅니다. 

* $T_{1}$의 정점 집합으로부터 $T_{2}$의 정점 집합으로의 1대1 대응 $f$가 다음 조건을 만족하도록 존재합니다. - $T_{1}$의 두 정점의 쌍 $(u, v)$에 대하여, $T_{1}$에서 정점 $u$와 정점 $v$ 사이에 간선이 존재한다는 것과 $T_{2}$에서 정점 $f(u)$와 $f(v)$ 사이에 간선이 존재한다는 것은 같은 의미입니다. (서로 필요충분조건)

### 입력 형식

첫 번째 줄에 $N$ ($1 \le N \le 100$)이 주어집니다. 두 번째 줄에 $N$개의 정수 $d_{1}, d_{2}, \cdots, d_{N}$ ($! \le d_{i} \le N-1$)이 공백을 사이로 두고 존재합니다.

### 출력 형식

다음 중 하나를 출력합니다: "`None`", "`Unique`" 또는 "`Multiple`"

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
1 1 3 1 3 1</td>
   <td class="code-font">Unique</td>
  </tr>
  <tr>
   <td class="code-font">3<br/>
2 2 2</td>
   <td class="code-font">None</td>
  </tr>
 </tbody>
</table>