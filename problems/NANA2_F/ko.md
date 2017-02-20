심심한 나나는 누구나 즐길 수 있는, <span class="tex-span"><i>n</i>&thinsp;&times;&thinsp;1</span> 크기, 즉 단위 격자 <span class="tex-span"><i>n</i></span>개가 일렬로 놓여 있는 격자판에서 하는 퍼즐 게임을 생각해 냈습니다. 격자들에는 <span class="tex-span"><i>n</i></span> 이하의 자연수 번호가 왼쪽 끝에서부터 차례대로 붙어있습니다. <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>n</i></span>)번째 격자에는 색이 <span class="tex-span"><i>b</i><sub class="lower-index"><i>i</i></sub></span>인 블록이 하나 놓여 있습니다. 격자판 아래에는 "대기열"이라고 불리는 격자판과 별개인 공간이 있는데, 여기에는 <span class="tex-span"><i>m</i></span>개의 블록들이 일렬로 놓여 있으며, 이 중 <span class="tex-span"><i>j</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>m</i></span>)번째 블록의 색은 <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span>입니다. 블록의 색들은 1 이상 <span class="tex-span"><i>c</i></span> 이하의 자연수로 표현할 수 있습니다. (즉 블록에 칠해져 있는 색의 종류는 <span class="tex-span"><i>c</i></span>가지입니다.)

여러분은 격자판에서 색이 같은 연속한 블록들을 선택하여 제거할 수 있습니다. 블록은 왼쪽에서부터 차례대로 제거되며, 격자에서 블록을 제거할 때마다 대기열의 맨 앞에 있는 블록이 그 격자 속으로 들어가게 됩니다.

이 게임의 목적은 블록들을 적절히 제거하여, 대기열에 있는 모든 블록을 없애는 것입니다. 물론 제거 작업을 무한히 할 수 있다면 게임이 너무 쉬워지므로, 제거 작업은 최대 <span class="tex-span"><i>t</i></span>번까지만 할 수 있습니다. 만약 <span class="tex-span"><i>t</i></span>번 안에 대기열의 모든 블록들을 소모하지 못했다면 부분 점수만을 얻게 되고, <span class="tex-span"><i>t</i></span>번 미만의 제거 작업으로 대기열의 모든 블록들을 소모했다면 추가 점수를 얻게 됩니다. 단, 대기열에 블록들이 없는데도 격자판의 블록을 제거하면 안 됩니다.

### 입력 형식

첫 번째 줄에는 격자의 수 <span class="tex-span"><i>n</i></span>과 색의 종류의 수 <span class="tex-span"><i>c</i></span>가 공백을 사이로 두고 주어집니다.

두 번째 줄에는 격자판 안에 있는 블록들의 색을 나타내는 <span class="tex-span"><i>n</i></span>개의 자연수 <span class="tex-span"><i>b</i><sub class="lower-index">1</sub>,&thinsp;<i>b</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>b</i><sub class="lower-index"><i>n</i></sub></span>이 공백을 사이로 두고 주어집니다.

세 번째 줄에는 대기열에 있는 블록의 수 <span class="tex-span"><i>m</i></span>과 제거 작업의 최대 횟수 <span class="tex-span"><i>t</i></span>가 주어집니다.

네 번째 줄에는 대기열에 있는 블록들의 색을 나타내는 <span class="tex-span"><i>m</i></span>개의 자연수 <span class="tex-span"><i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>s</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>s</i><sub class="lower-index"><i>m</i></sub></span>이 공백을 사이로 두고 주어집니다. 앞에 있는 블록 (즉, 번호가 작은 블록)이 먼저 사용됩니다.

### 출력 형식

첫 번째 줄에는 사용한 제거 작업의 횟수 <span class="tex-span"><i>u</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>u</i>&thinsp;&le;&thinsp;<i>t</i></span>)를 출력합니다.

이후 <span class="tex-span"><i>u</i></span>개의 줄을 출력하는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>u</i></span>)번째 줄에는 두 개의 자연수 <span class="tex-span"><i>L</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>R</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>R</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>n</i></span>)를 공백을 사이로 두고 출력합니다. 이는 <span class="tex-span"><i>i</i></span>번째 제거 작업에서 <span class="tex-span"><i>L</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>L</i><sub class="lower-index"><i>i</i></sub>&thinsp;+&thinsp;1,&thinsp;...,&thinsp;<i>R</i><sub class="lower-index"><i>i</i></sub>&thinsp;-&thinsp;1,&thinsp;<i>R</i><sub class="lower-index"><i>i</i></sub></span>번 블록을 제거했다는 것을 의미합니다.

### 파일 정보

각 입력의 파라미터는 다음과 같습니다. 게임 보드와 대기열은 주어진 파라미터를 이용하여 랜덤하게 만들어졌습니다. 입력 파일은 [여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_F/f_input.zip)에서 내려받을 수 있습니다.

<div class="row">
<div class="col-sm-12 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">입력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">출력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>n</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>c</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>m</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>t</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>F1.in</samp></td>
  <td><samp>F1.out</samp></td>
  <td><span class="tex-span">10</span></td>
  <td><span class="tex-span">4</span></td>
  <td><span class="tex-span">1,000</span></td>
  <td><span class="tex-span">420</span></td>
 </tr>
 <tr>
  <td><samp>F2.in</samp></td>
  <td><samp>F2.out</samp></td>
  <td><span class="tex-span">20</span></td>
  <td><span class="tex-span">5</span></td>
  <td><span class="tex-span">3,000</span></td>
  <td><span class="tex-span">1,300</span></td>
 </tr>
 <tr>
  <td><samp>F3.in</samp></td>
  <td><samp>F3.out</samp></td>
  <td><span class="tex-span">30</span></td>
  <td><span class="tex-span">5</span></td>
  <td><span class="tex-span">10,000</span></td>
  <td><span class="tex-span">4,320</span></td>
 </tr>
 <tr>
  <td><samp>F4.in</samp></td>
  <td><samp>F4.out</samp></td>
  <td><span class="tex-span">40</span></td>
  <td><span class="tex-span">6</span></td>
  <td><span class="tex-span">10,000</span></td>
  <td><span class="tex-span">4,490</span></td>
 </tr>
 <tr>
  <td><samp>F5.in</samp></td>
  <td><samp>F5.out</samp></td>
  <td><span class="tex-span">50</span></td>
  <td><span class="tex-span">6</span></td>
  <td><span class="tex-span">10,000</span></td>
  <td><span class="tex-span">4,440</span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 채점 방식

각 출력 파일에 대한 여러분의 점수는 아래와 같이 계산됩니다.

* 만약 여러분의 계획이 문제에서 제시한 조건을 만족하지 않는다면 0점입니다.
* 만약 여러분의 계획이 문제에서 제시한 조건을 만족한다면, 다음과 같이 점수가 계산됩니다. 여러분이 사용한 제거 작업의 횟수를 <span class="tex-span"><i>u</i></span>, 대기열에서 제거한 블록의 수를 <span class="tex-span"><i>w</i></span>로 둡시다.
  - <span class="tex-span"><i>w</i>&thinsp;=&thinsp;<i>m</i></span>이면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_F/36344855b06974a172fed161e16c2fd7ef9672b9.png"/>점. 
  - 그렇지 않으면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_F/a45a78fea8057bd1b43e7627afa7ea0c2968593b.png"/>점
  
제출한 답안의 점수는 각 출력 파일에서 받은 점수들의 합이 됩니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>10<br>4<br>1 2 2 3 3 3 4 4 4 4<br>8 2<br>3 1 2 3 4 3 2 1</samp></td><td><samp>2<br>7 10<br>4 7</samp></td></tr></tbody>
</table>

점수는 20점입니다.