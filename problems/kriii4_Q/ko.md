시간이 많은 그는 <span class="tex-span"><i>N</i></span>개의 비트(<samp>0</samp> 또는 <samp>1</samp>을 가질 수 있는 변수)를 조작하는 일을 반복하고 있다. 지금까지 하던 것이 식상해진 그는 새로운 규칙으로 <span class="tex-span"><i>N</i></span>개의 비트를 조작하려고 한다. 한 번의 조작이란 다음과 같은 작업을 의미한다.

1. 비트 중에서 <samp>0</samp>인 것들을 먼저, <samp>1</samp>인 것들을 나중에 놓는 방식으로 일렬로 늘어 놓는다. 즉 오름차순(엄밀히 비내림차순) 정렬한다.
2. 그 다음 <span class="tex-span">1</span> 이상 <span class="tex-span"><i>N</i></span> 이하의 정수 <span class="tex-span"><i>K</i></span>개(<span class="tex-span"><i>K</i></span>는 홀수)를 무작위로 뽑는다. 각 정수를 뽑을 확률은 모두 독립적으로, 같은 정수가 두 번 이상 뽑힐 수도 있으며, <span class="tex-span">1</span>부터 <span class="tex-span"><i>N</i>&thinsp;</span>까지의 각 자연수가 뽑힐 확률은 모두 동일하다.
3. 뽑힌 <span class="tex-span"><i>K</i>&thinsp;</span>개의 정수 각각에 대해서 정수가 <span class="tex-span"><i>i</i>&thinsp;</span>라면 <span class="tex-span"><i>i</i>&thinsp;</span>번째 비트를 토글한다. 즉, <samp>0</samp>이면 <samp>1</samp>로, <samp>1</samp>이면 <samp>0</samp>으로 바꾼다.

예를 들어, 그가 가진 비트가 <samp>0,1,0</samp>이고 <span class="tex-span"><i>K</i> = 3</span>이라고 해보자.

1. 먼저 비트를 정렬하여 <samp>0,0,1</samp>로 만든다.
2. <span class="tex-span"><i>K</i> = 3</span>개의 정수를 뽑아 <span class="tex-span">1,3,1</span>순서대로 뽑혔다고 해보자.
3. 첫 번째 정수 <span class="tex-span">1</span>에 의해서 비트는 <samp>1,0,1</samp>이 된다. 두 번째 정수 <span class="tex-span">3</span>에 의해서 비트는 <samp>1,0,0</samp>이 된다. 세 번째 정수 <span class="tex-span">1</span>에 의해서 비트는 <samp>0,0,0</samp>이 된다.

위의 과정에서 알 수 있듯, 사실 비트의 순서가 어떻게 되어있는지는 크게 중요한 것이 아니고 개수가 중요하다. 그는 조작을 한 후에 모든 비트가 <samp>1</samp>이 되면 조작을 끝내고 자러 갈 것이다. 현재 비트 중에서 <samp>0</samp>인 것의 개수가 <span class="tex-span"><i>z</i></span>개일 때 모든 비트를 <samp>1</samp>로 만들기 위한 조작 횟수의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 비트의 개수와 뽑게 되는 정수의 개수를 의미하는 두 자연수 <span class="tex-span"><i>N</i>, <i>K</i></span>가 공백으로 구분되어 주어진다. <span class="tex-span"><i>K</i></span>는 홀수이다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-6 col-md-6 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>K</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>9</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span></center></td>
  <td><center><span class="tex-span"><i>K</i> = 1</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>91</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
<span class="tex-span"><i>N</i></span>개의 줄에 걸쳐 답을 출력한다. <span class="tex-span"><i>z</i></span>번째 줄에는 현재 비트 중에서 <samp>0</samp>인 것의 개수가 <span class="tex-span"><i>z</i></span>개일 때 모든 비트를 <samp>1</samp>로 만들기 위해 필요한 조작 횟수의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 답이 존재하는 것이 확인된 입력만 들어온다.

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
		<tr><td><samp>1 1</samp></td><td><samp>1</samp></td></tr>
		<tr><td><samp>2 1</samp></td><td><samp>3<br>4<br></samp></td></tr>
		<tr><td><samp>5 99</samp></td><td><samp>812420891<br>724220653<br>692773316<br>452277443<br>513756160</samp></td></tr>
    </tbody>
</table>
