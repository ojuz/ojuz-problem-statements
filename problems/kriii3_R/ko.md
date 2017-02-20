'<samp>(</samp>'와 '<samp>)</samp>'로만 이루어진 문자열들을 괄호 문자열이라 하는데 괄호 문자열 중에서도 <b>올바른 괄호 문자열</b>은 아래와 같이 정의된다.

1. 빈 문자열은 올바른 괄호 문자열이다.
2. 문자열 <samp>S</samp>가 올바른 괄호 문자열이면 <samp>(S)</samp>도 올바른 괄호 문자열이다.
3. 문자열 <samp>S</samp>와 <samp>T</samp>가 올바른 괄호 문자열이면 <samp>ST</samp>도 올바른 괄호 문자열이다.

올바른 괄호 문자열이 아닌 괄호 문자열들은 <b>올바르지 않은 괄호 문자열</b>이라고 한다. 올바른 괄호 문자열의 예로는 "<samp>(())()</samp>", "<samp>()()()</samp>", "<samp>(()())</samp>” 등이 있고, 올바르지 않은 괄호 문자열의 예로는 "<samp>())(()</samp>", "<samp>(</samp>", "<samp>(()()()</samp>" 등이 있다.

어떤 문자열 <samp>S</samp>가 ***주기성이 있는 문자열***이라는 것은 문자열 <samp>S</samp>의 비어 있지 않은 접두사 <samp>u</samp>가 동시에 <samp>S</samp>의 접미사일 때가 있음을 뜻한다. 주기성이 있는 문자열이 아닌 문자열들은 ***주기성이 없는 문자열***이라고 한다. 주기성이 있는 문자열의 예로는 "<samp>abcabcab</samp>", "<samp>()(</samp>", "<samp>aaaaaa</samp>" 등이 있고, 주기성이 없는 문자열의 예로는 "<samp>abcd</samp>", "<samp>(())()</samp>", "<samp>a</samp>" 등이 있다. 각각 두 번째로 들었던 예는 주기성이 있는 괄호 문자열과 주기성이 없는 괄호 문자열이라고 할 수 있다.

길이가 <span class="tex-span"><i>L</i></span>인 괄호 문자열들 중에서 주어진 조건을 만족하는 개수를 구하는 프로그램을 작성하시오.

### 입력

첫 번째 줄에 네 정수 <span class="tex-span"><i>p</i></span>, <span class="tex-span"><i>q</i></span>, <span class="tex-span"><i>m</i></span>, <span class="tex-span"><i>Q</i></span> (<span class="tex-span">0 &le; <i>p</i>, <i>q</i> &le; 1</span>, <span class="tex-span">1 &le; <i>m</i> &le; 10<sup class="upper-index">6</sup></span>, <span class="tex-span">1 &le; <i>Q</i> &le; 10<sup class="upper-index">5</sup></span>)이 공백을 사이로 두고 차례대로 주어진다.

다음 <span class="tex-span"><i>Q</i></span>개의 각 줄에는 하나의 자연수 <span class="tex-span"><i>L</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span>)이 주어진다. 앞으로 길이가 <span class="tex-span"><i>L</i></span>인 모든 괄호 문자열의 집합을 <span class="tex-span"><i>A</i><sub class="lower-index"><i>L</i></sub></span>, 길이가 <span class="tex-span"><i>L</i></span>인 올바르지 않은 괄호 문자열의 집합을 <span class="tex-span"><i>B</i><sub class="lower-index"><i>L</i></sub></span>, 길이가 <span class="tex-span"><i>L</i></span>인 주기성이 없는 괄호 문자열의 집합을 <span class="tex-span"><i>C</i><sub class="lower-index"><i>L</i></sub></span>이라고 하자. 주어지는 각 <span class="tex-span"><i>L</i></span>마다 <span class="tex-span"><i>p</i>&thinsp;=&thinsp;0</span>이면 <span class="tex-span"><i>P</i>&thinsp;=&thinsp;<i>A</i><sub class="lower-index"><i>L</i></sub></span>, <span class="tex-span"><i>p</i>&thinsp;=&thinsp;1</span>이면 <span class="tex-span"><i>P</i>&thinsp;=&thinsp;<i>B</i><sub class="lower-index"><i>L</i></sub></span>이고, <span class="tex-span"><i>q</i>&thinsp;=&thinsp;0</span>이면 <span class="tex-span"><i>Q</i>&thinsp;=&thinsp;<i>A</i><sub class="lower-index"><i>L</i></sub></span>, <span class="tex-span"><i>q</i>&thinsp;=&thinsp;1</span>이면 <span class="tex-span"><i>Q</i>&thinsp;=&thinsp;<i>C</i><sub class="lower-index"><i>L</i></sub></span>이다. 여러분은 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii3_K/428c5c1261c7f5dbbe64b15636538d56e4c59174.png"/>의 크기를 <span class="tex-span"><i>m</i></span>으로 나눈 나머지를 출력해야 한다.

즉 <span class="tex-span"><i>p</i>&thinsp;=&thinsp;1,&thinsp;<i>q</i>&thinsp;=&thinsp;0</span>이면 길이가 <span class="tex-span"><i>L</i></span>인 올바르지 않은 괄호 문자열의 개수를, <span class="tex-span"><i>p</i>&thinsp;=&thinsp;0,&thinsp;<i>q</i>&thinsp;=&thinsp;1</span>이면 길이가 <span class="tex-span"><i>L</i></span>인 주기성이 없는 괄호 문자열의 개수를, <span class="tex-span"><i>p</i>&thinsp;=&thinsp;1,&thinsp;<i>q</i>&thinsp;=&thinsp;1</span>이면 길이가 <span class="tex-span"><i>L</i></span>인 올바르지 않으면서 주기성도 없는 괄호 문자열의 개수를 구하면 된다.

### 출력

<span class="tex-span"><i>Q</i></span>개의 줄에 걸쳐서 입력에서 정의한 대로 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii3_K/428c5c1261c7f5dbbe64b15636538d56e4c59174.png"/>의 크기를 <span class="tex-span"><i>m</i></span>으로 나눈 나머지를 출력하면 된다.

### 부분 문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-3 col-md-3 col-lg-3">점수</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>p</i></span></th>       
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>q</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>38</td>
  <td>1</td>
  <td>0</td>
 </tr>
 <tr>
  <td>2</td>
  <td>35</td>
  <td>0</td>
  <td>1</td>
 </tr>
 <tr>
  <td>3</td>
  <td>40</td>
  <td>1</td>
  <td>1</td>
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
	
	<tr><td><samp>1 0 17 2<br>4<br>8</samp></td><td><samp>14<br>4</samp></td></tr><tr><td><samp>0 1 17 2<br>4<br>8</samp></td><td><samp>6<br>6</samp></td></tr><tr><td><samp>1 1 17 2<br>4<br>8</samp></td><td><samp>5<br>12</samp></td></tr></tbody>
</table>

길이가 4인 괄호 문자열 중에서 올바른 것은 "<samp>()()</samp>"과 "<samp>(())</samp>"의 두 가지이므로, 올바르지 않은 괄호 문자열의 개수는 16 - 2 = 14개 이다.

그리고 길이가 4인 주기성이 없는 괄호 문자열은 "<samp>((()</samp>", "<samp>(())</samp>", "<samp>()))</samp>", "<samp>)(((</samp>", "<samp>))((</samp>", "<samp>)))(</samp>"의 6개이고, 이 중에서 올바른 괄호 문자열은 "<samp>(())</samp>" 하나이므로, 길이가 4인 올바르지 않으면서 주기성도 없는 괄호문자열은 5개이다.