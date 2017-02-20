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

승현이는 <span class="tex-span">1&thinsp;&times;&thinsp;<i>n</i></span> 크기의 격자판을 가지고 있습니다. 각 칸에는 <span class="tex-span">1</span> 이상 <span class="tex-span"><i>n</i></span> 이하의 자연수 번호가 왼쪽에서부터 차례대로 붙어있습니다. 이 중 <span class="tex-span"><i>k</i></span>개의 칸에는 말이 하나씩 놓여 있는데, 이 말들은 격자들을 좋아해서, 도달 가능한 모든 격자판을 방문합니다. 말들이 자신의 격자판을 더럽히는 것을 보고만 있을 수 없었던 승현이는 <span class="tex-span"><i>d</i></span>개의 칸막이를 구매했습니다. 각 칸막이는 인접한 두 격자가 만나는 선분 위에 놓을 수 있으며, 말들은 칸막이를 지나갈 수 없습니다.

<center>
<div class="row">
<a class="thumbnail">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_preserve/img1.png">
</a>
</div>
</center>

위 그림에서, 지금 5번 격자에 있는 말은 3번, 4번, 5번 격자를 모두 방문하고, 8번 격자에 있는 말은 6번, 7번, 8번 격자를 모두 방문합니다. 보존되는 격자는 1번 격자와 2번 격자뿐입니다.

승현이는 <span class="tex-span"><i>d</i></span>개의 칸막이들을 적절히 배치하여 어떤 말도 방문하지 않은 격자의 수를 최대화하려고 합니다. 하지만 그 방법은 잘 모르겠다고 합니다. 승현이를 도와 보존할 수 있는 최대 격자의 수를 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 격자판의 크기 <span class="tex-span"><i>n</i></span>, 말의 수 <span class="tex-span"><i>k</i></span>, 칸막이의 수 <span class="tex-span"><i>d</i></span>가 공백을 사이로 두고 주어집니다.

두 번째 줄에는 <span class="tex-span"><i>k</i></span>개의 정수 <span class="tex-span"><i>p</i><sub class="lower-index">1</sub>,&thinsp;<i>p</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>p</i><sub class="lower-index"><i>k</i></sub></span>가 공백을 사이로 두고 주어집니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>k</i></span>)번째 정수 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>는 <span class="tex-span"><i>i</i></span>번 말이 위치한 칸의 번호를 나타냅니다.

### 출력 형식

승현이가 <span class="tex-span"><i>d</i></span>개의 칸막이들을 잘 설치하여 보존할 수 있는 격자의 수의 최댓값을 출력합니다.

### 제약 조건

* <span class="tex-span">2&thinsp;&le;&thinsp;<i>n</i>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>min</i>(10<sup class="upper-index">5</sup>,&thinsp;<i>n</i>)</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>d</i>&thinsp;&le;&thinsp;<i>n</i>&thinsp;-&thinsp;1</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>p</i><sub class="lower-index">1</sub>&thinsp;&lt;&thinsp;<i>p</i><sub class="lower-index">2</sub>&thinsp;&lt;&thinsp;...&thinsp;&lt;&thinsp;<i>p</i><sub class="lower-index"><i>k</i>&thinsp;-&thinsp;1</sub>&thinsp;&lt;&thinsp;<i>p</i><sub class="lower-index"><i>k</i></sub>&thinsp;&le;&thinsp;<i>n</i></span>

### 부분문제

<div class="row">
<div class="col-lg-6 col-md-9 col-sm-12">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-2 col-md-2 col-lg-2">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>n</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>k</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>d</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>9</td>
  <td><span class="tex-span">&le; 20</span></td>
  <td><span class="tex-span">&le;&thinsp;<i>n</i>&thinsp;</span></td>
  <td><span class="tex-span">&le;&thinsp;<i>n</i>&thinsp;-&thinsp;1</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>17</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">5</sup></span></td>
  <td><span class="tex-span">= 3</span></td>
  <td><span class="tex-span">= 3</span></td>
 </tr>
 <tr>
  <td>3</td>
  <td>22</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">6</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">2</sup></span></td>
 </tr>
 <tr>
  <td>4</td>
  <td>17</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">5</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">3</sup></span></td>
 </tr>
 <tr>
  <td>5</td>
  <td>35</td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">5</sup></span></td>
  <td><span class="tex-span">&le;&thinsp;<i>n</i>&thinsp;-&thinsp;1</span></td>
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
	
	<tr><td><samp>15 4 3<br>3 5 10 11</samp></td><td><samp>8</samp></td></tr></tbody>
</table>