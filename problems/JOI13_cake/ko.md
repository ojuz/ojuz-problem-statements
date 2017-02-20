석환이와 상수는 S대학 동문입니다. 석환이는 최근 제과제빵학원에 다니며 과자와 빵 만들기에 열중하고 있습니다. 오늘도 석환이는 케이크를 만들어 먹으려고 했는데, 상수가 맛있는 냄새를 따라 주방에 왔기 때문에, 두 사람이 케이크를 나눠 먹게 되었습니다.

케이크는 원 모양입니다. 석환이는 특정 지점에서 직선을 몇 개 그어 케이크를 <span class="tex-span"><i>N</i></span>개의 조각으로 나눴고, 각 조각에 <span class="tex-span">1</span> 이상 <span class="tex-span"><i>N</i></span> 이하의 자연수 번호를 시계 반대 방향으로 붙였습니다. 즉 <span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>을 만족하는 모든 <span class="tex-span"><i>i</i></span>에 대해, <span class="tex-span"><i>i</i></span>번 조각은 <span class="tex-span">(<i>i</i>&thinsp;-&thinsp;1)</span>번 조각, <span class="tex-span">(<i>i</i>&thinsp;+&thinsp;1)</span>번 조각과 붙어 있습니다. (단 0번 조각은 <span class="tex-span"><i>N</i></span>번 조각으로, <span class="tex-span">(<i>N</i>&thinsp;+&thinsp;1)</span>번 조각은 <span class="tex-span">1</span>번 조각으로 간주합니다.) <span class="tex-span"><i>i</i></span>번 조각의 크기는 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>입니다. 석환이는 케이크 자르는 솜씨가 매우 서투르기 때문에, 각 조각의 크기, 즉 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>는 서로 다릅니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_cake/cake1.png">
<div><small>그림 1: 케이크의 예 (<span class="tex-span"><i>N</i>&thinsp;=&thinsp;5,&thinsp;<i>A</i><sub class="lower-index">1</sub>&thinsp;=&thinsp;2,&thinsp;<i>A</i><sub class="lower-index">2</sub>&thinsp;=&thinsp;8,&thinsp;<i>A</i><sub class="lower-index">3</sub>&thinsp;=&thinsp;1,&thinsp;<i>A</i><sub class="lower-index">4</sub>&thinsp;=&thinsp;10,&thinsp;<i>A</i><sub class="lower-index">5</sub>&thinsp;=&thinsp;9</span>)</small></div>
</center>

석환이와 상수는 케이크 <span class="tex-span"><i>N</i></span>조각을 서로 나누어 가지기로 했습니다. 나누는 방법은 아래와 같습니다:

* 우선 석환이가 <span class="tex-span"><i>N</i></span>조각 중 하나를 선택하여 가져갑니다.
* 이후 상수부터 시작해서 두 사람은 번갈아 가면서 케이크 한 조각을 가져갑니다. 두 조각 사이에 있는 조각을 가져가면 케이크의 모양이 흐트러질 우려가 있으므로, 조각들 중 좌우 양쪽의 조각 중 적어도 한 쪽이 집혀 간 조각만 집어 갈 수 있고, 그런 조각이 여러 개 있을 때에는 가장 큰 것을 집습니다.

석환이는, 각 조각에 대해, 그 조각을 자신이 가장 먼저 가져갔을 때, 자신이 최종적으로 가져갈 케이크 조각들의 크기의 합이 얼마인지 알고자 합니다

### 해야 할 일

케이크 조각의 수 <span class="tex-span"><i>N</i></span>과, <span class="tex-span"><i>N</i></span>개의 조각의 크기의 정보가 주어졌을 때, 각 조각에 대해, 석환이가 그 조각을 가장 먼저 가져갔을 때, 석환이가 최종적으로 가져갈 케이크 조각들의 크기의 합을 구하는 프로그램을 작성하세요.

### 입력 형식

* 첫 번째 줄에 정수 <span class="tex-span"><i>N</i></span>이 주어집니다. 이는 케이크가 <span class="tex-span"><i>N</i></span>개의 조각들로 분리되어 있음을 나타냅니다. 
* 이후 <span class="tex-span"><i>N</i></span>개의 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span>번째 줄 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)에는 정수 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>가 주어집니다. 이는 <span class="tex-span"><i>i</i></span>번 조각의 크기가 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>라는 것을 나타냅니다.

### 출력 형식

<span class="tex-span"><i>N</i></span>개의 줄을 출력합니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는, 석환이가 <span class="tex-span"><i>i</i></span>번 조각을 가장 먼저 가져갔을 때, 석환이가 최종적으로 가져갈 케이크 조각들의 크기의 합을 나타내는 정수 하나를 출력해야 합니다.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* <span class="tex-span">2&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;300&thinsp;000</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)

### 부분문제

#### 부분문제 1 (10점)

* <span class="tex-span">2&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;5&thinsp;000</span>

#### 부분문제 2 (90점)

추가 제약 조건이 없습니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>5<br>2<br>8<br>1<br>10<br>9</samp></td><td><samp>13<br>18<br>12<br>13<br>12</samp></td></tr></tbody>
</table>

이 예는 문제 문중의 그림의 예로 대응하고 있다.

이 예제는 위 [그림 1]과 같습니다.

석환이가 1번 조각을 처음 가져갔다고 합시다. 이 때, 

* 남아 있는 조각들 중 "좌우 양쪽의 조각 중 적어도 한 쪽 조각이 집혀 간" 조각은 2번 조각과 5번 조각입니다. 5번 조각이 크므로 상수는 5번 조각을 가져갑니다.
* 그 다음, 2번 조각과 4번 조각을 가져갈 수 있고, 이 중 4번 조각이 크므로, 석환이는 4번 조각을 가져갑니다.
* 그 다음, 2번 조각과 3번 조각을 가져갈 수 있고, 이 중 2번 조각이 크므로, 상수는 2번 조각을 가져갑니다.
* 마지막에는 3번 조각만 남아 있으므로 석환이가 3번 조각을 가져갑니다.

즉 조각을 가져가는 순서는

* 1번 조각 (크기 2) &rightarrow; 5번 조각 (크기 9) &rightarrow; 4번 조각 (크기 10) &rightarrow; 2번 조각 (크기 8) &rightarrow; 3번 조각 (크기 1)

석환이가 가져간 조각들은 1번, 4번, 3번 조각으로, 크기의 합은 13이므로, 첫 번째 줄에 `13`을 출력해야 합니다. 