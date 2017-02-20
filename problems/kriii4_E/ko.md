그는 그녀와 동전 <span class="tex-span"><i>N</i>&thinsp;</span>개를 가지고 게임을 하려고 한다. 이 게임은 서로 번갈아 가면서 진행하는 게임이며, 그는 그녀에게 첫 차례를 양보했다. 규칙은 다음과 같다.

1.	<span class="tex-span"><i>N</i>&thinsp;</span>개의 동전을 일렬로 늘어놓는다. 각 동전은 앞면 혹은 뒷면이 위로 와 있다.
2.	자신의 차례가 오면, 일렬로 늘어선 동전에서 특정한 연속적인 구간을 하나 선택해야 한다. 단, 선택한 구간에 있는 모든 동전은 앞면이어야 한다. 선택한 구간에 있는 동전은 마음대로 뒤집을 수 있다. 즉, 구간 내의 각 동전을 뒤집을지 뒤집지 않을지 자신이 결정할 수 있다. 그러나 적어도 하나의 동전은 뒤집어야 한다. 동전을 적절히 뒤집고 나면 상대에게 차례를 넘겨준다.
3.	자신의 차례에 선택할 수 있는 구간이 없는 사람이 패배한다. 즉 모든 동전이 뒷면인 상태로 자신의 차례가 오면 패배한다.

동전의 앞면이 위로 와 있으면 <samp>H</samp>, 뒷면이 위로 와 있으면 <samp>T</samp>라고 하자. 그리고 동전이 일렬로 <samp>HHHTHH</samp>의 순서로 늘어서 있다고 하자. 자신의 차례가 온 사람은 구간을 선택해야 하는데, 뒷면인 네 번째 동전이 들어가 있는 구간은 선택할 수 없다. 또한 선택하는 구간이 크면 클수록 더욱 자유롭게 뒤집을 수 있으므로, 첫 번째 동전에서 세 번째 동전까지를 선택하거나, 다섯 번째 동전에서 여섯 번째 동전까지를 선택하는 것이 의미가 있는 구간 선택이 된다. 만약 첫 세 개의 동전을 선택했다면, 세 동전을 뒤집는 경우의 수 <span class="tex-span">2<sup class="upper-index">3</sup> = 8</span>가지에서 아무것도 뒤집지 않는 경우를 제외한 <span class="tex-span">7</span>가지의 방법 중 하나로 동전을 뒤집어 차례를 넘길 수 있다.

그와 그녀는 이 게임을 계속할 것인데, 둘 다 지겨운 것을 싫어하기 때문에 게임이 시작할 때마다 처음 동전의 나열을 무작위로 선택하려고 한다. 즉 가능한 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개의 배열을 모두 동일한 확률로 하여 하나 선택하는 것이다.

이 게임은 동전을 한 번 뒷면으로 뒤집으면 앞면으로 다시 뒤집을 방법이 없고, 자기 차례에 무조건 하나 이상의 동전을 뒤집어야 하기 때문에, 두 사람이 최선을 다한다면 승패가 무조건 결정되는 게임이다. 두 사람이 최선을 다한다고 할 때, <b>그</b>가 이길 수 있는 처음 동전 나열의 개수는 몇 가지일까?

<br>

### 입력

첫 번째 줄에는 동전의 수를 나타내는 자연수 <span class="tex-span"><i>N</i>&thinsp;</span>이 주어진다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-4 col-md-4 col-lg-4">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>5</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;15</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>95</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;250</span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

그가 이길 수 있는 처음 동전 나열의 개수를 출력하라. 이 수는 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

<br>

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예제</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예제</th>
		</tr>
	</thead>
	<tbody>
		<tr><td><samp>1</samp></td><td><samp>1</samp></td></tr>
		<tr><td><samp>2</samp></td><td><samp>1</samp></td></tr>
		<tr><td><samp>3</samp></td><td><samp>2</samp></td></tr>
		<tr><td><samp>4</samp></td><td><samp>4</samp></td></tr>
		<tr><td><samp>5</samp></td><td><samp>8</samp></td></tr>
    </tbody>
</table>
