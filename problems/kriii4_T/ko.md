길이가 <span class="tex-span"><i>N</i>&thinsp;</span>인 *순열*이란, <span class="tex-span">1</span> 이상 <span class="tex-span"><i>N</i></span> 이하의 자연수 <span class="tex-span"><i>N</i>&thinsp;</span>개로 이루어진, 같은 수가 두 번 이상 등장하지 않는 수열을 의미한다. 길이가 <span class="tex-span"><i>N</i>&thinsp;</span>인 순열의 종류는 총 <span class="tex-span"><i>N</i>!</span>개가 있다.

이 순열에서 <span class="tex-span">K-minsum</span>이라는 것을 정의할 것이다. 순열 <span class="tex-span"><i>A</i>&thinsp;</span>가 있고, 각 원소를 순서대로 나열하면 <span class="tex-span"><i>A</i><sub class="lower-index">1</sub>,&thinsp;<i>A</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>A</i><sub class="lower-index"><i>N</i></sub></span>일 때, 순열 <span class="tex-span"><i>A</i>&thinsp;</span>의 <span class="tex-span">K-minsum</span>은

<p style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_T/63b4ad444fd90aeace3484403e0f67eef0a2a922.png">
</p>

이다. <span class="tex-span">min</span>은 인자로 나열된 수 중의 최솟값을 구하는 함수이다. <span class="tex-span"><i>K</i>&thinsp;</span>가 주어질 때, 길이가 <span class="tex-span"><i>N</i></span>인 모든 <span class="tex-span"><i>N</i>!</span>개의 순열에 대해 <span class="tex-span">K-minsum</span>을 구해 그 합을 출력하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 순열의 길이를 나타내는 자연수 <span class="tex-span"><i>N</i>&thinsp;</span>과 정수 <span class="tex-span"><i>K</i></span>(<span class="tex-span">0&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;<i>N</i></span>)가 주어진다.

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
  <td><center>8</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">3</sup></span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>92</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

길이가 <span class="tex-span"><i>N</i>&thinsp;</span>인 모든 <span class="tex-span"><i>N</i>!</span>개의 순열에 대해 <span class="tex-span">K-minsum</span>을 구해 그 합을 출력한다. 합이 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

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
		<tr><td><samp>1 1</samp></td><td><samp>0</samp></td></tr>
		<tr><td><samp>2 0</samp></td><td><samp>8</samp></td></tr>
		<tr><td><samp>3 1</samp></td><td><samp>22</samp></td></tr>
		<tr><td><samp>5 1</samp></td><td><samp>1908</samp></td></tr>
		<tr><td><samp>8 2</samp></td><td><samp>1435680</samp></td></tr>
		<tr><td><samp>13 3</samp></td><td><samp>880193815</samp></td></tr>
    </tbody>
</table>