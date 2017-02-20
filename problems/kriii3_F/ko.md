님(Nim) 게임이란 두 사람이 하는 게임의 일종으로, 물건(예를 들어 구슬)이 들어가 있는 여러 개의 주머니로 하는 게임이다. 게임을 하는 두 사람은 서로 번갈아 가면서 주머니들 속에 구슬이 몇 개씩 있는지 잘 살펴 본 후 적절한 전략을 정해 속에 있는 구슬을 꺼낸다. 자신의 차례가 되어 구슬을 꺼내야 할 때, 구슬 몇 개를 꺼내도 상관은 없지만 무조건 하나 이상의 구슬을 꺼내야 하고, 여러 개의 주머니에서 구슬을 꺼내면 안 된다. 한번 구슬을 꺼내면 다음 사람의 차례가 된다. 자기 차례에 꺼낼 구슬이 없는 사람이 패배한다.

명우는 승용이와 님 게임을 하기로 했다. 하지만 둘은 님 게임을 너무 잘 알고 있고, 이 게임에 필승 전략이 있다는 사실도 알고 있다. 이기고 싶은 명우는 특별한 행동을 하는 로봇 심판을 사용하기로 했다. 이 로봇 심판이 하는 일은 이전 사람이 조건에 맞게 구슬을 가져갔는지 확인하는 것과 명우나 승용이가 구슬을 뽑기 전에 모든 주머니에 대해 몇 가지 조건을 검사하는 것이다. 각 주머니 마다 먼저 <span class="tex-span"><i>N</i></span>개의 자연수 <span class="tex-span"><i>p</i><sub class="lower-index">1</sub>,&thinsp;<i>p</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>p</i><sub class="lower-index"><i>N</i></sub></span>에 대해서 주머니 속에 있는 구슬의 총 개수가 어떤 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>) 중 하나로라도 나누어 떨어진다면 주머니 전체를 폐기해 버린다. 그리고 <span class="tex-span"><i>M</i></span>개의 자연수 <span class="tex-span"><i>q</i><sub class="lower-index">1</sub>,&thinsp;<i>q</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>q</i><sub class="lower-index"><i>M</i></sub></span>에 대해서 주머니 속에 있는 구슬의 총 개수가 어떤 <span class="tex-span"><i>q</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>M</i></span>)로도 나누어 떨어지지 않는다면 주머니 전체를 폐기해 버린다. 폐기된 주머니에서는 더 이상 구슬을 꺼낼 수 없다.

명우는 이럴 때에도 필승 전략이 있다는 사실을 알아냈고, 이를 이용해 승용이와의 게임에서 승리하고자 한다. 그러나 자신이 너무 치사하다고 생각해서인지 승용이가 처음으로 구슬을 가져가도록 차례를 양보하고 로봇 심판이 어떤 일을 하는지 알려주었다. 게임이 내일로 다가왔고 승용이는 이 게임의 필승 전략을 찾아내고 싶다. 하지만 그런 일을 하기에는 자신의 시간이 너무 아까웠기 때문에 여러분에게 도움을 요청했다. 처음 주머니들 속에 담겨있는 구슬의 개수가 주어질 때 필승 전략을 찾아서 승용이를 도와주자.

### 입력 형식

첫 번째 줄에 세 정수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span>, <span class="tex-span"><i>K</i></span>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>,&thinsp;<i>M</i>,&thinsp;<i>N</i>&thinsp;+&thinsp;<i>M</i>&thinsp;&le;&thinsp;16</span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;20</span>)이 공백으로 구분되어 주어진다. <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>M</i></span>은 주머니를 검사하는 조건의 개수를 의미하며, <span class="tex-span"><i>K</i></span>는 처음 주머니의 개수를 의미한다. 

두 번째 줄에는 <span class="tex-span"><i>p</i><sub class="lower-index">1</sub></span>에서 <span class="tex-span"><i>p</i><sub class="lower-index"><i>N</i></sub></span>까지의 자연수가 공백으로 구분되어 주어진다. 이 자연수들은 모두 1 이상 <span class="tex-span">10<sup class="upper-index">6</sup></span> 이하이다.

세 번째 줄에는 <span class="tex-span"><i>q</i><sub class="lower-index">1</sub></span>에서 <span class="tex-span"><i>q</i><sub class="lower-index"><i>M</i></sub></span>까지의 자연수가 공백으로 구분되어 주어진다. 이 자연수들은 모두 1 이상 <span class="tex-span">10<sup class="upper-index">6</sup></span> 이하이다. 

네 번째 줄에는 주머니에 담겨 있는 구슬의 개수를 의미하는 <span class="tex-span"><i>K</i></span>개의 정수가 공백으로 구분되어 주어진다. 이 정수들은 1 이상 <span class="tex-span">10<sup class="upper-index">12</sup></span>이하이다.

### 출력 형식

<span class="tex-span"><i>K</i></span>개의 줄에 걸쳐서 승용이가 첫 번째 차례에서 입력에서 <span class="tex-span"><i>i</i></span>번째로 입력 받은 주머니에서 구슬을 꺼낼 때 필승 전략에 대한 정보를 출력한다.

명우와 승용이가 서로 이기기 위해 최선을 다한다고 가정할 때 승용이가 이기기 위해 꺼낼 수 있는 구슬 개수의 경우의 수와 그 중에서 가장 구슬을 적게 꺼낼 때의 구슬 개수를 공백으로 구분하여 출력하면 된다. 만약 이 주머니에서 구슬을 꺼내서 이기는 것이 불가능 하거나 승용이가 꺼내기 전에 로봇이 주머니를 폐기해 버린다면 0을 공백으로 구분하여 두 개 출력하면 된다.

### 부분 문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5">주머니 속 구슬의 총 개수</th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>28</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">6</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>51</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">12</sup></span></td>
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
	
	<tr><td><samp>2 1 2<br>2 3<br>1<br>1 5</samp></td><td><samp>0 0<br>1 4</samp></td></tr></tbody>
</table>