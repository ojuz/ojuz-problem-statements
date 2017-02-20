<CENTER> <IMG src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii3_EE/a79c4399504ad995e7d257beb230e5a167fd4c65.png"> </CENTER>

정우는 "뚊"과 "돌돔"을 의미하는 두 이미지를 받았다. 과연 두 그림이 같은지 검사해보자. 즉 <span class="tex-span"><i>N</i>&times;?<i>M</i></span> 크기의 이미지와 <span class="tex-span"><i>N</i>?&times;2?<i>M</i></span> 크기의 이미지가 주어질 때 첫 번째 이미지를 가로로 두 배로 늘이면 두 번째 이미지가 되는지 검사하는 프로그램을 작성하라.

### 입력

입력의 첫 번째 줄에 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span> (<span class="tex-span">1?&le;?<i>N</i>,?<i>M</i>?&le;?10</span>)이 주어진다. 다음 <span class="tex-span"><i>N</i></span>개의 줄의 각 줄에는 <span class="tex-span"><i>M</i></span>개의 문자가 주어진다. 다음 <span class="tex-span"><i>N</i></span>개의 줄의 각 줄에는 <span class="tex-span">2<i>M</i></span>개의 문자가 주어진다. 모든 문자는 영문 알파벳 대문자 혹은 소문자이다.

### 출력

첫 번째로 주어진 이미지를 가로로 두 배로 늘렸을 때 두 번째 이미지가 된다면 "<samp>Eyfa</samp>"을 출력하고, 되지 않는다면 "<samp>Not Eyfa</samp>"을 출력한다.

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
  <td><span class="tex-span">= 1</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>10</td>
  <td><span class="tex-span">&le; 10</span></td>
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
	
	<tr><td><samp>1 5<br>ABCDE<br>AABBCCDDEE</samp></td><td><samp>Eyfa</samp></td></tr><tr><td><samp>1 5<br>ABCDE<br>AABBCCDDEF</samp></td><td><samp>Not Eyfa</samp></td></tr><tr><td><samp>2 2<br>AB<br>CD<br>AABB<br>CCDD</samp></td><td><samp>Eyfa</samp></td></tr></tbody>
</table>