좌표평면 위에 <span class="tex-span"><i>N</i></span>개의 서로 색이 다른 색종이를 하나씩 하나씩 붙인다. 색종이는 반드시 좌표평면과 이미 붙어 있는 모든 색종이들의 위에 놓여야 하며, 색종이를 좌표평면 아래에 붙이거나 붙어 있는 색종이 사이에 넣는 것은 불가능하다. 

색종이의 모양에는 두 가지 종류가 있는데, 아래와 같다.

1. <span class="tex-span">(<i>x</i><sub class="lower-index">1</sub>,&thinsp;<i>y</i><sub class="lower-index">1</sub>)</span>, <span class="tex-span">(<i>x</i><sub class="lower-index">2</sub>,&thinsp;<i>y</i><sub class="lower-index">2</sub>)</span>, <span class="tex-span">(<i>x</i><sub class="lower-index">3</sub>,&thinsp;<i>y</i><sub class="lower-index">3</sub>)</span>을 세 꼭지점으로 하는 삼각형 모양 
2. 점 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>가 중심이고 반지름의 길이가 <span class="tex-span"><i>r</i></span>인 원 모양

색종이에 1번부터 <span class="tex-span"><i>N</i></span>번까지의 자연수 번호를 붙인 후, 번호가 작은 순서대로 차례대로 (1번, 2번, .., <span class="tex-span"><i>N</i></span>번) 색종이를 붙인다. 아래 그림은 색종이를 붙이는 과정의 예시를 나타낸다.

<center>
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii3/imgS.png"/>
</center>

1번부터 <span class="tex-span"><i>i</i></span>번까지의 모든 색종이를 붙인 시점에서, 붙어 있는 색종이들이 각각 얼마나 보이는지를 구하여 출력하는 프로그램을 작성하라.

### 입력

첫 번째 줄에 자연수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1 &le; <i>N</i> &le; 200</span>)이 주어진다.

이후 색종이들의 정보를 나타내는 <span class="tex-span"><i>N</i></span>개의 줄이 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1 &le; <i>i</i> &le; <i>N</i></span>)번째 줄에는 맨 처음 <span class="tex-span"><i>i</i></span>번 색종이의 종류를 나타내는 정수 <span class="tex-span"><i>t</i></span> (<span class="tex-span">1 &le; <i>t</i> &le; 2</span>)가 주어진다. <span class="tex-span"><i>t</i> = 1</span>이면 <span class="tex-span"><i>i</i></span>번 색종이의 모양이 삼각형이라는 것으로, 이후 같은 줄에 삼각형의 세 꼭짓점의 좌표를 나타내는 6개의 정수 <span class="tex-span"><i>x</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">3</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">3</sub></span>(<span class="tex-span">-100 &le; </span><span class="tex-span"><i>x</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">3</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">3</sub></span><span class="tex-span"> &le; 100</span>)이 공백을 사이로 두고 주어진다. 세 점이 일직선상에 놓여있는 경우는 없다. <span class="tex-span"><i>t</i> = 2</span>이면 <span class="tex-span"><i>i</i></span>번 색종이의 모양이 원이라는 것으로, 이후 같은 줄에 원의 중심의 좌표를 나타내는 두 정수 <span class="tex-span"><i>x</i></span>, <span class="tex-span"><i>y</i></span>(<span class="tex-span">-100 &le; </span><span class="tex-span"><i>x</i></span>, <span class="tex-span"><i>y</i></span><span class="tex-span"> &le; 100</span>)와 이 원의 반지름을 나타내는 정수 <span class="tex-span"><i>r</i></span>(<span class="tex-span">1 &le; </span><span class="tex-span"><i>r</i></span><span class="tex-span"> &le; 100</span>)이 공백을 사이로 두고 주어진다.


### 출력 형식

<span class="tex-span"><i>N</i></span>개의 줄에 걸쳐 정답을 출력한다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1 &le; <i>i</i> &le; <i>N</i></span>)번째 줄에는, 1번부터 <span class="tex-span"><i>i</i></span>번까지의 모든 색종이를 순서대로 올렸을 때, 1번 색종이의 보이는 면적, 2번 색종이의 보이는 면적, ..., <span class="tex-span"><i>i</i></span>번 색종이의 보이는 면적을 나타내는 <span class="tex-span"><i>i</i></span>개의 실수를 공백을 사이로 두고 차례대로 출력하면 된다. 

정답과의 절대 오차 또는 상대 오차가 <span class="tex-span">10<sup>-8</sup></span> 이하이면 올바른 답안으로 인정된다.


### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>t</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>36</td>
  <td><span class="tex-span">= 2</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>73</td>
  <td><span class="tex-span">&le; 2</span></td>
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
	
	<tr><td><samp>2<br>2 0 0 1<br>1 0 0 2 0 0 2</samp></td><td><samp>3.141592653590<br>2.356194490192 2.000000000000</samp></td></tr></tbody>
</table>