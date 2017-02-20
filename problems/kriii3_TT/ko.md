많이 자란 정민이는 부모님이 시키는 유명한 학습지 씽크스몰을 해야 한다. 정민이가 이번에 배워야 하는 부분은 다항식의 곱셈이다. 하지만 정민이는 게임을 해야만 하기에, 여러분에게 점수를 줄 테니 다항식 <span class="tex-span"><i>f</i>(<i>x</i>)</span>와 다항식 <span class="tex-span"><i>g</i>(<i>x</i>)</span>를 곱해주는 프로그램을 작성해 달라고 한다.

### 입력

첫 번째 줄에 다항식 <span class="tex-span"><i>f</i>(<i>x</i>)</span>의 차수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;1,000,000</span>)과 다항식 <span class="tex-span"><i>g</i>(<i>x</i>)</span>의 차수 <span class="tex-span"><i>M</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;1,000,000</span>)이 공백을 사이로 두고 주어진다.

두 번째 줄에는 다항식 <span class="tex-span"><i>f</i>(<i>x</i>)</span>의 계수를 나타내는 <span class="tex-span"><i>N</i>&thinsp;+&thinsp;1</span>개의 자연수 <span class="tex-span"><i>a</i><sub class="lower-index">0</sub>,&thinsp;<i>a</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>a</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub>,&thinsp;<i>a</i><sub class="lower-index"><i>N</i></sub></span>이 주어진다. <span class="tex-span"><i>f</i>(<i>x</i>)&thinsp;=&thinsp;<i>a</i><sub class="lower-index">0</sub>&thinsp;+&thinsp;<i>a</i><sub class="lower-index">1</sub>&middot;<i>x</i>&thinsp;+&thinsp;<i>a</i><sub class="lower-index">2</sub>&middot;<i>x</i><sup class="upper-index">2</sup>&thinsp;+&thinsp;<i>a</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub>&thinsp;&times;&thinsp;<i>x</i><sup class="upper-index"><i>N</i>&thinsp;-&thinsp;1</sup>&thinsp;+&thinsp;<i>a</i><sub class="lower-index"><i>N</i></sub>&thinsp;*&thinsp;<i>x</i><sup class="upper-index"><i>N</i></sup></span>이다.

세 번째 줄에는 다항식 <span class="tex-span"><i>g</i>(<i>x</i>)</span>의 계수를 나타내는 <span class="tex-span"><i>M</i>&thinsp;+&thinsp;1</span>개의 자연수 <span class="tex-span"><i>b</i><sub class="lower-index">0</sub>,&thinsp;<i>b</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>b</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub>,&thinsp;<i>b</i><sub class="lower-index"><i>M</i></sub></span>이 주어진다. <span class="tex-span"><i>g</i>(<i>x</i>)&thinsp;=&thinsp;<i>b</i><sub class="lower-index">0</sub>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">1</sub>&middot;<i>x</i>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">2</sub>&middot;<i>x</i><sup class="upper-index">2</sup>&thinsp;+&thinsp;<i>b</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub>&thinsp;&times;&thinsp;<i>x</i><sup class="upper-index"><i>M</i>&thinsp;-&thinsp;1</sup>&thinsp;+&thinsp;<i>b</i><sub class="lower-index"><i>M</i></sub>&thinsp;*&thinsp;<i>x</i><sup class="upper-index"><i>M</i></sup></span>이다.

### 출력

<span class="tex-span"><i>f</i>(<i>x</i>)&thinsp;&times;&thinsp;<i>g</i>(<i>x</i>)&thinsp;=&thinsp;<i>c</i><sub class="lower-index">0</sub>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">1</sub>&middot;<i>x</i>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">2</sub>&middot;<i>x</i><sup class="upper-index">2</sup>&thinsp;+&thinsp;...&thinsp;+&thinsp;<i>c</i><sub class="lower-index"><i>L</i></sub>&thinsp;*&thinsp;<i>x</i><sup class="upper-index"><i>L</i></sup></span>라고 하자. 

첫 번째 줄에 <span class="tex-span"><i>c</i><sub class="lower-index">0</sub>,&thinsp;<i>c</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>c</i><sub class="lower-index"><i>L</i></sub></span>의 값을 모두 [xor](https://ko.wikipedia.org/wiki/%EB%B0%B0%ED%83%80%EC%A0%81_%EB%85%BC%EB%A6%AC%ED%95%A9)한 값, 즉 <img align="middle" class="tex-formula" src="http://espresso.codeforces.com/ba2b4b21190538b043dcb08f496f9b90b1538187.png"/>을 출력한다. C/C++에서는 <samp>c[0] <b>^</b> c[1] <b>^</b> ... <b>^</b> c[L-1] ^ c[L]</samp>의 값을 구하면 된다.

xor 연산을 시행하는 이유는, <span class="tex-span"><i>c</i><sub class="lower-index"><i>i</i></sub></span>를 출력하기에는 그 양이 너무 많기 때문이며, 문제의 풀이에는 영향을 주지 않는다.

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-2 col-md-2 col-lg-2">점수</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span></th>
  <th class="col-sm-4 col-md-4 col-lg-4"><span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>10</td>
  <td><span class="tex-span">&le; 1,000</span></td>
  <td><span class="tex-span">&le; 100</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>10</td>
  <td><span class="tex-span">&le; 100,000</span></td>
  <td><span class="tex-span">&le; 100</span></td>
 </tr>
 <tr>
  <td>3</td>
  <td>10</td>
  <td><span class="tex-span">&le; 1,000,000</span></td>
  <td><span class="tex-span">&le; 1,000,000</span></td>
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
	
	<tr><td><samp>1 1<br/>1 2<br/>3 2</samp></td><td><samp>15</samp></td></tr></tbody>
</table>

<span class="tex-span"><i>f</i>(<i>x</i>)&thinsp;=&thinsp;1&thinsp;+&thinsp;2<i>x</i></span>, <span class="tex-span"><i>g</i>(<i>x</i>)&thinsp;=&thinsp;3&thinsp;+&thinsp;2<i>x</i></span>, <span class="tex-span"><i>f</i>(<i>x</i>)&thinsp;&times;&thinsp;<i>g</i>(<i>x</i>)&thinsp;=&thinsp;3&thinsp;+&thinsp;8<i>x</i>&thinsp;+&thinsp;4<i>x</i><sup class="upper-index">2</sup></span>