나나는 드넓은 초원에 놀러가서, 어린이들이 뛰노는 것을 즐겁게 바라보고 있습니다.

하지만 곧 눈이 온다는 예보가 있기 때문에, 멀리 보이는 나무까지 최대한 빨리 가고 싶습니다.

최근에도 눈이 왔었기 때문에, 초원의 곳곳에는 원형의 빙판이 존재합니다. 이 빙판은 지나갈 수 없습니다. 대신 빙판의 테두리는 거쳐서 갈 수 있습니다. 또한, 빙판들은 서로 겹치거나 테두리가 닿아있지 않다고 합니다.

나나는 빙판이 아닌 모든 곳에서 1의 속력으로 움직입니다. 시작 위치는 항상 (0, 0), 나무의 위치는 항상 (100, 100) 입니다. 나나는 현재 위치에서 나무가 있는 위치로 가는 가장 빠른 길을 찾고 싶습니다.

### 입력 형식

첫 번째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;100</span>)가 주어집니다.

각 테스트 케이스의 첫째 줄에는 빙판의 수 <span class="tex-span"><i>N</i></span>가 주어집니다. 다음 <span class="tex-span"><i>T</i></span>줄에는 빙판의 정보를 나타내는 세 정수  <span class="tex-span"><i>X</i><sub class="lower_index"><i>i</i></sub></span>, <span class="tex-span"><i>Y</i><sub class="lower_index"><i>i</i></sub></span>, <span class="tex-span"><i>R</i><sub class="lower_index"><i>i</i></sub></span>가 주어집니다. 이는 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>)</span> 를 중심으로 하는 반지름이 <span class="tex-span"><i>R</i><sub class="lower_index"><i>i</i></sub></span>인 빙판을 나타냅니다. 

빙판의 반지름은 1 이상입니다. 빙판들은 서로 겹치거나 접촉하지 않으며, (0, 0)-(100, 0)-(100, 100)-(0, 100)-(0, 0)으로 돌아오는 박스를 벗어나지 않습니다. 이 조건에 따라서, 빙판은 시작 위치와 나무의 위치도 포함하거나 접촉하고 있지 않음을 확인해주세요.

### 출력 형식

각 줄에 시작 위치에서 나무의 위치로 가는데 필요한 최소 시간을 출력해야 합니다. 정답과의 상대 오차 또는 절대 오차가 <span class="tex-span">10<sup>-6</sup></span> 이하여야 합니다.

### 파일 정보


<div class="row">
<div class="col-sm-12 col-md-10 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">입력 파일명</th>
  <th class="col-sm-3 col-md-3 col-lg-3">출력 파일명</th>
  <th class="col-sm-3 col-md-3 col-lg-3">점수</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><span class="tex-span"><i>N</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>D1.in</samp></td>
  <td><samp>D1.out</samp></td>
  <td>21</td>
  <td><span class="tex-span">= 1</span></td>
 </tr>
 <tr>
  <td><samp>D2.in</samp></td>
  <td><samp>D2.out</samp></td>
  <td>79</td>
  <td><span class="tex-span">&le; 100</span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 답안 생성 및 제출 방법

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_D/d_input.zip)에서 입력 파일을 내려받아, 위 표에 따라 출력 파일을 만듭니다. 제출하는 방법은 두 가지가 있습니다.

* 모든 출력 파일을 하나의 zip 파일에 압축하여 제출합니다. 다른 폴더 안에 출력 파일을 넣고 압축하는 등의 행위를 할 시 업로드 공격으로 의심되어 업로드가 즉시 차단됩니다.
* 각 출력 파일을 하나씩 업로드하여 제출합니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>2<br>1<br>50 50 20<br>2<br>20 50 20<br>99 90 1</samp></td><td><samp>147.116861750967<br>141.421356237310</samp></td></tr>
    </tbody>
</table>

2번 예제를 그리면 아래와 같습니다.

<a class="thumbnail">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_D/ex2.png" class="img-responsive">
</a>