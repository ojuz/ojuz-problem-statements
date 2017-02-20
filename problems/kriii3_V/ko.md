피보나치 수열 <span class="tex-span"><i>f</i><sub class="lower-index"><i>n</i></sub></span>은 다음과 같이 정의되는 수열이다.

<center>
<img src="https://attach.oj.uz/contest/kriii3/0b42cedd159778b6e255554c72343444.png" class="thumbnail" style="border: none;"/>
</center>

피보나미얼 <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span"><i>n</i>&thinsp;&ge;&thinsp;1</span>)은 <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub>&thinsp;=&thinsp;<i>f</i><sub class="lower-index">1</sub>&thinsp;&times;&thinsp;<i>f</i><sub class="lower-index">2</sub>&thinsp;&times;&thinsp;...&thinsp;&times;&thinsp;<i>f</i><sub class="lower-index"><i>n</i></sub></span>으로 정의된다. 즉 <span class="tex-span"><i>f</i><sub class="lower-index">1</sub>,&thinsp;<i>f</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>f</i><sub class="lower-index"><i>n</i></sub></span>를 모두 곱한 값이다.

어떤 자연수 <span class="tex-span"><i>k</i></span>에 대해, <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub></span>을 <span class="tex-span"><i>k</i></span>로 몇 번을 나누어야 <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub></span>이 더 이상 <span class="tex-span"><i>k</i></span>로 나누어 떨어지지 않는지를 구하는 프로그램을 작성하라.

### 입력

첫 번째 줄에 두 자연수 <span class="tex-span"><i>n</i></span>과 <span class="tex-span"><i>p</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>n</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span>, <span class="tex-span">2&thinsp;&le;&thinsp;<i>p</i>&thinsp;&le;&thinsp;10<sup class="upper-index">3</sup></span>)이 공백을 사이로 두고 주어진다.

### 출력

<span class="tex-span"><i>p</i>&thinsp;-&thinsp;1</span>줄에 걸쳐 답을 출력한다. 이 중 <span class="tex-span"><i>i</i></span>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>p</i>&thinsp;-&thinsp;1</span>)번째 줄에는 <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub></span>이 <span class="tex-span">(<i>i</i>&thinsp;+&thinsp;1)</span>로 나누어 떨어지지 않도록 하기 위해 <span class="tex-span"><i>F</i><sub class="lower-index"><i>n</i></sub></span>을 <span class="tex-span">(<i>i</i>&thinsp;+&thinsp;1)</span>로 나눠야 할 횟수를 출력해야 한다.

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>n</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>32</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>42</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
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
	
	<tr><td><samp>12 6</samp></td><td><samp>9<br>4<br>4<br>2<br>4</samp></td></tr></tbody>
</table>

<span class="tex-span"><i>F</i><sub class="lower-index"><i>12</i></sub> = 1,570,247,078,400 = 2<sup class="upper-index">9</sup>&times;3<sup class="upper-index">4</sup>&times;5<sup class="upper-index">2</sup>&times;...</span>