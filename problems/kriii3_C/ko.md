경근이는 요즘 여러 능력을 가지고 몬스터들과 싸우는 웹게임을 열심히 하고 있다. 경근이는 지금 <span class="tex-span"><i>N</i></span>개의 공격 능력을 가지고 있다. 경근이는 능력들을 편하게 관리하고자 각 능력에 1 이상 <span class="tex-span"><i>N</i></span> 이하의 자연수 번호를 붙였다. 

<span class="tex-span"><i>i</i></span>번 능력에는 그 능력이 발동될 확률 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>와 상대에게 입히는 피해량 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>가 책정되어 있다. 따라서 경근이가 <span class="tex-span"><i>i</i></span>번 능력에 발동 명령을 내리면, <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>의 확률로 능력이 발동되어 상대에게 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>만큼의 피해를 입히고, <span class="tex-span">(1&thinsp;-&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>)</span>의 확률로 능력이 발동되지 않아 아무 일도 일어나지 않는다.

열심히 게임을 한 결과, 경근이는 드디어 게임 내에서 모든 능력을 자유롭게 장착하고 해제할 수 있게 되었다! 이제 경근이는 상대가 입을 피해량의 기댓값이 최대가 되도록 하기 위해 어떤 능력들을 장착해야 할지를 알고 싶다. 경근이가 어떤 능력(들)을 장착한 채로 상대방을 공격할 기회를 얻었다면, 아래 과정이 일어난다:

- 하나의 능력만 장착했을 때: 해당 능력에 발동 명령을 내린 후, 그 결과와 상관 없이 공격 기회를 잃는다.
- 두 개 이상의 능력을 장착했을 때: 가지고 있는 모든 능력들 중 하나를 임의로 고른다. 모든 능력을 고를 확률은 서로 같다. 고른 능력에 발동 명령을 내린다. 만약 이 능력이 발동되었다면, 공격 기회를 잃고 과정이 끝난다. 하지만 이 능력이 발동되지 않았다면, 아직 발동 명령을 내려 보지 않은 능력들 중 하나를 동일한 확률로 무작위하게 고른 후, 다시 발동 명령을 내린다. 만약 능력이 발동되었다면 공격 기회를 잃은 후 과정을 끝내고, 발동되지 않았다면 같은 과정을 더 이상 발동 명령을 내려 보지 않은 능력이 없을 때까지 반복한다. 모든 능력에 발동 명령을 내렸음에도 발동된 능력이 하나도 없으면 공격 기회를 잃는다.

현재 경근이가 가지고 있는 <span class="tex-span"><i>N</i></span>개의 능력이 발동될 확률과 상대에게 입히는 피해량이 주어질 때, 한 번의 공격 기회에서 피해량의 기댓값이 최대가 되도록 하기 위해 장착해야 할 능력의 집합을 구하는 프로그램을 작성하라.

### 입력

첫 번째 줄에 자연수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;20</span>)이 주어진다. 다음 <span class="tex-span"><i>N</i></span>개의 줄에는 능력들의 정보가 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 <span class="tex-span"><i>i</i></span>번 능력이 발동될 확률과 상대에게 입히는 피해량을 의미하는 두 정수 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>&thinsp;,&thinsp;<i>d</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;100</span>)이 공백을 사이로 두고 주어진다. 이는 <span class="tex-span"><i>i</i></span>번 능력은 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>% (<span class="tex-span">&thinsp;=&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>&thinsp;/&thinsp;100</span>)의 확률로 발동하는 능력이며 상대에게 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>만큼의 피해를 입힌다는 의미이다.

### 출력

가지고 있는 능력들을 적절히 장착하여 얻을 수 있는 피해량의 기댓값의 최댓값을 출력한다. 정답과의 절대/상대 오차가 <span class="tex-span">10<sup class="upper-index">&thinsp;-&thinsp;8</sup></span> 이하이면 올바른 답안으로 처리된다.

### 부분문제

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
  <td>25</td>
  <td><span class="tex-span">&le; 7</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>37</td>
  <td><span class="tex-span">&le; 20</span></td>
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
	
	<tr><td><samp>2<br>100 1<br>10 20</samp></td><td><samp>2.000000000000</samp></td></tr><tr><td><samp>3<br>12 10<br>11 11<br>10 12</samp></td><td><samp>3.227420000000</samp></td></tr></tbody>
</table>

첫 번째 예제의 경우 1번 능력은 100% 발동하지만 피해량이 너무 낮아 이를 사용하지 않고 2번 능력만 사용하는 것이 피해량의 기댓값이 더 높다.