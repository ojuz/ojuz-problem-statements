<span class="tex-span"><i>N</i>&thinsp;&times;&thinsp;<i>M</i></span> 크기의 격자판이 있다. 격자판의 각 칸은 빨간색 또는 파란색으로 색칠되어 있다. 편의상 <span class="tex-span"><i>i</i></span>행 <span class="tex-span"><i>j</i></span>열 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>M</i></span>)의 격자를 <span class="tex-span">(<i>i</i>,&thinsp;<i>j</i>)</span>로 표시한다.

주어진 격자판 내에서 빨간색 격자로만 이루어진 직사각형의 개수를 세는 프로그램을 작성하자. 여기서 직사각형은 <span class="tex-span">1&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index">2</sub>&thinsp;&le;&thinsp;<i>N</i></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>y</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>y</i><sub class="lower-index">2</sub>&thinsp;&le;&thinsp;<i>M</i></span>를 만족하는 네 개의 정수 <span class="tex-span"><i>x</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">2</sub></span>에 의해 결정되며, <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>x</i>&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index">2</sub></span>와 <span class="tex-span"><i>y</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>y</i><sub class="lower-index">2</sub></span>를 만족하는 모든 격자 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>를 일컫는다. 예를 들어 <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>&thinsp;=&thinsp;2,&thinsp;<i>y</i><sub class="lower-index">1</sub>&thinsp;=&thinsp;3,&thinsp;<i>x</i><sub class="lower-index">2</sub>&thinsp;=&thinsp;4,&thinsp;<i>y</i><sub class="lower-index">2</sub>&thinsp;=&thinsp;4</span>라면, 6개의 격자 (2, 3), (2, 4), (3, 3), (3, 4), (4, 3), (4, 4)가 모두 한 직사각형에 속한다. 두 직사각형이 서로 다르다는 것은 <span class="tex-span">[<i>x</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">2</sub>]</span>이 서로 다르다는 것이다.


### 입력

첫 번째 줄에 행의 수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;3,000</span>)과 열의 수 <span class="tex-span"><i>M</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;3,000</span>)이 공백을 사이로 두고 주어진다.

다음 <span class="tex-span"><i>N</i></span>개의 줄의 각 줄에는 <span class="tex-span"><i>M</i></span>개의 문자가 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄은 주어진 격자판의 <span class="tex-span"><i>i</i></span>번째 행의 격자에 칠해진 색들을 나타내며, 이 중 <span class="tex-span"><i>j</i></span>번째 문자는 <span class="tex-span">(<i>i</i>,&thinsp;<i>j</i>)</span>에 칠해진 색을 나타낸다. 모든 문자는 'R' 또는 'B'로만 구성된다. 'R'은 해당 칸이 빨간색임을, 'B'는 해당 칸이 파란색임을 의미한다.


### 출력

첫 번째 줄에 빨간색 격자로만 이루어진 직사각형의 개수를 출력한다.


### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>10</td>
  <td><span class="tex-span">&le; 500</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>10</td>
  <td><span class="tex-span">&le; 3,000</span></td>
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
	
	<tr><td><samp>2 2<br>RR<br>RB</samp></td><td><samp>5</samp></td></tr></tbody>
</table>

5개의 직사각형은 다음과 같다. (<span class="tex-span">[<i>x</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>x</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>y</i><sub class="lower-index">2</sub>]</span>으로 나타냄)

* [1, 1, 1, 1]
* [1, 1, 1, 2]
* [1, 2, 1, 2]
* [1, 1, 2, 1]
* [2, 1, 2, 1]