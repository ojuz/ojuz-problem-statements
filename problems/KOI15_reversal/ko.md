1부터 20까지 숫자가 하나씩 쓰인 20장의 카드가 아래 그림과 같이 오름차순으로 한 줄로 놓여있다. 각 카드의 위치는 카드 위에 적힌 숫자와 같이 1부터 20까지로 나타낸다. 

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/KOI15_reversal/1.png" style="max-width: 430px;"/>
</div>

이제 여러분은 다음과 같은 규칙으로 카드의 위치를 바꾼다: 구간 [a, b] (단, 1 ≤ a ≤ b ≤ 20)가 주어지면 위치 a부터 위치 b까지의 카드를 현재의 역순으로 놓는다.

예를 들어, 현재 카드가 놓인 순서가 위의 그림과 같고 구간이 [5, 10]으로 주어진다면, 위치 5부터 위치 10까지의 카드 5, 6, 7, 8, 9, 10을 역순으로 하여 10, 9, 8, 7, 6, 5로 놓는다. 이제 전체 카드가 놓인 순서는 아래 그림과 같다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/KOI15_reversal/2.png" style="max-width: 430px;"/>
</div>

이 상태에서 구간 [9, 13]이 다시 주어진다면, 위치 9부터 위치 13까지의 카드 6, 5, 11, 12, 13을 역순으로 하여 13, 12, 11, 5, 6으로 놓는다. 이제 전체 카드가 놓인 순서는 아래 그림과 같다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/KOI15_reversal/3.png" style="max-width: 430px;"/>
</div>

오름차순으로 한 줄로 놓여있는 20장의 카드에 대해 10개의 구간이 주어지면, 주어진 구간의 순서대로 위의 규칙에 따라 순서를 뒤집는 작업을 연속해서 처리한 뒤 마지막 카드들의 배치를 구하는 프로그램을 작성하시오.

### 입력 형식

총 10개의 줄에 걸쳐 한 줄에 하나씩 10개의 구간이 주어진다. i번째 줄에는 i번째 구간의 시작 위치 a<sub>i</sub>와 끝 위치 b<sub>i</sub>가 차례대로 주어진다. 이때 두 값의 범위는 1 ≤ a<sub>i</sub> ≤ b<sub>i</sub> ≤ 20 이다. 

### 출력 형식

1부터 20 까지 오름차순으로 놓인 카드들에 대해, 입력으로 주어진 10개의 구간 순서대로 뒤집는 작업을 했을 때 마지막 카드들의 배치를 한 줄에 출력한다. 

### 입력과 출력의 예

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-4 col-md-4 col-sm-4">입력 예시</th>
			<th class="col-lg-8 col-md-8 col-sm-8">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>5 10<br>9 13<br>1 2<br>3 4<br>5 6<br>1 2<br>3 4<br>5 6<br>1 20<br>1 20</samp></td><td><samp>1 2 3 4 10 9 8 7 13 12 11 5 6 14 15 16 17 18 19 20</samp></td></tr><tr><td><samp>1 1<br>2 2<br>3 3<br>4 4<br>5 5<br>6 6<br>7 7<br>8 8<br>9 9<br>10 10</samp></td><td><samp>1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20</samp></td></tr><tr><td><samp>1 20<br>2 19<br>3 18<br>4 17<br>5 16<br>6 15<br>7 14<br>8 13<br>9 12<br>10 11</samp></td><td><samp>20 2 18 4 16 6 14 8 12 10 11 9 13 7 15 5 17 3 19 1</samp></td></tr></tbody>
</table>
 