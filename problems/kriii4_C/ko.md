그가 사는 집의 한 벽면은 <span class="tex-span">1&thinsp;&times;&thinsp;1</span>크기의 정사각형 벽돌 <span class="tex-span"><i>H</i>&thinsp;&times;&thinsp;<i>W</i></span>개로 이루어진 직사각형 형태이다. 즉, 이 벽은 <span class="tex-span">1&thinsp;&times;&thinsp;1&thinsp;</span>크기의 정사각형 벽돌이 세로로 <span class="tex-span"><i>H</i></span>행, 가로로 <span class="tex-span"><i>W</i></span>열 쌓여 있는 것이다.

그는 창문이 없는 집이 너무 답답했기 때문에, 벽에 있는 몇 개의 벽돌을 제거하여 창문을 만들려고 한다. 창문을 만들 것이기 때문에, 제거하는 벽돌들은 하나로 붙어 있는 직사각형 모양을 이루어야 한다.

일단 그는 창문을 설치하는 것은 다음에 생각하도록 하고, 우선 창문을 만들 위치를 정해 그 위치에 있는 모든 벽돌을 제거하기로 했다. 그는 무작위성을 좋아하기 때문에, 설치하는 것이 가능한 창문의 위치 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_C/98bfc193ce2a40188795c52634877f448e21cafb.png">개 중 하나를 무작위로 선택하여 해당하는 모든 벽돌을 제거하려고 한다. 벽돌 하나를 제거하는 데 드는 비용은 9(九)원이다. 그가 벽돌을 제거하기 위해 드는 비용의 기댓값을 출력하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 벽의 크기를 나타내는 두 자연수 <span class="tex-span"><i>H</i>&thinsp;</span>와 <span class="tex-span"><i>W</i>&thinsp;</span>가 공백 하나로 구분되어 주어진다.

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
  <th class="col-sm-4 col-md-4 col-lg-4"><center><span class="tex-span"><i>H,&thinsp;W</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>3</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i>,&thinsp;<i>W</i>&thinsp;&le;&thinsp;50</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>97</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i>,&thinsp;<i>W</i>&thinsp;&le;&thinsp;10<sup class="upper-index">18</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
그가 벽돌을 제거하기 위해 드는 비용의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>1 1</samp></td><td><samp>9</samp></td></tr>
		<tr><td><samp>3 5</samp></td><td><samp>35</samp></td></tr>
		<tr><td><samp>8 10</samp></td><td><samp>120</samp></td></tr>
		<tr><td><samp>1234567890 999999999999</samp></td><td><samp>259384379</samp></td></tr>
    </tbody>
</table>