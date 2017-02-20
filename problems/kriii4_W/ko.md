시간이 많은 그는 제비 뽑기를 계속하고 있다. 그냥 아무것도 없이 하다 보니 재미가 없어서 제비를 뽑고 난 후에 어떤 제비를 뽑았는지 에 따라 지켜야 하는 규칙을 만들어 신선한 제비 뽑기를 하려고 한다.

그는 지금 끝을 빨간색으로 칠한 제비를 <span class="tex-span"><i>R</i>&thinsp;</span>개, 초록색은 <span class="tex-span"><i>G</i>&thinsp;</span>개, 파란색은 <span class="tex-span"><i>B</i>&thinsp;</span>개를 만들었다. 이 제비들을 모두 색칠한 쪽이 보이지 않게 통에 넣고 잘 섞은 다음에 제비를 하나씩 뽑을 것이다. 그는 제비를 매우 잘 섞기 때문에 모든 제비는 뽑힐 확률이 동일해진다. 뽑은 제비의 색에 따라 다음과 같은 일을 한다.

1. 빨간 제비를 뽑은 경우에는 뽑은 제비를 쓰레기통에 버린다.
2. 초록 제비를 뽑은 경우에는 뽑은 제비를 다시 통에 넣고 제비들을 잘 섞는다.
3. 파란 제비를 뽑은 경우에는 뽑은 제비를 다시 통에 넣고 제비들을 잘 섞는다. 만약 파란 제비를 뽑은 횟수가 <span class="tex-span"><i>K</i>&thinsp;</span>번이 되면 제비 뽑기를 그만 두고 잠이나 자러 가도록 한다.

그가 잠을 자러 갈 때까지 뽑게 되는 제비 개수의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 테스트 케이스의 개수 <span class="tex-span"><i>T</i>(1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;10<sup class="upper-index">3</sup>)</span>가 주어진다.
각 테스트 케이스의 첫 번째 줄에는 그가 가진 빨간 제비의 개수 <span class="tex-span"><i>R</i></span>, 초록 제비의 개수 <span class="tex-span"><i>G</i></span>, 파란 제비의 개수 <span class="tex-span"><i>B</i></span>, 파란 제비를 몇 번 뽑아야 잠을 자러 가게 되는지를 나타내는 <span class="tex-span"><i>K</i>&thinsp;</span>가 공백으로 구분되어 주어진다. 각 수는 모두 1이상의 자연수이다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-9 col-md-9 col-lg-9">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center>입력되는 수의 범위</center></th>
  <th class="col-sm-7 col-md-7 col-lg-7"><center>추가 제한</center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>6</center></td>
  <td><center><span class="tex-span">1</span>이상 <span class="tex-span">10<sup class="upper-index">3</sup></span>이하</center></td>
  <td><center>모든 테스트 케이스에 대해 <span class="tex-span"><i>R, G, B</i></span>값이 동일</center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>94</center></td>
  <td><center><span class="tex-span">1</span>이상 <span class="tex-span">10<sup class="upper-index">9</sup></span>이하</center></td>
  <td><center>없음</center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
각 테스트 케이스마다 한 줄에 그가 잠을 자러 갈 때까지 뽑게 되는 제비 개수의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>4<br>1 1 1 1<br>1 2 3 4<br>1000 1000 1 1000<br>50000 50000 50000 10000000</samp></td><td><samp>500000006<br>569010428<br>490804548<br>595034885</samp></td></tr>
		<tr><td><samp>4<br>9 9 9 1<br>9 9 9 2<br>9 9 9 4<br>9 9 9 1000</samp></td><td><samp>300000005<br>470000009<br>700700016<br>814176661<br></samp></td></tr>
    </tbody>
</table>

첫 번째 입력은 1번 부분 문제에 속하지 않음에 유의하라.

첫 번째 입력의 첫 번째 테스트 케이스의 답은 <span class="tex-span">5/2</span>를 나타낸다.

두 번째 입력은 1번 부분 문제에 속한다.
