0 이상 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup>-1</span> 이하의 모든 정수가 하나씩 있다. 또한 정수들을 담을 수 있는 상자가 <span class="tex-span">2<sup class="upper-index"><i>K</i></sup></span>개 있으며, 각 상자에는 1부터 <span class="tex-span">2<sup class="upper-index"><i>K</i></sup></span>까지의 자연수 번호가 차례대로 붙어 있다. 

나는 가지고 있는 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개의 정수들을 <span class="tex-span">2<sup class="upper-index"><i>K</i></sup></span>개의 상자에 넣으려고 한다. 나는 정수들이 골고루 분배되기를 원하므로, 각 상자에 들어 있는 정수의 개수는 서로 같아야 한다. 따라서 분배 결과 <span class="tex-span">2<sup class="upper-index"><i>K</i></sup></span>개의 상자 각각에는 <span class="tex-span">2<sup class="upper-index"><i>N-K</i></sup></span>개의 서로 다른 정수들이 들어 있게 된다. 그런데 안타깝게도 나는 완벽주의자이기 때문에, 모든 상자에 대해 그 상자 안에 들어 있는 모든 수를 각각 이진수로 나타냈을 때 1의 개수의 합이 서로 같도록 분배해야 한다.

### 입력

첫 번째 줄에 두 개의 자연수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>K</i></span> (<span class="tex-span">1 &le; <i>K</i> &lt; <i>N</i> &le; 16</span>)이 공백을 사이로 두고 주어진다.

### 출력

<span class="tex-span">2<sup class="upper-index"><i>K</i></sup></span>개의 줄을 출력한다. 이 중 <span class="tex-span"><i>i</i></span>(<span class="tex-span">1 &le; <i>i</i> &le; 2<sup class="upper-index"><i>K</i></sup></span>)번째 줄에는 <span class="tex-span"><i>i</i></span>번 상자에 들어 있는 정수 <span class="tex-span">2<sup class="upper-index"><i>N-K</i></sup></span>개를 공백 하나를 사이로 두고 출력한다.

전체 출력에서 같은 수가 여러 번 나오면 안 되고, 각 상자마다 들어 있는 모든 수를 이진수로 나타냈을 때 나타난 1의 개수의 합이 모든 상자에 대해 동일해야 한다.

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>24</td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

이 문제는 부분문제가 없는 것과 같다.

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>2 1</samp></td><td><samp>0 3<br>1 2</samp></td></tr></tbody>
</table>

* 1번 상자: 0 = 0<sub>(2)</sub>, 3 = <u>11</u><sub>(2)</sub> 이므로, 1은 총 2개
* 2번 상자: 1 = <u>1</u><sub>(2)</sub>, 2 = <u>1</u>0<sub>(2)</sub> 이므로, 1은 총 2개

상자에 있는 수들이 중복되지 않고, 각 상자마다 그 안에 들어 있는 수를 이진수로 나타냈을 때 나타나는 1의 개수의 합이 2로 서로 같으므로, 이 분배는 완벽주의자인 나에게도 만족스러운 분배인 것이다.