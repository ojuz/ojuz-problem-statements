<b>올바른 괄호 문자열</b>이란 다음과 같은 문자열의 집합이다.

* 빈 문자열은 올바른 괄호 문자열이다.
* <samp>S</samp>가 올바른 괄호 문자열이면 <samp>(S)</samp>도 올바른 괄호 문자열이다. 즉 올바른 괄호 문자열의 앞에 여는 괄호를 붙이고 뒤에 닫는 괄호를 붙여도 올바른 괄호 문자열이다.
* <samp>S</samp>와 <samp>T</samp>가 올바른 괄호 문자열이면 <samp>ST</samp>도 올바른 괄호 문자열이다. 즉 올바른 괄호 문자열을 이어 붙여도 올바른 괄호 문자열이다.

그는 괄호 문자열을 매우 좋아한다. 하지만 괄호의 종류를 하나만 사용해왔던 것이 너무 재미가 없어서 서로 구별할 수 있는 <span class="tex-span"><i>K</i>&thinsp;</span>개의 색을 괄호에 칠하기로 했다. 예를 들어 <span class="tex-span"><i>K</i> = 3&thinsp;</span>이고 빨간색, 녹색, 파란색을 사용하기로 했다면 위의 정의에서 두 번째 부분이 아래처럼 확장된다.

* <samp>S</samp>가 올바른 괄호 문자열이면 <samp><span style="color: #F00000;"><b>(</b></span>S<span style="color: #F00000;"><b>)</b></span></samp>, <samp><span style="color: #00B050;"><b>(</b></span>S<span style="color: #00B050;"><b>)</b></span></samp>, <samp><span style="color: #0070C0;"><b>(</b></span>S<span style="color: #0070C0;"><b>)</b></span></samp>도 올바른 괄호 문자열이다. 즉 올바른 괄호 문자열의 앞에 여는 괄호를 붙이고 뒤에 닫는 괄호를 붙여도 올바른 괄호 문자열이다.

<span class="tex-span"><i>K</i>&thinsp;</span>가 더 늘어나면 구별 가능한 색을 더 추가해서 정의를 확장하면 된다. 이제 <span class="tex-span">2<i>N</i>&thinsp;</span>개의 괄호를 사용하여 만든 올바른 문자열 중에서 자기 자신과 자기 자신을 뒤집은 문자열이 같은 것들의 개수를 구하는 프로그램을 작성하라. 어떤 문자열을 뒤집는다는 것은 문자열을 거울에 비춘 다음 거울에 비친 모양대로 적는다는 것과 같다. 예를 들어 <span style="color: #F00000;"><b>(</b></span><span style="color: #00B050;"><b>()</b></span><span style="color: #F00000;"><b>)</b></span><span style="color: #0070C0;"><b>()</b></span>를 뒤집으면 <span style="color: #0070C0;"><b>()</b></span><span style="color: #F00000;"><b>(</b></span><span style="color: #00B050;"><b>()</b></span><span style="color: #F00000;"><b>)</b></span>가 될 것이다. 이 문자열은 자기 자신과 뒤집은 문자열이 같지 않으므로 세면 안 된다. <span style="color: #0070C0;"><b>()</b></span><span style="color: #F00000;"><b>(</b></span><span style="color: #00B050;"><b>()</b></span><span style="color: #F00000;"><b>)</b></span><span style="color: #0070C0;"><b>()</b></span>는 뒤집어도 똑같이 <span style="color: #0070C0;"><b>()</b></span><span style="color: #F00000;"><b>(</b></span><span style="color: #00B050;"><b>()</b></span><span style="color: #F00000;"><b>)</b></span><span style="color: #0070C0;"><b>()</b></span>가 될 것이므로 개수를 세어야 한다.

<br>

### 입력

첫 번째 줄에는 사용하는 괄호의 개수와 괄호의 색을 나타내는 두 자연수 <span class="tex-span"><i>N</i>, <i>K</i>&thinsp;</span>가 공백으로 구분되어 주어진다.

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
  <td><center>8</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
  <td><center><span class="tex-span"><i>K</i> = 1</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>92</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

<span class="tex-span"><i>K</i>&thinsp;</span>종류의 괄호를 <span class="tex-span">2<i>N</i>&thinsp;</span>개 사용해 올바른 괄호 문자열을 만들었을 때, 자기 자신과 자기 자신을 뒤집은 문자열이 같은 것들의 개수를 출력한다. 이 수는 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

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
		<tr><td><samp>2 2</samp></td><td><samp>6</samp></td></tr>
    </tbody>
</table>

다음의 6가지 경우가 있을 수 있다.

<center>  	 	 
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii4/R.png" style="border: none; width: 40%; height: 40%"/>  	 	 
</center>