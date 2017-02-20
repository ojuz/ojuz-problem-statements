<span class="tex-span"><i>xy</i></span>평면의 원점에 로봇이 서 있다. 로봇은 <span class="tex-span"><i>x</i></span>축 양의 방향을 바라보고 있으며, 지금부터 <span class="tex-span"><i>N</i>&thinsp;</span>번 움직이려고 한다. 로봇이 한 번 움직이는 과정은 다음과 같다.

1. 먼저 로봇은 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_F/f70202effb3e2373050ee3ed97cc9f878eaf1b79.png">의 확률로 자신이 바라보는 방향의 왼쪽으로 90도 돌고, <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_F/d7b56bb8f55a7f3503d4154358a4e88e3f3f9b72.png">의 확률로 방향을 바꾸지 않으며, <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_F/8688eb9a61db0f2213bc444f0549da44e03c5d37.png">의 확률로 자신이 바라보는 방향의 오른쪽으로 90도 돈다. 
 - 예를 들어, 처음 상태에서는 로봇이 왼쪽으로 90도 돌면 <span class="tex-span"><i>y</i></span>축 양의 방향을 바라보게 되고, 오른쪽으로 90도 돌면 <span class="tex-span"><i>y</i></span>축 음의 방향을 바라보게 된다. 
2. 1번 과정이 끝나고 나서, 로봇은 자신이 바라보고 있는 방향으로 <span class="tex-span">1</span>의 거리를 움직인다. 

로봇이 <span class="tex-span"><i>N</i></span>번 움직인 결과 좌표 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>에 위치해 있다면, 로봇이 원점으로부터 떨어져 있는 정도는 <span class="tex-span"><i>x</i><sup class="upper-index">2</sup>&thinsp;+&thinsp;<i>y</i><sup class="upper-index">2</sup></span>로 나타난다. 로봇이 <span class="tex-span"><i>N</i>&thinsp;</span>번 움직인 다음 원점으로부터 떨어져 있는 정도의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 로봇이 움직일 횟수, 왼쪽으로 방향을 바꿀 확률, 가만히 있을 확률, 오른쪽으로 방향을 바꿀 확률을 결정하는 네 정수 <span class="tex-span"><i>N</i>, <i>L</i>, <i>M</i>, <i>R</i></span>이 공백으로 구분되어 주어진다. <span class="tex-span"><i>L</i>, <i>M</i>, <i>R</i></span> 중 적어도 하나는 양의 정수이다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-8">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
  <th class="col-sm-4 col-md-4 col-lg-4"><center><span class="tex-span"><i>L</i>, <i>M</i>, <i>R</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>4</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;15</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>L</i>, <i>M</i>, <i>R</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>96</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>L</i>, <i>M</i>, <i>R</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

로봇이 <span class="tex-span"><i>N</i>&thinsp;</span>번 이동한 다음 원점으로부터 떨어져 있는 정도의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>5 1 0 1</samp></td><td><samp>5</samp></td></tr>
		<tr><td><samp>10 5 0 7</samp></td><td><samp>308301433</samp></td></tr>
		<tr><td><samp>15 249 123 953</samp></td><td><samp>644460144</samp></td></tr>
		<tr><td><samp>100 4 5 6</samp></td><td><samp>648224530</samp></td></tr>
    </tbody>
</table>

