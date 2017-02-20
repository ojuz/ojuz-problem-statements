길이가 <span class="tex-span"><i>L</i></span>인 선분 형태의 통로가 있다. 경근이는 통로를 원활하게 관리하기 위해, 도로에 좌표를 도입했다. 도로의 왼쪽 끝점의 좌표는 0이고, 도로의 오른쪽 끝점의 좌표는 <span class="tex-span"><i>L</i></span>이며, 도로를 <span class="tex-span"><i>x</i>&thinsp;:&thinsp;<i>y</i></span>로 내분하는 점의 좌표는 <img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/d5fb48f42fbd26561ed06e8ab99ce1ca899450b5.png"/>이다.

이제 경근이는 심심할 때마다 개미를 통로 위에 한 마리씩 올릴 것이다. 경근이의 통로는 매우 신비로워서, 어떤 개미라도 경근이의 통로 위에 올라가기만 하면 반드시 오른쪽이나 왼쪽 방향으로 1초에 1의 거리를 움직인다. 통로의 폭은 최대 한 마리의 개미만이 움직일 수 있을 정도로 매우 좁아서, 서로 반대방향으로 움직이는 개미들이 어느 한 위치에서 부딪치면 그 즉시 두 개미 모두 방향을 반대로 바꾸어 원래의 속력을 유지하며 움직인다. 개미가 통로의 양 끝점에 도달할 때에도 그 즉시 방향을 반대로 바꾸어 원래의 속력을 유지하며 움직인다. 개미의 크기는 매우 작아서 점으로 취급하여, 두 개미는 정확히 같은 위치에 존재해야 부딪히고, 정확히 통로의 끝점에 가야 방향을 바꾼다고 생각하자.

처음의 시각을 0초로 두자. 0초에는 통로 위에 개미가 한 마리도 없다. 여러분은 다음과 같은 동작을 <span class="tex-span"><i>Q</i></span>번 처리하는 프로그램을 작성해야 한다.

1. <span class="tex-span"><i>t</i></span>초에 통로의 위치가 <span class="tex-span"><i>x</i></span>인 지점 위에 오른쪽 또는 왼쪽으로 움직이는 개미를 올린다. 이 개미가 <span class="tex-span"><i>i</i></span>번째로 올려졌다면, 이 개미에 번호 <span class="tex-span"><i>i</i></span>를 부여한다.
2. <span class="tex-span"><i>t</i></span>초일 때 <span class="tex-span"><i>i</i></span>번 개미의 좌표를 출력한다.

### 입력

첫 번째 줄에 두 자연수 <span class="tex-span"><i>L</i></span>과 <span class="tex-span"><i>Q</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>Q</i>&thinsp;&le;&thinsp;2&times;10<sup class="upper-index">5</sup></span>)가 주어진다.

다음 <span class="tex-span"><i>Q</i></span>개의 줄에는 프로그램이 처리해야 할 동작들이 한 줄에 하나씩 주어진다. 각 줄의 입력 형식은 아래와 같다.

* 먼저 동작을 하는 시점을 나타내는 정수 <span class="tex-span"><i>t</i></span>(<span class="tex-span">0&thinsp;&le;&thinsp;<i>t</i>&thinsp;&le;&thinsp;10<sup class="upper-index">18</sup></span>)와 동작의 종류를 나타내는 자연수 <span class="tex-span"><i>p</i></span>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>p</i>&thinsp;&le;&thinsp;2</span>)가 공백을 사이로 두고 주어진다.
 - <span class="tex-span"><i>p</i>&thinsp;=&thinsp;1</span>이면 개미가 올라가는 위치를 나타내는 정수 <span class="tex-span"><i>x</i></span>(<span class="tex-span">0&thinsp;&lt;&thinsp;<i>x</i>&thinsp;&lt;&thinsp;<i>L</i></span>)와 개미가 움직이는 방향을 나타내는 정수 <span class="tex-span"><i>d</i></span> (<img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/f0bc9ce4628976496a5fc89c55f4aaec278bb122.png"/>)가 공백을 사이로 두고 주어진다. 이는 <span class="tex-span"><i>t</i></span>초일 때 <span class="tex-span"><i>x</i></span>번 위치에 <span class="tex-span"><i>d</i>&thinsp;=&thinsp;1</span>이면 오른쪽으로, <span class="tex-span"><i>d</i>&thinsp;=&thinsp;-1</span>이면 왼쪽으로 움직이는 개미를 올린다는 의미이다. 이 위치에 다른 개미가 이미 있는 경우는 입력으로 주어지지 않는다.
 - <span class="tex-span"><i>p</i>&thinsp;=&thinsp;2</span>이면 위치를 알고 싶은 개미의 번호 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;</span>(현재 까지 올라간 개미 수))가 공백을 사이로 두고 주어진다. 이는 <span class="tex-span"><i>t</i></span>초에 <span class="tex-span"><i>i</i></span>번 개미의 좌표를 출력하라는 의미이다.
 
<span class="tex-span"><i>t</i></span>의 값이 증가하는 순서대로 입력이 주어지며(즉 시간 순으로 입력이 주어진다), 두 동작이 같은 <span class="tex-span"><i>t</i></span>를 가지는 경우는 없다(같은 시각에 두 가지 이상의 동작을 처리할 일은 없다). 
 
### 출력
 
<span class="tex-span"><i>p</i>&thinsp;=&thinsp;2</span>인 동작을 처리할 때마다, 각 줄에 문제에서 요구하는 답(개미의 좌표)을 출력한다.
 
### 부분문제
 
<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>Q</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>30</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>55</td>
  <td><span class="tex-span">&le; 2&times;10<sup class="upper-index">5</sup></span></td>
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
	
	<tr><td><samp>5 5<br>0 1 2 1<br>2 1 3 -1<br>6 2 2<br>7 2 1<br>8 2 2</samp></td><td><samp>1<br>2<br>0</samp></td></tr></tbody>
</table>