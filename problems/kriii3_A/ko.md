엘리가 좋아하는 과자는 직각삼각형 모양이고, 빗변을 제외한 다른 두 변의 길이가 각각 <span class="tex-span"><i>a</i></span>와 <span class="tex-span"><i>b</i></span>이다. 어느 날 엘리는 이 과자를 많이 많이 먹을 수 있는 방법을 떠올리고 자신의 천재성에 전율했다.

<center>
<img class="thumbnail" src="https://attach.oj.uz/contest/kriii3/imgM.png"/>
</center>

엘리는 빗변의 양 끝점이 아닌 점에서 빗변으로 과자를 자르면 직각삼각형 두 개를 만들 수 있다는 것을 알았다! 사실 이렇게 잘라봐야 과자의 총 면적은 같지만, 어린 엘리는 과자가 두 개가 되었다는 사실이 너무 행복했고 이런 방법을 떠올린 자신이 너무 기특했다. 그리고 또 생각했다. 직각삼각형 모양 과자가 두 개가 되었으니까 이 두 개를 아까처럼 자르면 직각삼각형 모양 과자가 네 개… 여덟 개… <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개! 즉 엘리가 하나의 직각삼각형 모양 과자를 가지고 시작해서 자신이 가진 모든 과자를 잘라 과자의 개수를 두 배로 불리는 것을 <span class="tex-span"><i>N</i></span>번 반복하면 엘리가 가진 직각삼각형 모양 과자의 개수는 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개가 되는 것이다! 이렇게 자르는 것은 엘리가 가진 놀라운 힘을 이용하면 간단한 것이었고, 엘리는 이미 이런 식으로 과자들을 자르는 행위를 <span class="tex-span"><i>N</i></span>번 반복해 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개의 조각을 가지고 있다.

엘리는 이 과자들을 모두 먹고 싶었지만 모두 먹기에는 너무 조각이 많다고 생각해서 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>개의 조각들 중 크기(=면적)가 <span class="tex-span"><i>K</i></span>번째로 큰 한 조각은 바보 피터에게 주기로 했다. 피터가 받게 될 과자의 면적이 얼마지 구하는 프로그램을 작성하라.

### 입력

첫 번째 줄에 네 개의 자연수 <span class="tex-span"><i>a</i></span>, <span class="tex-span"><i>b</i></span>, <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>K</i></span> (<span class="tex-span">1&thinsp;≤&thinsp;<i>a</i>,&thinsp;<i>b</i>&thinsp;≤&thinsp;100</span>, <span class="tex-span">1&thinsp;≤&thinsp;<i>N</i>&thinsp;≤&thinsp;40</span>, <span class="tex-span">1&thinsp;≤&thinsp;<i>K</i>&thinsp;≤&thinsp;2<sup class="upper-index"><i>N</i></sup></span>)이 공백을 사이로 두고 주어진다.

### 출력

첫 번째 줄에 피터가 받게 될 과자의 크기(=면적)를 출력한다. 다만 이 값이 너무 작을 수 있으므로, 면적에 자연 로그(<img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/32c31c1837a97fbf3b6bb5a9452cd00fd8e642a4.png">)을 취한 값을 출력한다. (즉 면적이 <span class="tex-span"><i>S</i></span>라면, <img align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii3/ab5e35ce16e5d96926cf5577f14ed4b8ff68e371.png">의 값을 출력해야 한다.) `math.h` 또는 `cmath` 헤더에 있는 `log` 함수([레퍼런스](http://www.cplusplus.com/reference/cmath/log/))가 자연 로그를 계산하는 함수이다.

출제진이 의도한 정답과의 절대 오차 또는 상대 오차가 <span class="tex-span">10<sup class="upper-index">&thinsp;-&thinsp;8</sup></span> 이하이면 올바른 답안으로 인정한다. 비교는 여러분이 출력한 값, 즉 면적에 자연로그를 취한 값을 기준으로 이루어진다.

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
  <td>10</td>
  <td><span class="tex-span">&le; 10</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>23</td>
  <td><span class="tex-span">&le; 40</span></td>
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
	
	<tr><td><samp>3 4 1 1</samp></td><td><samp>1.345472366600</samp></td></tr><tr><td><samp>3 4 1 2</samp></td><td><samp>0.770108221696</samp></td></tr><tr><td><samp>1 1 40 1</samp></td><td><samp>-28.419034402958</samp></td></tr></tbody>
</table>