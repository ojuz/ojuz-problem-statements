그는 요즘 여러 능력을 가지고 몬스터들과 싸우는 웹게임을 열심히 하고 있다. 그는 지금 <span class="tex-span"><i>N</i></span>개의 공격 능력을 가지고 있고 이 모든 능력을 장착하고 있다. 그는 능력들을 편하게 관리하고자 각 능력에 1 이상 <span class="tex-span"><i>N</i></span> 이하의 자연수 번호를 붙였다. 

<span class="tex-span"><i>i</i></span>번 능력에는 그 능력이 발동될 확률 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>와 상대에게 입히는 피해량 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>가 책정되어 있다. 따라서 그가 <span class="tex-span"><i>i</i></span>번 능력에 발동 명령을 내리면, <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>의 확률로 능력이 발동되어 상대에게 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>만큼의 피해를 입히고, <span class="tex-span">(1&thinsp;-&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>)</span>의 확률로 능력이 발동되지 않아 아무 일도 일어나지 않는다. 그가 어떤 능력(들)을 장착한 채로 상대방을 공격할 기회를 얻었다면, 아래 과정이 일어난다:

- 가지고 있는 모든 능력들 중 하나를 임의로 고른다. 모든 능력을 고를 확률은 서로 같다. 고른 능력에 발동 명령을 내린다. 만약 이 능력이 발동되었다면, 공격 기회를 잃고 과정이 끝난다. 하지만 이 능력이 발동되지 않았다면, 아직 발동 명령을 내려 보지 않은 능력들 중 하나를 동일한 확률로 고른 후, 다시 발동 명령을 내린다. 만약 능력이 발동되었다면 공격 기회를 잃은 후 과정을 끝내고, 발동되지 않았다면 같은 과정을 더 이상 발동 명령을 내려 보지 않은 능력이 없을 때까지 반복한다. 모든 능력에 발동 명령을 내렸음에도 발동된 능력이 하나도 없으면 공격 기회를 잃는다.

현재 그가 장착하고 있는 <span class="tex-span"><i>N</i></span>개의 능력이 발동될 확률과 상대에게 입히는 피해량이 주어질 때, 한 번의 공격 기회에서 주게 되는 피해량의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에 능력의 수를 나타내는 자연수 <span class="tex-span"><i>N</i></span>이 주어진다.

다음 <span class="tex-span"><i>N</i></span>개의 줄에는 능력들의 정보가 주어진다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 <span class="tex-span"><i>i</i></span>번 능력이 발동될 확률과 상대에게 입히는 피해량을 의미하는 두 정수 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>d</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span>)이 공백을 사이로 두고 주어진다. 이는 <span class="tex-span"><i>i</i></span>번 능력은 <span class="tex-span">&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>&thinsp;/&thinsp;10<sup class="upper-index">9</sup></span>의 확률로 발동하는 능력이며 상대에게 <span class="tex-span"><i>d</i><sub class="lower-index"><i>i</i></sub></span>만큼의 피해를 입힌다는 의미이다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-4 col-md-4 col-lg-4">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>10</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;200</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>90</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;5,000</span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

그가 한 번의 공격 기회에서 주게 되는 피해량의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>1<br>500000000 10</samp></td><td><samp>5</samp></td></tr>
		<tr><td><samp>9<br>1 9<br>2 8<br>3 7<br>4 6<br>5 5<br>6 4<br>7 3<br>8 2<br>9 1</samp></td><td><samp>93531355</samp></td></tr>
    </tbody>
</table>
