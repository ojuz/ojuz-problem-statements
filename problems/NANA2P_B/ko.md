3차원 세상에서 운영되는 나나택배에는 오늘도 많은 택배 물건들이 들어오고 있습니다. 물류비를 절약하기 위해, 나나는 고정된 크기의 트럭만을 운용합니다. 각 트럭 내에는 물건을 보관할 수 있는 <span class="tex-span">30&thinsp;&times;&thinsp;30&thinsp;&times;&thinsp;30</span> 크기의 정육면체 형태의 공간이 있습니다. 이 공간은 3차원 좌표계로 표현할 수 있으며, 공간의 한 꼭짓점은 원점이며, 정육면체의 변 중 세 개는 각각 <span class="tex-span"><i>x</i></span>축, <span class="tex-span"><i>y</i></span>축, <span class="tex-span"><i>z</i></span>축과 겹치며 좌표가 증가하는 방향으로 놓여 있습니다. 각 택배 박스는 직육면체 모양으로, 트럭 내의 공간에 넣을 때 공간의 벽면에 평행하기만 하다면 원하는 대로 회전하여 넣을 수 있습니다. 모든 택배 박스들의 부피의 합은 항상 <span class="tex-span">30&thinsp;&times;&thinsp;30&thinsp;&times;&thinsp;30&thinsp;=&thinsp;27,&thinsp;000</span>입니다.

만약 박스들을 트럭 내의 공간 안에 쌓는 것이 쉽지 않을 경우, 공간의 크기를 각 방향(<span class="tex-span"><i>x</i></span>축, <span class="tex-span"><i>y</i></span>축, <span class="tex-span"><i>z</i></span>축)으로 최대 1만큼 늘리는 것이 허용됩니다. 단 부피를 늘리는 데에는 비용이 들기 때문에, 크기를 한 방향에 대해서 1 늘릴 때마다 점수는 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2P_B/26b808893af1ddee7377b540816a50afeb3b4481.png"/>로 감소합니다.

### 입력 형식

첫째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i>&thinsp;=&thinsp;25</span>가 주어집니다.

각 테스트 케이스의 첫 줄에는 택배 상자의 개수 <span class="tex-span"><i>N</i></span>이 주어집니다. 다음 <span class="tex-span"><i>N</i></span>개의 줄에는 박스들의 정보가 주어지는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 <span class="tex-span"><i>i</i></span>번째 택배 상자의 크기를 나타내는 30 이하의 자연수 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>Z</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다.

### 출력 형식

각 테스트 케이스에 대해, 첫 번째 줄에는 트럭 내 택배 수납 공간의 크기를 나타내는 30 이상 31 이하의 자연수 세 개 <span class="tex-span"><i>TX</i></span>, <span class="tex-span"><i>TY</i></span>, <span class="tex-span"><i>TZ</i></span>를 공백을 사이로 두고 출력합니다. 단, 조건에 맞는 답을 찾지 못한 경우에는 한 줄에 "<samp>-1 -1 -1</samp>"만을 출력하고 이 테스트 케이스의 출력을 중단합니다.

만약 조건에 맞는 답을 찾았다면, <span class="tex-span"><i>N</i></span>개의 줄을 출력해야 하는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>n</i></span>)번째 줄에는 6개의 정수 <span class="tex-span"><i>sx</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>sy</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>sz</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>fx</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>fy</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>fz</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>sx</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>fx</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>TX</i>,&thinsp;0&thinsp;&le;&thinsp;<i>sy</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>fy</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>TY</i>,&thinsp;0&thinsp;&le;&thinsp;<i>sz</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>fz</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>TZ</i></span>) 를 출력합니다. 이는 <span class="tex-span"><i>i</i></span>번째 택배 박스가 차지하는 직육면체 공간의 상반된 위치에 놓인 두 꼭짓점을 나타냅니다. 임의의 두 택배 박스가 차지하는 공간은 서로 닿을 수 있지만 겹치면 안 됩니다. 출력하는 택배 박스의 순서는 입력받는 순서와 일치해야 합니다.

### 채점 방식

각 테스트 케이스에 대해 아래와 같이 점수가 부여됩니다.

<div class="row">
<div class="col-lg-4 col-md-6 col-sm-10">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-6 col-md-6 col-lg-6"><span class="tex-span"><i>TX</i>&thinsp;+&thinsp;<i>TY</i>&thinsp;+&thinsp;<i>TZ</i></span></th>
  <th class="col-sm-6 col-md-6 col-lg-6">점수</th>
</tr>
</thead>
<tbody>
 <tr>
  <td>90</td>
  <td>4</td>
</tr>
 <tr>
  <td>91</td>
  <td>1</td>
</tr>
 <tr>
  <td>92</td>
  <td>0.25</td>
</tr>
 <tr>
  <td>93</td>
  <td>0.0625</td>
</tr>
</tbody>
</table>
</div>

</div>
</div>

### 제출 방법

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2P_B/B.in)에 주어진 입력 파일을 내려받습니다. 이 입력 파일에 대한 출력 파일을 제출하면 됩니다. 파일을 압축해서 제출하시려면, 출력 파일명을 `B.out`로 두신 후 압축하셔야 합니다.

<!--
### 입력 형식

첫째 줄에 테스트 케이스의 수 $T = 25$ 가 주어집니다.

각 테스트 케이스의 첫 줄에는 택배 물건의 개수 $N$이 주어집니다. 그 다음 줄부터 각 줄에는 30 이하의 자연수인 $X_i, Y_i, Z_i$의 숫자 세 개가 들어오며 각각의 택배 박스의 크기를 나타냅니다.

### 출력 형식

각 테스트 케이스에 대해서 첫 줄에는 공간의 크기를 30 이상 31 이하의 자연수 세 개 $TX, TY, TZ$로 출력합니다. 조건에 맞는 답을 을 출력하고 다음 케이스로 넘어갑니다.

다음 줄부터 $N$줄에는 각 택배 박스가 차지하는 위치를 0 이상 $TX, TY, TZ$ 이하의 $sx_i, sy_i, sz_i, fx_i, fy_i, fz_i$의 6개로 출력합니다. $fx_i - sx_i = X_i, fy_i - sy_i = Y_i, fz_i - sz_i = Z_i$ 의 관계를 만족해야 하며, 각 택배 박스가 점유하는 공간은 서로 닿을 수는 있지만 겹쳐서는 안됩니다. 출력하는 택배 박스의 순서는 입력받는 순서와 일치해야 합니다.


각 테스트 케이스에 대해서 다음과 같이 점수가 부여됩니다.

$TX + TY + TZ = 90$ : 4점

$TX + TY + TZ = 91$ : 1점

$TX + TY + TZ = 92$ : 0.25점

$TX + TY + TZ = 93$ : 0.0625점


-->

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>3<br>4<br>15 15 30<br>15 15 30<br>15 30 15<br>30 15 15<br>1<br>30 30 30<br>8<br>29 29 29<br>29 29 1<br>29 29 1<br>29 29 1<br>1 1 29<br>1 1 29<br>1 1 29<br>1 1 1</samp></td><td><samp>30 30 30<br>0 0 0 15 30 15<br>15 0 0 30 30 15<br>15 0 15 30 30 30<br>0 0 15 15 0 30<br>-1 -1 -1<br>31 30 30<br>0 0 0 29 29 29<br>29 0 0 30 1 29<br>0 29 0 1 30 29<br>0 0 29 29 29 30<br>30 0 0 31 1 29<br>30 1 0 31 2 29<br>30 2 0 31 3 29<br>30 3 0 31 4 1</samp></td></tr></tbody>
</table>

각 테스트 케이스에 대해 4, 0, 1점을 받아서 총 점수는 5점입니다.