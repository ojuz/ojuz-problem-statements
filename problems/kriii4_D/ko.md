악수는 두 사람이 각자 한 손을 마주 내어 잡고 서로 반가움을 표하며 결속을 다지는 매우 뜻깊은 일이다.

그는 자신을 포함하여 <span class="tex-span"><i>N</i></span>명이 참석하는 파티를 주최했다. 그는 파티의 재미를 위해 모든 참가자들이 이미 알고 있던 사람이 한 명도 없도록 참가자들을 무작위로 모집했으나, 그의 예상과는 달리 얼어붙은 분위기는 잘 깨지지 않았다. 그는 어떻게 하면 자신이 원하던 즐거운 파티를 이끌어낼 수 있을지 고심하다가 이것은 서로가 서로를 잘 알지 못하기 때문이라는 결론을 내리고, 먼저 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_D/ca0f7b6b05b9e74fd6da34bc396013043f21be9c.png">가지의 모든 사람 쌍에 대해 악수를 한 번씩 하는 행사를 하여 서로의 친목을 다지기로 했다. 

그는 매우 독특한 사람이라, 어떤 두 사람 A, B가 악수를 하면 그 즉시 A와 B는 서로 아는 사람이 된다고 생각한다. 거기까지는 이해할 수 있을지 모르지만, 그는 A가 알고 있던 사람들과 B가 알고 있던 사람들 역시 서로 아는 사람이 된다고 생각한다. 예를 들어, 4명의 사람 P, Q, R, S가 참여한 파티에서 P와 Q, R과 S끼리 이미 악수를 해서 서로 아는 사람일 때 P와 R이 악수를 한다면, P와 R, P와 S, Q와 R, Q와 S 모두 서로 아는 사람이 된다. 이는 실제와는 매우 동떨어진 생각이지만 어쨌든 그는 그렇게 생각한다.

악수 행사를 진행할 때는 아직까지 악수를 하지 않은 사람 쌍들 중 하나를 동일한 확률로 무작위로 하나 골라 진행한다고 할 때, 그의 생각 상에서 모든 사람이 서로를 알게 되는 악수는 몇 번째가 될 것인지 그 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 사람의 수를 나타내는 자연수 <span class="tex-span"><i>N</i>&thinsp;</span>이 주어진다.

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
  <td><center>5</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;5</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>95</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;40</span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력
모든 사람이 서로를 알게 되는 악수는 몇 번째가 될 것인지 그 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>1</samp></td><td><samp>0</samp></td></tr>
		<tr><td><samp>2</samp></td><td><samp>1</samp></td></tr>
		<tr><td><samp>3</samp></td><td><samp>2</samp></td></tr>
    </tbody>
</table>
