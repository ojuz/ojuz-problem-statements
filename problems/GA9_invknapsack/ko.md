<style type="text/css">
.tex-span {
    font-size: 125%;
    font-family: times new roman;
}
.tex-formula {
    vertical-align: middle;
    margin: 0;
    border:medium none;
    position: relative;
    bottom: 2px;
}
</style>

문제를 출제하는 과정 중에서 중요한 축 중 하나가 바로 데이터를 만드는 일입니다. 데이터를 만드는 일반적인 방법 같은 것은 없고, 문제에 따라 발생할 수 있는 모든 오답들을 최대한 생각해보고 이들에 대비한 데이터를 만들어야 합니다.

예를 들어 아래와 같은 유명한 문제를 생각해 봅시다.

<div style="text-align:center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_invknapsack/ques.png" class="thumbnail">
</div>

저는 이 문제에서 발생할 수 있는 다양한 오답들을 떠올리다가, 답이 정확히 <span class="tex-span"><i>t</i></span>인 데이터에서 <span class="tex-span"><i>t</i>&thinsp;-&thinsp;1</span>을 출력하는 답안을 생각해냈습니다. 이러한 답안을 걸러주는 데이터를 마련하기 위해, 저는 어떤 자연수 <span class="tex-span"><i>t</i></span>가 주어졌을 때, 위 문제의 답이 <span class="tex-span"><i>t</i></span>가 되도록 하는 집합 <span class="tex-span"><i>S</i></span>와 자연수 <span class="tex-span"><i>k</i></span>를 구해주는 프로그램이 필요합니다.

하지만 저는 그 능력이 부족한 관계로, 여러분이 대신 프로그램을 작성해주셔야 합니다.

### 입력 형식

첫 번째 줄에 자연수 <span class="tex-span"><i>t</i></span>가 주어집니다.

### 출력 형식

첫 번째 줄에 <span class="tex-span"><i>n</i></span>과 <span class="tex-span"><i>k</i></span>를 공백을 사이로 두고 출력합니다. 두 번째 줄에 <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>,&thinsp;<i>a</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>a</i><sub class="lower-index"><i>n</i></sub></span>을 공백을 사이로 두고 출력합니다.

모든 변수의 이름과 제약 조건은 위 그림에 나타낸 문제와 같습니다. 출력한 데이터는 반드시 이 조건을 충족해야 합니다.

### 제약 조건

* <span class="tex-span">1 &le; <i>t</i> &le; 10<sup class="upper-index">18</sup></span>

### 부분문제

<div class="row">
<div class="col-lg-4 col-md-8 col-sm-12">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-4 col-md-4 col-lg-4">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-4 col-md-4 col-lg-4"><span class="tex-span"><i>t</i></span></th>
</tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>5</td>
  <td><span class="tex-span">&le; 300</span></td>
</tr>
 <tr>
  <td>2</td>
  <td>13</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">4</sup></span></td>
</tr>
 <tr>
  <td>3</td>
  <td>17</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">5</sup></span></td>
</tr>
 <tr>
  <td>4</td>
  <td>29</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
</tr>
 <tr>
  <td>5</td>
  <td>36</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">18</sup></span></td>
</tr>
</tbody>
</table>
</div>

</div>
</div>

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>1</samp></td><td><samp>4 13<br>1 2 4 8</samp></td></tr><tr><td><samp>3</samp></td><td><samp>4 3<br>1 1 2 3</samp></td></tr><tr><td><samp>17</samp></td><td><samp>10 12<br>1 2 3 4 5 6 7 8 9 5</samp></td></tr></tbody>
</table>