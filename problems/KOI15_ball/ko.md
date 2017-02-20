지훈이가 최근에 즐기는 컴퓨터 게임이 있다.

이 게임은 여러 플레이어가 참여하며, 각 플레이어는 특정한 색과 크기를 가진 자기 공 하나를 조정하여 게임에 참여한다. 각 플레이어의 목표는 자기 공보다 크기가 작고 색이 다른 공을 사로잡아 그 공의 크기만큼의 점수를 얻는 것이다. 그리고 다른 공을 사로잡은 이후에도 본인의 공의 색과 크기는 변하지 않는다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/KOI15_ball/1.png" style="max-width: 320px;"/>
</div>

다음 예에는 네 개의 공이 있다. 편의상 색은 숫자로 표현한다. 

이 경우, 2번 공은 다른 모든 공을 사로잡을 수 있다. 반면, 1번 공은 크기가 더 큰 2번 공과 색이 같은 3번 공은 잡을 수 없으며, 단지 4번 공만 잡을 수 있다.

공들의 색과 크기가 주어졌을 때, 각 플레이어가 사로잡을 수 있는 모든 공들의 크기의 합을 출력하는 프로그램을 작성하시오. 

### 입력 형식

첫 줄에는 공의 개수를 나타내는 자연수 N 이 주어진다(1 ≤ N ≤ 200,000).

다음 N 개의 줄 중 i번째 줄에는 i번째 공의 색을 나타내는 자연수 C<sub>i</sub>와 그 크기를 나타내는 자연수 S<sub>i</sub>가 주어진다(1 ≤ C<sub>i</sub> ≤ N, 1 ≤ S<sub>i</sub> ≤ 2,000).

서로 같은 크기 혹은 같은 색의 공들이 있을 수 있다. 

### 출력 형식

N 개의 줄을 출력한다. N 개의 줄 중 i번째 줄에는 i번째 공을 가진 플레이어가 잡을 수 있는 모든 공들의 크기 합을 출력한다. 
 
### 입력과 출력의 예

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>4<br>1 10<br>3 15<br>1 3<br>4 8</samp></td><td><samp>8<br>21<br>0<br>3</samp></td></tr><tr><td><samp>3<br>2 3<br>2 5<br>2 4<br></samp></td><td><samp>0<br>0<br>0</samp></td></tr></tbody>
</table>