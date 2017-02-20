트리란 그래프의 일종으로 어떤 두 정점을 잇는 경로가 정확히 하나만 있는 방향성 없는 그래프를 뜻한다. 다른 말로 하자면, 모든 정점이 연결되어 있으며 사이클이 없는 그래프이다.

<span class="tex-span"><i>N</i>&thinsp;</span>개의 구별할 수 있는 정점을 가진 트리를 만들 수 있는 경우의 수를 생각해보자. 정점에 <span class="tex-span">1&thinsp;</span>에서 <span class="tex-span"><i>N</i>&thinsp;</span>까지의 번호를 붙이면, 간선이 어떤 두 정점을 연결하는지에 따라 경우를 구분할 수 있게 된다. 예를 들어 <span class="tex-span"><i>N</i>=4&thinsp;</span>인 경우 다음과 같이 <span class="tex-span">16&thinsp;</span>가지의 트리가 있을 수 있다.

<center>  	 	 
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii4/X1.png" style="border: none;"/>  	 	 
</center>

<span class="tex-span"><i>N</i>&thinsp;</span>개의 구별할 수 있는 정점을 가진 트리 중에서 특정한 <span class="tex-span"><i>M</i>&thinsp;</span>개의 간선을 포함하는 트리의 개수를 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 트리의 정점 개수와 포함해야 하는 간선의 개수를 나타내는 두 정수 <span class="tex-span"><i>N</i>,&thinsp;<i>M</i></span>이 공백으로 구분되어 주어진다.
다음 <span class="tex-span"><i>M</i>&thinsp;</span>개의 줄에는 포함해야 하는 간선의 양 끝점 <span class="tex-span"><i>a</i>,&thinsp;<i>b</i>&thinsp;(1&thinsp;&leq;&thinsp;<i>a</i>,&thinsp;<i>b</i>&thinsp;&leq;&thinsp;<i>N</i>&thinsp;)</span>이 주어진다. <span class="tex-span"><i>a</i></span>와 <span class="tex-span"><i>b</i></span>는 다른 수이며 같은 간선이 여러 번 주어지는 일은 없다. 주어진 간선을 모두 포함하는 트리를 만들지 못할 수도 있다.

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
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>M</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>9</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;8</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;8</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>91</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;10<sup class="upper-index">5</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
주어진 간선을 모두 포함하는 트리의 개수를 출력한다. 이 수는 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

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
		<tr><td><samp>4 0</samp></td><td><samp>16</samp></td></tr>
		<tr><td><samp>4 1<br>1 2</samp></td><td><samp>8</samp></td></tr>
    </tbody>
</table>

<center>  	 	 
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii4/X2.png" style="border: none;"/>  	 	 
</center>

위 그림에서 <span class="tex-span">1</span>과 <span class="tex-span">2</span>를 연결하는 간선을 빨간 색으로 칠하였다. 이런 간선을 포함하는 트리는 <span class="tex-span">8</span>개 밖에 없음을 알 수 있다.