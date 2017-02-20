
석환이는 "Lightballb"라는 상품을 판매합니다. Lightballb 한 세트에는 두 개의 같은 자연수 번호가 적혀 있는 공이 들어있습니다. 이 공은 평상시에는 공의 역할을 하다가, 같은 번호가 쓰여 있는 두 공을 전선으로 연결하면 전구의 역할을 한다고 합니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_wire/img1.png" class="thumbnail"/>
<small>(1) 같은 번호가 쓰여 있는 두 개의 공이 전선으로 연결되어 있으므로 전구가 켜집니다.<br>
(2) 한 공에 전선이 연결되어 있으므로 전구는 켜지지 않습니다.<br>
(3) 전선이 연결되어 있지 않으므로 전구는 켜지지 않습니다.<br>
(4) 서로 다른 번호가 쓰여 있는 두 개의 공이 전선으로 연결되어 있으므로 전구가 켜지지 않습니다.</small>
</center>

승현이는 석환이의 상품이 전혀 팔리지 않는다는 소식을 듣고, 석환이를 돕기 위해 <span class="tex-span"><i>n</i></span>개의 Lightballb 세트를 구매했습니다. 따라서 승현이는 <span class="tex-span">2<i>n</i></span>개의 공을 가지고 있으며, 1 이상 <span class="tex-span"><i>n</i></span> 이하의 모든 자연수 <span class="tex-span"><i>k</i></span>에 대해 <span class="tex-span"><i>k</i></span>가 적혀 있는 공은 정확히 2개입니다.

승현이는 방대한 공들을 보관할만한 장소를 찾다가, 아래와 같이 생긴 길쭉한 보관함을 찾고 그 안에 공을 무작위로 넣었습니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_wire/img2.png" class="thumbnail"/>
</center>

다음 날, 승현이는 공을 사용하기 위해 보관함에서 공을 꺼내려고 시도했지만, 공들은 꼼짝도 하지 않았습니다! 공이 반짝반짝 빛나는 모습을 보고 싶던 승현이는 절망감에 빠졌습니다. 낙담하고 있던 그 때, 승현이는 전선이 보관함을 뚫고 들어간다는 사실을 알아냈습니다! 승현이는 공들에 전선을 잘 꽂아 모든 공들이  빛나는 모습을 보고자 합니다.

무턱대고 전선을 끼우면 고장이 날 우려가 있기 때문에, 승현이는 미리 전선을 어떻게 연결할지에 대한 계획을 수립하려고 합니다. 우선, 승현이는 보관함과 전선이 움직이는 것을 방지하기 위해, 이들을 반드시 바닥 위에 놓기로 했습니다. 하지만, 이것만으로는 위험에 대비할 수 없다고 생각한 승현이는 다음과 같은 규칙을 세웁니다. 

1. 합선의 우려가 있으므로, 전선끼리 서로 교차하면 안 된다.
2. 한 전선의 모든 부분은 보관함의 위에 있거나 보관함의 아래에 있어야 한다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_wire/img3.png" class="thumbnail"/>
<small>위 3개의 그림 모두 보관함을 위에서 내려다본 모습을 나타낸 것입니다.<br>
(A)는 모든 규칙을 만족합니다.<br>
(B)는 2번 공을 잇는 전선과 3번 공을 잇는 전선이 교차하므로 1번 규칙을 만족하지 않습니다.<br>
(C)는 4번 공을 잇는 전선이 보관함의 위에 있기도 하면서 보관함의 아래에도 있기도 하므로(?) 2번 규칙을 만족하지 않습니다.</small>
</center>

승현이는 위 규칙을 만족하면서 전선을 연결하여 모든 공이 빛나도록 할 수 있는 방법이 존재하는지 알고자 합니다. 하지만 전구의 개수가 너무 많아 스스로 해결할 수 없었고, 여러분에게 도움을 요청했습니다. 승현이의 보관함에 적혀 있는 공의 번호가 차례대로 주어질 때, 각 공의 전선이 보관함 위에 있어야 하는지, 아래에 있어야 하는지를 결정하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 자연수 <span class="tex-span"><i>n</i></span>이 주어집니다.

두 번째 줄에 <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>,&thinsp;<i>a</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>a</i><sub class="lower-index">2<i>n</i>&thinsp;-&thinsp;1</sub>,&thinsp;<i>a</i><sub class="lower-index">2<i>n</i></sub></span>이 공백을 사이로 두고 차례대로 주어집니다. 여기서 <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>는 승현이의 보관함에서 왼쪽에서부터 <span class="tex-span"><i>i</i></span>번째에 위치한 공에 적혀 있는 번호를 나타냅니다.

### 출력 형식

만약 주어진 조건을 만족하면서 모든 공을 빛나게 하는 방법이 존재하지 않는다면, "<samp>IMPOSSIBLE</samp>" (따옴표 제외)를 출력합니다.

만약 방법이 존재한다면, 첫 번째 줄에 길이가 <span class="tex-span">2<i>n</i></span>인 문자열을 출력합니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;2<i>n</i></span>)번째 글자는, 왼쪽에서 <span class="tex-span"><i>i</i></span>번째에 위치한 공에 꽂는 전선이 보관함 위에 있어야 한다면 '<samp>^</samp>', 보관함 아래에 있어야 한다면 '<samp>v</samp>'이어야 합니다.

### 제약 조건

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>n</i>&thinsp;&le;&thinsp;300,&thinsp;000</span> 
* 모든 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;2<i>n</i></span>)에 대해, <span class="tex-span">1&thinsp;&le;&thinsp;<i>a</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>n</i></span>
* 모든 <span class="tex-span"><i>k</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>n</i></span>)에 대해, <span class="tex-span"><i>k</i></span>는 수열 <span class="tex-span"><i>a</i></span>에서 정확히 2번 나타납니다. 

### 부분문제

<div class="row">
<div class="col-lg-6 col-md-8 col-sm-12">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-4 col-md-4 col-lg-4">부분문제</th>
  <th class="col-sm-4 col-md-4 col-lg-4">점수</th>
  <th class="col-sm-4 col-md-4 col-lg-4"><span class="tex-span"><i>n</i></span></th>
</tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>9</td>
  <td><span class="tex-span">&le; 10</span></td>
</tr>
 <tr>
  <td>2</td>
  <td>15</td>
  <td><span class="tex-span">&le; 1,000</span></td>
</tr>
 <tr>
  <td>3</td>
  <td>37</td>
  <td><span class="tex-span">&le; 100,000</span></td>
</tr>
 <tr>
  <td>4</td>
  <td>39</td>
  <td><span class="tex-span">&le; 300,000</span></td>
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
	<tr><td><samp>4<br>1 2 3 2 3 1 4 4</samp></td><td><samp>^^v^v^vv</samp></td></tr>
	<tr><td><samp>3<br>1 2 3 3 2 1</samp></td><td><samp>^^^^^^</samp></td></tr><tr><td><samp>3<br>1 2 3 1 2 3</samp></td><td><samp>IMPOSSIBLE</samp></td></tr></tbody>
</table>

참고로, 맨 위의 예제는 그림 (A)와 같습니다.
