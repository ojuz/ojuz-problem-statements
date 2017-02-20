최근 일직선으로 달려가면서 점수가 있는 무언가를 차례대로 먹는 게임이 유행하고 있다. 시류를 남들보다 조금 늦게 따르는 경근이 역시 이런 게임을 개발하였다. 아직 이름은 없다.

이 게임에는 물체를 먹을 때마다 점수에 곱해지는 **<i>곱 계수</i>**라는 것이 있다. 게임을 시작한 처음에 이 값은 0이다. 이 게임의 캐릭터는 아주 먼 왼쪽의 한 지점에서 출발하여 오른쪽으로 달려간다. 경근이는 일직선에 물체 몇 개를 놓아두었기 때문에, 캐릭터는 필연적으로 물체를 만나게 된다. 만약 캐릭터가 그 물체를 먹는다면 캐릭터의 곱 계수가 1 증가한 다음, "(먹은 물체의 점수) &times; (현재 가진 곱 계수)"가 캐릭터가 얻은 점수에 더해진다. 만약 그 물체를 먹지 않는다면 곱 계수가 0으로 초기화되고 점수는 얻을 수 없다. 각 물체를 먹을 때 얻는 점수는 양수임이 보장되지 않기 때문에 높은 점수를 받기 위해서는 적절하게 물체들을 먹을지 말지 정해야 한다. 이를 결정하면 캐릭터는 다시 오른쪽으로 달리게 되며, 다시 왼쪽으로 돌아갈 수는 없다.

경근이가 만들고 있는 맵에서는 <span class="tex-span"><i>N</i></span>개의 물체를 순서대로 먹을 수 있다. 경근이는 이 맵에서 캐릭터가 얻을 수 있는 최대 점수가 몇 점인지 궁금해졌다. 맵에 놓여 있는 물체들의 점수가 차례대로 주어질 때, 캐릭터가 얻을 수 있는 최대 점수를 구하는 프로그램을 작성하라.

만약 실수형 변수를 사용해야 한다면, 그 정확도에 대해 크게 신경 쓰지 않아도 되도록 테스트 데이터가 만들어져 있다.

### 입력

첫 번째 줄에 자연수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1 &le; <i>N</i> &le; 10<sup class="upper-index">6</sup></span>)이 주어진다.

두 번째 줄에는 물체들의 점수를 의미하는 <span class="tex-span"><i>N</i></span>개의 정수가 공백을 사이로 두고 주어진다. 물체들은 맵에 놓여 있는 순서대로 주어지므로, 캐릭터는 주어진 순서대로 물체를 먹을 수 있다. 이 정수들의 절댓값은 <span>10<sup class="upper-index">6</sup></span> 이하이다.

### 출력

주어진 맵에서 캐릭터가 얻을 수 있는 최대 점수를 출력한다.

### 부분 문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>N</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>26</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>44</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">6</sup></span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>3<br>-1 -1 5</samp></td><td><samp>12</samp></td></tr></tbody>
</table>

모든 물체를 먹는 것이 최선이다.

* 세 번째 물체만 먹으면 <span class="tex-span">5&thinsp;&times;&thinsp;1&thinsp;=&thinsp;5</span>점
* 두 번째, 세 번째 물체만 먹으면 <span class="tex-span">(&thinsp;-&thinsp;1)&thinsp;&times;&thinsp;1&thinsp;+&thinsp;5&thinsp;&times;&thinsp;2&thinsp;=&thinsp;9</span>점
* 모든 물체를 먹는다면 <span class="tex-span">(&thinsp;-&thinsp;1)&thinsp;&times;&thinsp;1&thinsp;+&thinsp;(&thinsp;-&thinsp;1)&thinsp;&times;&thinsp;2&thinsp;+&thinsp;5&thinsp;&times;&thinsp;3&thinsp;=&thinsp;12</span>점