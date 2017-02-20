그는 새로운 전략 카드 게임에 입문했다. 이 게임에서 카드를 구입할 때는 카드가 정확히 하나 들어 있는 카드 팩을 사야한다. 카드 팩 안의 내용물은 뜯어보기 전까지는 알 수 없고 게임에 있는 <span class="tex-span"><i>N</i>&thinsp;</span>종류의 카드 중 하나가 들어 있으며 모든 카드는 뽑힐 확률이 동일하다.

카드를 모은다고 끝나는 것이 아니라 덱을 구성해야 한다. 카드에 <span class="tex-span">1&thinsp;</span>번에서 <span class="tex-span"><i>N</i>&thinsp;</span>번까지의 번호를 붙이면, 그가 원하는 덱들을 구성하기 위해서는 <span class="tex-span"><i>i</i>&thinsp;</span>번 카드가 적어도 <span class="tex-span"><i>D<sub class="lower-index">i</sub></i>&thinsp;</span>장은 필요하다. 그러므로 그의 목표는 각 카드 <span class="tex-span"><i>i</i>&thinsp;</span>에 대해 <span class="tex-span"><i>D<sub class="lower-index">i</sub></i>&thinsp;</span>개 이상의 카드를 모으는 것이다.

하지만 현실은 그다지 녹록치 않다. 카드 팩은 돈을 주고 사야하고 그가 가진 돈은 적기 때문이다. 결국 그는 카드 팩을 <span class="tex-span"><i>L</i>&thinsp;</span>개만 구매하기로 했다. 그가 그의 목표를 달성할 확률을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 카드의 종류, 사려고 하는 카드 팩의 수를 나타내는 두 자연수 <span class="tex-span"><i>N</i>,&thinsp;<i>L</i>&thinsp;</span>이 공백으로 구분되어 주어진다.

두 번째 줄에는 각 카드마다 모아야 하는 개수를 나타내는 <span class="tex-span"><i>N</i>&thinsp;</span>개의 정수 <span class="tex-span"><i>D</i><sub class="lower-index">1</sub>,&thinsp;,&thinsp;…,&thinsp;<i>D<sub class="lower-index">N</sub></i>&thinsp;</span>이 공백으로 구분되어 주어진다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-8 col-md-8 col-lg-8">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center>각 <span class="tex-span"><i>D<sub class="lower-index">i</sub></i></span></center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>L</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>13</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;3,000</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>D<sub class="lower-index">i</sub></i>&thinsp;&le;&thinsp;1</span></center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i>&thinsp;&le;&thinsp;3,000</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>87</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;3,000</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>D<sub class="lower-index">i</sub></i>&thinsp;&le;&thinsp;10</span></center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i>&thinsp;&le;&thinsp;3,000</span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
그가 목표를 달성할 확률을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

<br>

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예제</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예제</th>
		</tr>
	</thead>
	<tbody>
		<tr><td><samp>1 1<br>1</samp></td><td><samp>1</samp></td></tr>
		<tr><td><samp>3 8<br>3 3 3</samp></td><td><samp>0</samp></td></tr>
		<tr><td><samp>2 2<br>1 1</samp></td><td><samp>500000004</samp></td></tr>
		<tr><td><samp>10 30<br>0 0 1 1 1 1 1 3 8 9</samp></td><td><samp>34678654</samp></td></tr>
    </tbody>
</table>

세 번째 예제의 답은 <span class="tex-span">1/2</span>를 의미한다.