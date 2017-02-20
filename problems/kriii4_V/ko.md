그는 여러 가지 색을 지닌 구슬을 엮어 팔찌를 만드는 취미에 빠졌다. 그가 만드는 팔찌는 여러 개의 구슬을 일렬로 놓은 다음 실로 꿰어 실의 양 끝을 묶어 원형으로 만든 것이다. 그가 만들 수 있는 팔찌의 종류는 무궁무진하지만 비슷한 것을 싫어하는 그는 팔찌를 회전시키거나 뒤집어서 사용된 구슬의 색 순서가 같으면 같은 종류로 취급하기로 했다.

<p style="text-align: center;">
<img src="https://attach.oj.uz/contest/kriii4/V1.png" style="width: 50%; height: 50%"/>
</p>

위의 그림은 빨간 구슬과 파란 구슬을 교대로 엮어 구슬을 네 개 사용한 팔찌를 만든 경우이다. 어떤 색 구슬을 기준으로 보느냐에 따라 두 가지 종류로 볼 수 있다. 그러나 왼쪽의 팔찌를 시계방향으로 조금 회전시키면 오른쪽에 있는 팔찌와 같은 구성이 되므로, 한 가지 종류로 생각해야 한다. 

<p style="text-align: center;">
<img src="https://attach.oj.uz/contest/kriii4/V2.png" style="border: none; width: 50%; height: 50%"/>  	 	 
</p>

또 다른 예로, 위의 그림은 다섯 개의 구슬을 사용하여 팔찌를 만든 경우이다. 왼쪽의 팔찌를 좌우로 뒤집으면 오른쪽에 있는 팔찌를 만들 수 있으므로, 위의 두 팔찌는 한 가지 종류로 생각해야 한다.

그가 가진 구슬 색의 종류는 현재 <span class="tex-span"><i>K</i></span>종류이고, 각 종류의 구슬은 무한히 많이 준비되어 있다. 구슬을 <span class="tex-span"><i>N</i></span>개 이하만 사용해서 만들 수 있는 서로 다른 팔찌의 종류의 수를 구하는 프로그램을 작성하라. 구슬을 하나도 사용하지 않은 팔찌도 하나의 종류로 생각한다.

<br>

### 입력

첫 번째 줄에는 사용할 수 있는 구슬의 개수와 구슬 색의 종류를 나타내는 두 자연수 <span class="tex-span"><i>N</i>,&thinsp;<i>K</i></span>가 공백으로 구분되어 주어진다.

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
  <th class="col-sm-3 col-md-3 col-lg-3"><center><span class="tex-span"><i>K</i></span></center></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><center>1</center></td>
  <td><center>6</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;8</span></center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;8</span></center></td>
 </tr>
 <tr>
  <td><center>2</center></td>
  <td><center>94</center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
  <td><center><span class="tex-span">1&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;10<sup class="upper-index">6</sup></span></center></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

<br>

### 출력

첫 번째 줄에 구슬을 <span class="tex-span"><i>N</i>&thinsp;</span>개 이하만 사용해서 만들 수 있는 팔찌의 종류 개수를 출력한다. 이 수는 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

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
		<tr><td><samp>1 3</samp></td><td><samp>4</samp></td></tr>
		<tr><td><samp>8 8</samp></td><td><samp>1237325</samp></td></tr>
		<tr><td><samp>100 100</samp></td><td><samp>639265925</samp></td></tr>
    </tbody>
</table>
