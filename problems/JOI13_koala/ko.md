긴 직선 모양의 길 위에 지학이의 집과 석환이의 집이 있습니다. 점프가 특기인 코알라 우현이는 지학이의 집에서 출발하여 석환이의 집에 가려고 합니다.

이 길 위의 각 지점은, 1개의 수로 표현되는 좌표로 나타낼 수 있습니다. 지학이의 집의 좌표는 <span class="tex-span"><i>K</i></span>이고, 석환이의 집의 좌표는 <span class="tex-span"><i>M</i></span>입니다. 이 두 집 사이에는 <span class="tex-span"><i>N</i></span>개의 간이 숙소가 있습니다. <span class="tex-span"><i>i</i></span>번째 간이 숙소의 좌표는 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>입니다.

우현이는 체력이 0인 상태로 지학이의 집을 떠나서, 점프를 몇 차례 반복하여, 석환이의 집에 갑니다. 한 번 점프하면, 우현이는 석환이의 집 쪽으로 <span class="tex-span"><i>d</i></span>만큼 이동한 위치로 이동할 수 있습니다. 이 때 <span class="tex-span"><i>d</i></span>는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>d</i>&thinsp;&le;&thinsp;<i>D</i></span>를 만족하는 정수여야 합니다. 한 번 점프하면, 우현이의 체력은 <span class="tex-span"><i>A</i></span>만큼 줄어듭니다. 체력의 값은 음수가 될 수도 있습니다.

우현이가 뛰어서 도착한 지점에 간이 숙소가 있다면, 우현이는 그 곳에서 최대 1회까지 잘 수 있습니다. 우현이가 <span class="tex-span"><i>i</i></span>번째 간이 숙소에 묵으면, 체력의 값이 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>만큼 증가합니다.

우현이는 가급적 체력이 많은 (체력의 값이 큰) 상태로 석환이의 집에 도착하고자 합니다.

### 해야 할 일

우현이가 적절히 점프하여 석환이의 집에 도착했을 때 우현이의 체력의 값의 최댓값을 구하는 프로그램을 작성하세요.

### 입력 형식 

첫 번째 줄에 지학이의 집의 좌표 <span class="tex-span"><i>K</i></span>, 석환이의 집의 좌표 <span class="tex-span"><i>M</i></span>, 한 번 점프할 수 있는 거리의 최댓값 <span class="tex-span"><i>D</i></span>, 한 번 점프하면 줄어드는 체력 <span class="tex-span"><i>A</i></span>, 간이 숙소의 개수 <span class="tex-span"><i>N</i></span>이 공백을 사이로 두고 주어집니다. 이 수들은 모두 정수입니다.

이후 <span class="tex-span"><i>N</i></span>개의 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span>번째 줄 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)에는 <span class="tex-span"><i>i</i></span>번째 간이 숙소의 좌표 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>i</i></span>번째 간이 숙소에서 자면 늘어나는 체력 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다. 이 수들은 모두 정수입니다.

### 출력 형식

첫 번째 줄에 우현이가 적절히 점프하여 석환이의 집에 도착했을 때 우현이의 체력의 값의 최댓값을 나타내는 정수 하나를 출력하세요.

### 제약 조건

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>D</i>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100&thinsp;000</span> 
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>K</i>&thinsp;&lt;&thinsp;<i>T</i><sub class="lower-index">1</sub>&thinsp;&lt;&thinsp;...&thinsp;&lt;&thinsp;<i>T</i><sub class="lower-index"><i>N</i></sub>&thinsp;&lt;&thinsp;<i>M</i>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000(1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i>)</span>

### 부분문제

#### 부분문제 1 [20점]

* <span class="tex-span"><i>N</i>&thinsp;&le;&thinsp;1&thinsp;000</span> 

#### 부분문제 2 [30점]

* <span class="tex-span"><i>D</i>&thinsp;&le;&thinsp;100</span> 

#### 부분문제 3 [50점]

추가 제약 조건이 없습니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시 1</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시 1</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>0 10 4 10 2<br>3 10<br>8 5</samp></td><td><samp>-20</samp></td></tr></tbody>
</table>

이 예제에서, 다음과 같이 행동하는 것이 최적입니다.

* 거리가 3인 점프를 합니다. 우현이는 좌표가 3인 지점으로 가고 체력은 -10이 됩니다.
* 1번 간이 숙소에 묵습니다. 체력은 0이 됩니다.
* 거리가 4인 점프를 합니다. 우현이는 좌표가 7인 지점으로 가고 체력은 -10이 됩니다.
* 거리가 3인 점프를 합니다. 우현이는 석환이의 집에 도착하고 체력은 -20이 됩니다.

<table class="table table-condensed table-bordered " id="examples_table_2">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시 2</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시 2</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>3 42 9 10 8<br>10 5<br>12 9<br>26 7<br>27 2<br>30 8<br>34 6<br>36 8<br>40 10</samp></td><td><samp>-25</samp></td></tr></tbody>
</table>

이 예제에서, 다음과 같이 행동하는 것이 최적입니다.

* 거리가 9인 점프를 합니다. 우현이는 좌표가 12인 지점으로 가고 체력은 -10이 됩니다.
* 2번 간이 숙소에 묵습니다. 체력은 -1이 됩니다.
* 거리가 9인 점프를 합니다. 우현이는 좌표가 21인 지점으로 가고 체력은 -11이 됩니다.
* 거리가 9인 점프를 합니다. 우현이는 좌표가 30인 지점으로 가고 체력은 -21이 됩니다.
* 5번 간이 숙소에 묵습니다. 체력은 -13이 됩니다.
* 거리가 6인 점프를 합니다. 우현이는 좌표가 36인 지점으로 가고 체력은 -23이 됩니다.
* 7번 간이 숙소에 묵습니다. 체력은 -15이 됩니다.
* 거리가 6인 점프를 합니다. 우현이는 석환이의 집에 도착하고 체력은 -25가 됩니다.