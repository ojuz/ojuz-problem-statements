경근이는 새로운 컴퓨터를 발명했다. 이 컴퓨터는 다른 컴퓨터들과는 달리 [이진법](https://ko.wikipedia.org/wiki/%EC%9D%B4%EC%A7%84%EB%B2%95)이 아닌 [사진법](https://ko.wikipedia.org/wiki/%EC%82%AC%EC%A7%84%EB%B2%95)으로 자료를 저장한다. 

이 컴퓨터에서 <span class="tex-span"><i>p</i>&thinsp;+&thinsp;<i>q</i></span>의 연산 결과와 <img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/66a462b7179d9ea6bd80ffb431f0606ab96e488d.png"/>의 연산 결과를 표로 나타내면 아래와 같다. 

<center>  	 	 
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii3/imgZ.png" style="border: none;"/>  	 	 
</center>

경근이는 자신이 발명한 컴퓨터가 너무나 혁신적이라고 생각하여, 이를 한시라도 빨리 사용해 보고 싶은 마음에 컴퓨터를 직접 만들었다!

이 컴퓨터는 아주 적은 예산을 들여 임시로 만든 것이기 때문에, <span class="tex-span"><i>N</i></span>개의 변수만 저장할 수 있으며, 각 변수는 0 이상 3 이하의 정수 하나만 저장할 수 있다. 경근이는 편의상 각 변수에 0 이상 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;1</span> 이하의 번호를 붙였고, <span class="tex-span"><i>i</i></span>번 변수를 <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>로 부르기로 했다.

경근이는 시간과 정성을 들여 꼭 필요하다고 판단한 4가지 기본 명령을 만들었다. 

* <samp>addv</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>,&thinsp;<i>z</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span"><i>x</i>, <i>y</i>, <i>z</i></span>의 값은 모두 정수): <span class="tex-span"><i>v</i><sub class="lower-index"><i>x</i></sub></span>에 <span class="tex-span"><i>v</i><sub class="lower-index"><i>y</i></sub>&thinsp;+&thinsp;<i>v</i><sub class="lower-index"><i>z</i></sub></span>의 값을 대입한다. 
* <samp>xorv</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>,&thinsp;<i>z</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span"><i>x</i>, <i>y</i>, <i>z</i></span>의 값은 모두 정수): <span class="tex-span"><i>v</i><sub class="lower-index"><i>x</i></sub></span>에 <img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/1d63e409946aaf72e0a685beff06bf0600e1ea50.png"/>의 값을 대입한다. 
* <samp>addc</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span">0&thinsp;&le;&thinsp;<i>z</i>&thinsp;&le;&thinsp;3</span>, <span class="tex-span"><i>x</i>, <i>y</i>, <i>z</i></span>의 값은 모두 정수): <span class="tex-span"><i>v</i><sub class="lower-index"><i>x</i></sub></span>에 <span class="tex-span"><i>v</i><sub class="lower-index"><i>y</i></sub>&thinsp;+&thinsp;<i>z</i></span>의 값을 대입한다. 
* <samp>xorc</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span">0&thinsp;&le;&thinsp;<i>z</i>&thinsp;&le;&thinsp;3</span>, <span class="tex-span"><i>x</i>, <i>y</i>, <i>z</i></span>의 값은 모두 정수): <span class="tex-span"><i>v</i><sub class="lower-index"><i>x</i></sub></span>에 <img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/5da491c305ffe693ea8794c7658bf0291b731918.png"/>의 값을 대입한다.

경근이는 <span class="tex-span"><i>M</i></span>개의 기본 명령을 나열한 코드를 작성했다. 코드를 컴파일하면 프로그램이 생성되는데, 이 프로그램은 명령을 실행하기 전 각 변수 <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>에 저장할 값을 입력받아, 코드에 있는 <span class="tex-span"><i>M</i></span>개의 명령을 하나씩 하나씩 순서대로 실행하고, 모든 명령을 실행한 이후 각 변수 <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>에 저장되어 있는 값을 출력한다. 편의상 입력을 <span class="tex-span"><i>a</i><sub class="lower-index">0</sub>,&thinsp;<i>a</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>a</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span>로, 출력을 <span class="tex-span"><i>b</i><sub class="lower-index">0</sub>,&thinsp;<i>b</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>b</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span>로 나타내자.

아쉽게도, 경근이의 구현 실수로 인해, 모든 변수 <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>에는 초기에 저장될 수 없는 값인 <span class="tex-span"><i>f</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>f</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;3</span>)이 존재한다. 따라서 <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub>&thinsp;&ne;&thinsp;<i>f</i><sub class="lower-index"><i>i</i></sub></span>여야 하므로, <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>로 가능한 값은 0, 1, 2, 3 중 <span class="tex-span"><i>f</i><sub class="lower-index"><i>i</i></sub></span>가 아닌 수들이다. 그러므로 가능한 모든 입력의 수는 <span class="tex-span">3<sup class="upper-index"><i>N</i></sup></span>가지임을 알 수 있다.

경근이는 완벽한 프로그램을 작성했는지 알고자 모든 가능한 입력들을 고려해 보기로 한다. 경근이는 결과를 기록하기 위해 <span class="tex-span"><i>N</i></span>페이지로 구성된 노트를 구매했으며, 각 페이지에 0 이상 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;1</span> 이하의 정수 번호를 붙였다. 경근이는 가능한 모든 입력을 만들어 이를 모두 한번씩 프로그램에 넣어 보면서, 각 입력에 대한 프로그램의 출력 <span class="tex-span"><i>b</i><sub class="lower-index">0</sub>,&thinsp;<i>b</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>b</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span>을 얻은 후, <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>의 값을 <span class="tex-span"><i>i</i></span>번 페이지에 적는 일을 할 것이다.

모든 입력을 고려한 이후, <span class="tex-span"><i>i</i></span>번 페이지에 적혀 있는 수들의 합을 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>라고 하자. 경근이는 작업을 시작하기 전, 최소한의 안전 장치를 마련하고자 모든 <span class="tex-span"><i>i</i></span>에 대해 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>를 4로 나눈 나머지를 알고자 한다.

### 입력

첫 번째 줄에 변수의 수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;18</span>)과 명령의 수 <span class="tex-span"><i>M</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;400</span>)이 주어진다.

두 번째 줄에는 <span class="tex-span"><i>f</i><sub class="lower-index">0</sub>,&thinsp;<i>f</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>f</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>f</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;3</span>)이 공백을 사이로 두고 주어진다. 여기서 <span class="tex-span"><i>f</i><sub class="lower-index"><i>i</i></sub></span>는 명령을 실행하기 전 변수 <span class="tex-span"><i>v</i><sub class="lower-index"><i>i</i></sub></span>에 저장될 수 없는 값이며, 정수이다.

이후 <span class="tex-span"><i>M</i></span>개의 줄에 명령들이 실행되는 순서대로 한 줄에 하나씩 주어진다. 이 중 <span class="tex-span"><i>j</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>M</i></span>)번째 줄의 입력 형식은 다음과 같으며, 주어지는 모든 수는 정수이며, 공백 하나로 구분된다.

* "<span class="tex-span">0</span> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>" (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>,&thinsp;<i>z</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>): <span class="tex-span"><i>j</i></span>번째로 실행되는 명령이 <samp>addv</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>임을 나타낸다.
* "<span class="tex-span">1</span> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>" (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>,&thinsp;<i>z</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>): <span class="tex-span"><i>j</i></span>번째로 실행되는 명령이 <samp>xorv</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>임을 나타낸다.
* "<span class="tex-span">2</span> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>" (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span">0&thinsp;&le;&thinsp;<i>z</i>&thinsp;&le;&thinsp;3</span>): <span class="tex-span"><i>j</i></span>번째로 실행되는 명령이 <samp>addc</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>임을 나타낸다.
* "<span class="tex-span">3</span> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>" (<span class="tex-span">0&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>, <span class="tex-span">0&thinsp;&le;&thinsp;<i>z</i>&thinsp;&le;&thinsp;3</span>): <span class="tex-span"><i>j</i></span>번째로 실행되는 명령이 <samp>xorc</samp> <span class="tex-span"><i>x</i></span> <span class="tex-span"><i>y</i></span> <span class="tex-span"><i>z</i></span>임을 나타낸다.

### 출력

<span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>를 4로 나눈 나머지를 <span class="tex-span"><i>t</i><sub class="lower-index"><i>i</i></sub></span>라고 할 때, 첫 번째 줄에 <span class="tex-span"><i>t</i><sub class="lower-index">0</sub></span>, <span class="tex-span"><i>t</i><sub class="lower-index">1</sub></span>, <span class="tex-span">...</span>, <span class="tex-span"><i>t</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span>을 공백을 사이로 두고 출력한다.

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-5 col-md-5 col-lg-5"><span class="tex-span"><i>N</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>31</td>
  <td><span class="tex-span">&le; 12</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>95</td>
  <td><span class="tex-span">&le; 18</span></td>
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
	
	<tr><td><samp>2 2<br>2 3<br>0 0 1 0<br>1 1 1 0</samp></td><td><samp>1 0</samp></td></tr></tbody>
</table>