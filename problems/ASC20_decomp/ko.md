문자열 $\alpha$와 정수 $n$에 대해서 $\alpha$를 $n$번 붙여 쓴 것을 $\alpha^{n}$로 둡시다. 예로 들어서 $aab^{4}=aabaabaabaab$입니다.

모든 문자열 $S$는 $S = S_{1}^{d_{1}}S_{2}^{d_{2}}\cdots S_{k}^{d_{k}}$로 분해될 수 있습니다. 이러한 표현 방식은 여러 개가 있을 수도 있습니다. 이 때 분해하는 데 드는 비용은 $|S_{1}| + |S_{2}| + \cdots + |S_{k}|$가 됩니다. ($|Z|$는 문자열 $Z$의 길이입니다.)

문자열 $S$가 주어질 때 비용을 최소화하도록 분해해 보세요.

### 입력 형식

첫 번째 줄에 문자열 $S$가 주어집니다. $S$는 알파벳 대문자로만 구성되어 있으며 길이가 5000을 넘지 않습니다.

### 출력 형식

첫 번째 줄에 최소화한 비용 $w$를 출력합니다. 이 때 분해된 원소들의 개수를 $k$로 둡시다. 다음 $k$개 줄에는 $S_{i}$와 $d_{i}$를 공백을 사이로 두고 출력해야 합니다. 여러 가지 답안이 존재한다면, 아무거나 출력하면 됩니다.

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
   <td class="code-font">ABABAAABABA</td>
   <td class="code-font">5<br/>
AB 2<br/>
A 3<br/>
BA 2</td>
  </tr>
 </tbody>
</table>