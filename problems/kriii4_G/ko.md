<span class="tex-span">1&thinsp;&times;&thinsp;1&thinsp;</span>크기의 정사각형 <span class="tex-span"><i>H</i>&thinsp;&times;&thinsp;<i>W</i>&thinsp;</span>개로 이루어진 직사각형이 있다. 즉, 이 직사각형은 <span class="tex-span"><i>H</i>&thinsp;</span>개의 행과 <span class="tex-span"><i>W</i>&thinsp;</span>개의 열을 가지고 균등한 <span class="tex-span">1&thinsp;&times;&thinsp;1&thinsp;</span>크기의 정사각형으로 나뉘어 있는 것이다. 각 정사각형은 흑색으로 칠해져 있거나 백색으로 칠해져 있을 수 있으며, 그 확률은 각각 <span class="tex-span">50%</span>이다.

이 직사각형에서 <i>부분 직사각형</i>이라는 것을 정의한다. 부분 직사각형은 한 개 이상의 행을 선택하고 한 개 이상의 열을 선택하여 이 행이나 열에 포함되지 않는 모든 정사각형을 제외하여 만드는 직사각형이다. 예를 들어 <span class="tex-span">3&thinsp;&times;&thinsp;5&thinsp;</span>크기의 직사각형이 적절히 칠해져 있다고 하자. 첫 번째, 세 번째 행을 선택하고 두 번째, 네 번째, 다섯 번째 열을 선택하면 다음과 같이 선택되는 것이다.

<center>  	 	 
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii4/G.png" style="border: none;"/>  	 	 
</center>

부분 직사각형에 칠해진 구성이 같아도 선택한 행과 열 중에서 하나라도 다른 것이 있다면 다른 경우로 생각한다. 부분 직사각형을 만들었을 때, 포함된 <b>모든</b> 칸의 색이 흑색이면 흑색 부분 직사각형, 백색이면 백색 부분 직사각형이라고 하자. 흑색 부분 직사각형의 개수와 백색 부분 직사각형의 개수를 곱한 값의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 직사각형의 크기를 나타내는 두 자연수 <span class="tex-span"><i>H</i>&thinsp;</span>와 <span class="tex-span"><i>W</i>&thinsp;</span>가 공백 하나로 구분되어 주어진다.

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
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>H,&thinsp;W</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>6</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i>,&thinsp;<i>W</i>&thinsp;&le;&thinsp;4</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>94</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i>,&thinsp;<i>W</i>&thinsp;&le;&thinsp;10<sup class="upper-index">3</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
흑색 부분 직사각형의 개수와 백색 부분 직사각형의 개수를 곱한 값의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>1 2</samp></td><td><samp>500000004</samp></td></tr>
		<tr><td><samp>2 2</samp></td><td><samp>250000007</samp></td></tr>
		<tr><td><samp>99 101</samp></td><td><samp>395910821</samp></td></tr>
    </tbody>
</table>