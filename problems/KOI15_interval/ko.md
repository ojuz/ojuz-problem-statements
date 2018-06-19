매 초마다 신호를 발생시키는 두 장치 A, B가 있다. 이 신호는 알파벳 소문자의 서열로 표현된다. A, B로부터 발생한 신호를 서열로 표시한 S<sub>A</sub>, S<sub>B</sub>의 예는 다음과 같다.

 * S<sub>A</sub> = [a, f, c, d, r, d, e, s, d, c, f, w, s, z, r]
 * S<sub>B</sub> = [g, e, d, s, r, d, d, e, m, z, r]

신호 서열의 어떤 구간에 포함된 문자의 종류와 개수가 순서에 상관없이 동일하면 이 두 ‘구간의 성분’은 같다고 한다. 아래에서 박스로 표시된 부분은 두 신호 S<sub>A</sub>, S<sub>B</sub>에서 성분이 같은 구간을 나타내고 있다.

 * a f c **[d r d e s d e]** f w s z r
 * g **[e d s r d d e]** m z r

즉 위의 예와 같이 성분이 같은 구간의 길이는 두 서열에서 반드시 같아야 한다. 그리고 같은 성분의 구간은 하나 이상 존재할 수 있다. 우리는 두 신호 서열에 각각 존재하는 같은 성분 구간 중에서 가장 긴 것을 찾으려고 한다.

### 입력 형식
첫 두 줄에 신호 서열이 공백 없는 하나 의 문자열로 각각 주어진다. 이 문자열은 영문 소문자로만 구성되어 있다.

두 입력 문자열의 크기 N,M의 범위는 5 ≤ N,M ≤ 1,500이다.

### 출력 형식
두 서열에서 같은 성분을 가진 구간 중에서 가장 긴 구간을 찾아, 그 구간의 길이를 출력해야 한다.

### 부분문제의 제약 조건
 * **부분문제 1:** 전체 점수 100점 중 7점에 해당하며, N,M ≤ 100이다.
 * **부분문제 2:** 전체 점수 100점 중 23점에 해당하며, N,M ≤ 500이다.
 * **부분문제 3:** 전체 점수 100점 중 31점에 해당하며, N,M ≤ 1,000이다.
 * **부분문제 4:** 전체 점수 100점 중 39점에 해당하며, N,M ≤ 1,500이다.
 
### 입력과 출력의 예

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>xraphy<br>edgeedgem</samp></td><td><samp>0</samp></td></tr>
	<tr><td><samp>afcdrdesdefwszr<br>gedsrddemzr</samp></td><td><samp>7</samp></td></tr>
	<tr><td><samp>computersystem<br>sesystuercomplexity</samp></td><td><samp>11</samp></td></tr></tbody>
</table>
