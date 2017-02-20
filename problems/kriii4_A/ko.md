목공을 시작한 그는 기본기를 쌓기 위해 나무 상자를 만드는 것을 반복하고자 한다. 나무 상자 하나는 <SPAN class="tex-span"><I>N</I></SPAN>개의 나무판자를 이어 붙여 만들 수 있다. 이렇게 만들어진 나무 상자는 어차피 공간만 차지하므로 다시 나무판자로 분해하여 새로운 나무 상자를 만들기 위해 사용한다. 나무 상자를 분해하여 새로 얻을 수 있는 온전한 나무판자의 수는 <SPAN class="tex-span"><I>N</I></SPAN>개보다 작으며(<SPAN class="tex-span"><I>N</I></SPAN>개 미만), 상자를 언제나 잘 분해할 수는 없기에 그는 확률적으로 나무판자를 얻게 된다. 모든 <SPAN class="tex-span">0&thinsp;&le;&thinsp;<I>i</I>&thinsp;&lt;&thinsp;<I>N</I></SPAN>에 대해 나무 상자를 분해하여 나무판자 <SPAN class="tex-span"><I>i</I></SPAN>개를 얻을 확률은 정수 <SPAN class="tex-span"><I>q</I><SUB class="lower-index"><I>i</I></SUB></SPAN>에 비례함이 알려져 있으며, <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_A/8a33559d809853de25983f2299b8d46da644864a.png">로 계산된다.

그는 현재 <SPAN class="tex-span"><I>M</I></SPAN>개의 나무판자를 가지고 있으며, 나무 상자를 만들 수 없을 때까지 계속해서 나무 상자를 만들 것이다. 그가 만들게 되는 나무 상자 수의 기댓값을 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에 나무 상자를 만드는데 필요한 나무 판자의 수와 그가 가지고 있는 나무 판자의 개수를 나타내는 두 자연수 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>M</i></span>이 공백으로 구분되어 주어진다.

다음 <span class="tex-span"><i>N</i></span>개의 줄의 <span class="tex-span"><i>i</i></span>번째 줄에는 나무 상자를 분해했을 때, 나무 판자 <span class="tex-span"><i>i</i>-1</span>개를 얻게 되는 확률을 의미하는 음이 아닌 정수 <span class="tex-span"><i>q</i><sub class="lower-index"><i>i</i>-1</sub>&thinsp;</span>이 주어진다. <SPAN class="tex-span"><I>q</I><SUB class="lower-index">0</SUB>&thinsp;+&thinsp;<I>q</I><SUB class="lower-index">1</SUB>&thinsp;+&thinsp;...&thinsp;+&thinsp;<I>q</I><SUB class="lower-index"><I>N</I>&thinsp;-&thinsp;1</SUB></SPAN>은 <SPAN class="tex-span">1</SPAN> 이상 <SPAN class="tex-span">10<SUP class="upper-index">9</SUP></SPAN> 이하임이 보장된다.

<br>

### 부분문제

<div class="row">
<div class="col-sm-6 col-md-6 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered' id="subtasks_table_for_problems">
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2"><center>부분문제</center></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><center>점수</center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>N</i></span></center></th>
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>M</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>4</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;1,000</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;5,000</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>96</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;16,000</span></center></td>
  <td><center><span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;10<sup class="upper-index">12</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

그가 만들게 되는 나무 상자 개수의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_A/06b42b72067b0539be8ff3d3d038be409c39d339.png">(<span class="tex-span">=&thinsp;2<sup class="upper-index">21</sup>&thinsp;&times;&thinsp;521&thinsp;+&thinsp;1&thinsp;</span>이며, 소수이다.)을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈로 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

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
		<tr><td><samp>2 3<br>1<br>1</samp></td><td><samp>546308098</samp></td></tr>
		<tr><td><samp>3 6<br>10<br>10<br>1</samp></td><td><samp>933814619</samp></td></tr>
    </tbody>
</table>

첫 번째 예제의 답은 <span class="tex-span">3/2</span>를 나타낸다.