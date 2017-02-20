길이가 <span class="tex-span"><i>N</i></span>인 문자열 중에서 문자열을 구성하는 문자의 종류가 <span class="tex-span"><i>M</i></span>가지 이하인 것들의 접미사 배열을 구할 때, 서로 다른 접미사 배열의 개수는 몇 개인가?

### 입력

첫 번째 줄에 두 자연수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span>(<span class="tex-span">1 &le; <i>N</i>, <i>M</i> &le; 10<sup class="upper-index">6</sup></span>)이 공백으로 구분되어 주어진다.

### 출력

길이가 <span class="tex-span"><i>N</i></span>인 문자열 중에서 문자열을 구성하는 문자의 종류가 <span class="tex-span"><i>M</i></span>가지 이하인 문자열들의 접미사 배열의 종류의 개수를 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력한다.

### 참고

접미사 배열의 정의는 [여기](https://ko.wikipedia.org/wiki/%EC%A0%91%EB%AF%B8%EC%82%AC_%EB%B0%B0%EC%97%B4)에서 확인할 수 있다.

두 배열 <span class="tex-span"><i>A</i></span>와 <span class="tex-span"><i>B</i></span>가 서로 다르다는 것은, <span class="tex-span"><i>A</i>[<i>i</i>] &ne; <i>B</i>[<i>i</i>]</span>를 만족하는 정수 <span class="tex-span"><i>i</i></span>가 적어도 하나 존재한다는 것이다.

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-3 col-md-3 col-lg-3">점수</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>N</i></span></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>M</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>10</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>36</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">6</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">6</sup></span></td>
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
	
	<tr><td><samp>4 2</samp></td><td><samp>12</samp></td></tr></tbody>
</table>

* [1, 2, 3, 4]: "aaab"
* [1, 2, 4, 3]: "aabb"
* [1, 4, 3, 2]: "abbb"
* [2, 3, 4, 1]: "baab"
* [2, 4, 1, 3]: "babb"
* [3, 1, 4, 2]: "abab"
* [3, 4, 2, 1]: "bbab"
* [4, 1, 2, 3]: "aaba"
* [4, 1, 3, 2]: "abba"
* [4, 2, 3, 1]: "baba"
* [4, 3, 1, 2]: "abaa"
* [4, 3, 2, 1]: "aaaa", "baaa", "bbaa", "bbba", "bbbb"