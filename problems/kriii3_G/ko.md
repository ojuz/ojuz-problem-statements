흑백 이미지에는 색이 없다. 따라서 흑백 이미지를 표현할 때에는, 각 픽셀마다 그 픽셀의 밝기를 나타내는 수치 하나만 기록한다. 이 문제에서는 0 이상 65,535 이하의 정수로 한 픽셀의 밝기를 나타낼 수 있다고 하자.

<span class="tex-span"><i>H</i>&thinsp;&times;&thinsp;<i>W</i></span> 크기의 흑백 사진 <span class="tex-span"><i>I</i></span>는 <span class="tex-span"><i>H</i>&thinsp;&times;&thinsp;<i>W</i></span>개의 픽셀들이 <span class="tex-span"><i>H</i></span>행 <span class="tex-span"><i>W</i></span>열로 배열된 형태라고 생각하고, <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>H</i></span>)행 <span class="tex-span"><i>j</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>W</i></span>)열에 있는 픽셀의 밝기를 <span class="tex-span"><i>I</i>[<i>i</i>,&thinsp;<i>j</i>]</span>로 표현하자.

경근이는 <span class="tex-span"><i>N</i>&thinsp;&times;&thinsp;<i>M</i></span> 크기의 흑백 이미지 <span class="tex-span"><i>A</i></span>와 <span class="tex-span"><i>R</i>&thinsp;&times;&thinsp;<i>C</i></span> 크기의 흑백 이미지 <span class="tex-span"><i>B</i></span>를 가지고 있다. 이 때 <span class="tex-span"><i>N</i>&thinsp;&ge;&thinsp;<i>R</i></span>, <span class="tex-span"><i>M</i>&thinsp;&ge;&thinsp;<i>C</i></span>이다. (<span class="tex-span"><i>A</i></span>가 <span class="tex-span"><i>B</i></span>보다 가로/세로 길이가 모두 더 길다) 경근이는 <span class="tex-span"><i>A</i></span>가 <span class="tex-span"><i>B</i></span>를 표절했다고 생각하고, <span class="tex-span"><i>A</i></span>에서 <span class="tex-span"><i>B</i></span>와 비슷한 부분이 몇 개나 되는지 찾고자 한다.

그 방법은 다음과 같다. 우선 흑백 이미지 <span class="tex-span"><i>A</i></span>에서 <span class="tex-span"><i>R</i>&thinsp;&times;&thinsp;<i>C</i></span> 크기의 픽셀로 구성된 직사각형을 하나 선택한다. 이 직사각형은 좌측 상단 꼭짓점에 있는 픽셀의 위치 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>x</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;<i>R</i>&thinsp;+&thinsp;1</span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>M</i>&thinsp;-&thinsp;<i>C</i>&thinsp;+&thinsp;1</span>)에 의해 결정된다.

<center>
<img class="thumbnail" style="border: none;" src="https://attach.oj.uz/contest/kriii3/imgG.png"/>
</center>

예를 들어 위 흑백 이미지를 <span class="tex-span"><i>A</i></span>라고 하자. <span class="tex-span"><i>A</i></span>에서 <span class="tex-span">4&thinsp;&times;&thinsp;6</span> 크기의 직사각형을 하나 선택했다고 하면 이 직사각형은 좌측 상단 꼭짓점인 <span class="tex-span">(4,&thinsp;4)</span>에 의해 결정된다. (만약 좌측 상단 꼭짓점을 움직이면, 크기가 고정되어 있으므로, 직사각형도 같이 움직일 것) 이 직사각형의 우측 하단 꼭짓점은 <span class="tex-span">(7,&thinsp;9)</span>인데, 이는 <span class="tex-span">(4&thinsp;+&thinsp;4&thinsp;-&thinsp;1,&thinsp;4&thinsp;+&thinsp;6&thinsp;-&thinsp;1)</span>과 같다.

이제 이 직사각형과 사진 <span class="tex-span"><i>B</i></span>가 비슷한지를 판단하는데, 그 기준은 다음과 같다.

<blockquote>
어떤 실수 <span class="tex-span"><i>p</i></span>와 <span class="tex-span"><i>q</i></span>가 모든 <span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>R</i></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>C</i></span>에 대해 <span class="tex-span"><i>p</i>&middot;<i>A</i>[<i>x</i>&thinsp;+&thinsp;<i>i</i>&thinsp;-&thinsp;1,&thinsp;<i>y</i>&thinsp;+&thinsp;<i>j</i>&thinsp;-&thinsp;1]&thinsp;+&thinsp;<i>q</i>&thinsp;=&thinsp;<i>B</i>[<i>i</i>,&thinsp;<i>j</i>]</span>를 만족시키면, <span class="tex-span"><i>A</i></span>에서 선택한 직사각형과 사진 <span class="tex-span"><i>B</i></span>는 비슷하다.
</blockquote>

이 판단 기준을 <span class="tex-span"><i>A</i></span>에 있는 모든 <span class="tex-span"><i>R</i>&thinsp;&times;&thinsp;<i>C</i></span> 크기의 직사각형에 대해 적용하여, <span class="tex-span"><i>B</i></span>와 비슷한 직사각형의 개수를 세면 된다. 다시 말해 <span class="tex-span">1&thinsp;&le;&thinsp;<i>x</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;<i>R</i>&thinsp;+&thinsp;1</span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>M</i>&thinsp;-&thinsp;<i>C</i>&thinsp;+&thinsp;1</span>를 만족하는 모든 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>에 대해 위 판단 기준을 적용한 후, 비슷하다고 판단되는 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span> 쌍의 수를 세면 된다. 참고로 크기가 같은 두 직사각형이 다르다는 것은 좌측 상단 꼭짓점의 좌표가 서로 다르다는 것으로, 직사각형 내부 픽셀의 밝기와는 관계가 없다.

여러분은 경근이를 도와 <span class="tex-span"><i>A</i></span>에서 <span class="tex-span"><i>B</i></span>와 비슷한 부분이 몇 개인지 구하는 프로그램을 작성해야 한다.


### 입력

첫 번째 줄에 흑백 이미지 <span class="tex-span"><i>A</i></span>의 행의 수 <span class="tex-span"><i>N</i></span>, 열의 수 <span class="tex-span"><i>M</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>,&thinsp;<i>M</i>&thinsp;&le;&thinsp;10<sup class="upper-index">3</sup></span>)이 공백을 사이로 두고 주어진다.

다음 <span class="tex-span"><i>N</i></span>개의 줄에는 <span class="tex-span"><i>A</i></span>의 픽셀들에 대한 정보가 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 <span class="tex-span"><i>M</i></span>개의 정수 <span class="tex-span"><i>A</i>[<i>i</i>,&thinsp;1],&thinsp;<i>A</i>[<i>i</i>,&thinsp;2],&thinsp;...,&thinsp;<i>A</i>[<i>i</i>,&thinsp;<i>M</i>&thinsp;-&thinsp;1],&thinsp;<i>A</i>[<i>i</i>,&thinsp;<i>M</i>]</span>이 공백을 사이로 두고 주어진다. 즉 <span class="tex-span"><i>i</i></span>번째 줄에서 <span class="tex-span"><i>j</i></span>번째로 주어지는 정수는 <span class="tex-span"><i>A</i></span>의 <span class="tex-span"><i>i</i></span>행 <span class="tex-span"><i>j</i></span>열에 있는 픽셀의 밝기를 의미한다.

그 다음 줄에 흑백 이미지 <span class="tex-span"><i>B</i></span>의 행의 수 <span class="tex-span"><i>R</i></span>, 열의 수 <span class="tex-span"><i>C</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i>&thinsp;&le;&thinsp;<i>N</i></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i>&thinsp;&le;&thinsp;<i>M</i></span>)이 공백을 사이로 두고 주어진다.

다음 <span class="tex-span"><i>N</i></span>개의 줄에는 <span class="tex-span"><i>B</i></span>의 픽셀들에 대한 정보가 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>R</i></span>)번째 줄에는 <span class="tex-span"><i>C</i></span>개의 정수 <span class="tex-span"><i>B</i>[<i>i</i>,&thinsp;1],&thinsp;<i>B</i>[<i>i</i>,&thinsp;2],&thinsp;...,&thinsp;<i>B</i>[<i>i</i>,&thinsp;<i>C</i>&thinsp;-&thinsp;1],&thinsp;<i>B</i>[<i>i</i>,&thinsp;<i>C</i>]</span>이 공백을 사이로 두고 주어진다. 즉 <span class="tex-span"><i>i</i></span>번째 줄에서 <span class="tex-span"><i>j</i></span>번째로 주어지는 정수는 <span class="tex-span"><i>B</i></span>의 <span class="tex-span"><i>i</i></span>행 <span class="tex-span"><i>j</i></span>열에 있는 픽셀의 밝기를 의미한다.

주어지는 모든 픽셀 밝기는 0 이상 65,535 이하의 정수임이 보장된다.

### 출력

<span class="tex-span"><i>A</i></span>에서 <span class="tex-span"><i>B</i></span>와 비슷한 부분의 개수를 출력한다.

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
  <td>33</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">2</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>68</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
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
	
	<tr><td><samp>4 4<br>1 2 3 4<br>2 1 4 3<br>3 4 1 2<br>4 3 2 1<br>2 2<br>5 6<br>6 5</samp></td><td><samp>5</samp></td></tr>
    <tr><td><samp>5 5<br>9 2 5 4 3<br>6 8 2 0 2<br>4 3 6 4 3<br>7 2 3 4 8<br>8 2 4 6 7<br>3 3<br>77 77 77<br>77 77 77<br>77 77 77</samp></td><td><samp>9</samp></td></tr>
    </tbody>
</table>

두 번째 예제의 경우 <span class="tex-span"><i>p</i>&thinsp;=&thinsp;0, <i>q</i>&thinsp;=&thinsp;77</span>이면 모든 부분이 비슷하다고 판별된다.