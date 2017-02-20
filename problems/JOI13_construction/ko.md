IOI 나라에서는 교통망을 새로 건설하려고 합니다. IOI 나라는 2차원 좌표 평면으로 나타낼 수 있고, 이 평면 위에는 <span class="tex-span"><i>N</i></span>개의 마을이 있습니다. 이 중 <span class="tex-span"><i>i</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>) 마을은 점 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>)</span>로 표현됩니다. 교통망 건설은 다음과 같은 순서로 진행됩니다.

* <span class="tex-span"><i>N</i></span>개의 마을 중 1개 이상의 마을에 국제 공항을 건설합니다. 국제 공항은 한 개 건설할 때마다 정해진 비용이 추가로 듭니다. 
* 마을 사이를 잇는 도로들을 몇 개 건설합니다. 도로는 마을을 나타내는 점들을 직접 잇는, <span class="tex-span"><i>x</i></span>축 또는 <span class="tex-span"><i>y</i></span>축에 평행하는 선분으로, 새로 건설할 때마다 그 길이만큼의 비용이 추가로 듭니다. 

이 때, 아래 조건을 만족해야 합니다.

* IOI 나라에는 지반이 약한 것과 같은 이유로 도로를 건설할 수 없는 영역이 <span class="tex-span"><i>M</i></span>개 있습니다. 각 영역은 직사각형으로 표현되며, <span class="tex-span"><i>j</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>M</i></span>) 직사각형의 왼쪽 아래 점은 <span class="tex-span">(<i>P</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>Q</i><sub class="lower-index"><i>j</i></sub>)</span>이고 오른쪽 위의 점은 <span class="tex-span">(<i>R</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>S</i><sub class="lower-index"><i>j</i></sub>)</span>입니다. (<span class="tex-span"><i>P</i><sub class="lower-index"><i>j</i></sub>&thinsp;&lt;&thinsp;<i>R</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>Q</i><sub class="lower-index"><i>j</i></sub>&thinsp;&lt;&thinsp;<i>S</i><sub class="lower-index"><i>j</i></sub></span>) 모든 도로는 <span class="tex-span"><i>M</i></span>개의 영역 중 하나와도 공통 부분을 가지면 안 됩니다. 영역은 직사각형의 변(경계) 역시 포함합니다. 따라서 영역을 나타내는 직사각형의 변과 공통 부분을 가지는 도로도 존재하면 안 됩니다. 
* <span class="tex-span"><i>N</i></span>개의 어떤 마을에서도, 도로를 따라 여러 도시를 거쳐 국제 공항이 있는 마을(공항만 있다면 어떤 마을이라도 괜찮음)에 도착할 수 있어야 합니다.

IOI 나라는 이 건설 사업의 발주 업체를 선정해야 합니다. <span class="tex-span"><i>C</i></span>개의 건설 업체가 후보로 선정되었습니다. 이 중 <span class="tex-span"><i>k</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>C</i></span>) 건설 업체는, 국제 공항을 한 개 건설하는 데 <span class="tex-span"><i>B</i><sub class="lower-index"><i>k</i></sub></span>의 비용이 들고, 최대 <span class="tex-span"><i>H</i><sub class="lower-index"><i>k</i></sub></span>개의 국제 공항을 건설할 수 있습니다. 도로 건설에 드는 비용은 건설 업체별로 다르지 않으며(모두 길이 1당 비용 1 추가), 건설할 도로의 개수나 길이의 제한은 없습니다. 각 건설 업체에 대해, 그 건설 업체가 위의 조건을 만족하도록 교통망을 적절히 건설할 때 드는 비용의 합의 최솟값을 알고자 합니다.

건설할 수 있는 국제 공항의 수가 작기 때문에, 조건을 만족하면서 교통망을 건설할 수 없는 건설 업체가 있을 수도 있습니다. 그러한 경우, 비용의 합 대신 조건을 만족할 수 없다는 것을 알려줘야 합니다.

### 해야 할 일

IOI나라의 마을의 수를 나타내는 정수 <span class="tex-span"><i>N</i></span>, 각 마을의 좌표, 도로를 건설할 수 없는 영역의 수를 나타내는 정수 <span class="tex-span"><i>M</i></span>, 각 영역의 꼭짓점의 좌표, 발주 업체 후보 수를 나타내는 정수 <span class="tex-span"><i>C</i></span>와, 각 건설 업체의 정보가 주어졌을 때, 각 건설 업체에 대해, 그 건설 업체가 위의 조건을 만족하도록 교통망을 적절히 건설할 때 드는 비용의 합의 최솟값을 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에는 세 개의 정수 <span class="tex-span"><i>N</i>,&thinsp;<i>M</i>,&thinsp;<i>C</i></span>가 공백을 사이로 두고 주어집니다. <span class="tex-span"><i>N</i></span>은 IOI 나라의 마을의 수, <span class="tex-span"><i>M</i></span>은 도로를 건설할 수 없는 영역의 수, <span class="tex-span"><i>C</i></span>는 발주 업체 후보 수를 나타냅니다.

이후 <span class="tex-span"><i>N</i></span>개의 줄이 주어지는데, 그 중 <span class="tex-span"><i>i</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>) 줄에는 2개의 정수 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어지며, 이는 <span class="tex-span"><i>i</i></span>번째 마을의 좌표가 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>)</span>임을 나타냅니다.

이후 <span class="tex-span"><i>M</i></span>개의 줄이 주어지는데, 그 중 <span class="tex-span"><i>j</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>M</i></span>) 줄에는 4개의 정수 <span class="tex-span"><i>P</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>Q</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>R</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>S</i><sub class="lower-index"><i>j</i></sub></span>가 공백을 사이로 두고 주어지며, 이는 <span class="tex-span"><i>j</i></span>번째 도로 건설 불가 영역을 나타내는 직사각형의 왼쪽 아래 점의 좌표가 <span class="tex-span">(<i>P</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>Q</i><sub class="lower-index"><i>j</i></sub>)</span>, 오른쪽 위 점의 좌표가 <span class="tex-span">(<i>R</i><sub class="lower-index"><i>j</i></sub>,&thinsp;<i>S</i><sub class="lower-index"><i>j</i></sub>)</span>임을 나타냅니다.

이후 <span class="tex-span"><i>C</i></span>개의 줄이 주어지는데, 그 중 <span class="tex-span"><i>k</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>C</i></span>) 줄에는 2개의 정수 <span class="tex-span"><i>B</i><sub class="lower-index"><i>k</i></sub>,&thinsp;<i>H</i><sub class="lower-index"><i>k</i></sub></span>가 공백을 사이로 두고 주어지며, 이는 <span class="tex-span"><i>k</i></span>번째 건설 업체는 국제 공항을 하나 건설하는 데 <span class="tex-span"><i>B</i><sub class="lower-index"><i>k</i></sub></span>의 비용이 들며, 최대 <span class="tex-span"><i>H</i><sub class="lower-index"><i>k</i></sub></span>개의 국제 공항을 건설할 수 있다는 것을 의미합니다.

### 출력 형식

<span class="tex-span"><i>C</i></span>개의 줄을 출력합니다. 이 중 <span class="tex-span"><i>k</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>C</i></span>) 줄에는, <span class="tex-span"><i>k</i></span>번째 건설 업체가 위의 조건을 만족하도록 교통망을 적절히 건설할 때 드는 비용의 합의 최솟값을 출력합니다. 단, <span class="tex-span"><i>k</i></span>번째 건설 업체가 위의 조건을 만족하도록 교통망을 적절히 건설할 수 없을 시, <span class="tex-span">&thinsp;-&thinsp;1</span>을 출력합니다.

### 제약 조건

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;200&thinsp;000</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;200&thinsp;000</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i>&thinsp;&le;&thinsp;500&thinsp;000</span>
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>X</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)
* 한 점 위에 두 개 이상의 마을이 있는 경우는 없습니다.
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>j</i></sub>&thinsp;&lt;&thinsp;<i>R</i><sub class="lower-index"><i>j</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>M</i></span>)
* 어떤 영역도 도로를 그 영역의 내부 또는 경계 위에 포함하지 않습니다.
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>B</i><sub class="lower-index"><i>k</i></sub>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>C</i></span>)
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i><sub class="lower-index"><i>k</i></sub>&thinsp;&le;&thinsp;<i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;<i>C</i></span>)

### 부분문제

#### 부분문제 1 [10점]

* <span class="tex-span"><i>M</i>&thinsp;&le;&thinsp;100</span>
* <span class="tex-span"><i>C</i>&thinsp;&le;&thinsp;100</span>

#### 부분문제 2 [30점]

* <span class="tex-span"><i>C</i>&thinsp;&le;&thinsp;100</span>

#### 부분문제 3 [30점]

* <span class="tex-span"><i>M</i>&thinsp;&le;&thinsp;100</span>

#### 부분문제 4 [30점]

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
	
	<tr><td><samp>4 2 3<br>1 1<br>10 1<br>1 10<br>10 10<br>4 0 8 9<br>1 4 9 8<br>7 4<br>10 3<br>1 1</samp></td><td><samp>28<br>38<br>-1<br></samp></td></tr></tbody>
</table>

위 예제를 그림으로 나타내면 아래와 같습니다. 굵은 선으로 표시된 직사각형은 도로를 건설할 수 없는 영역을 나타내며, 따라서 그 내부 (경계 포함)에는 도로를 건설할 수 없습니다.

<div class="thumbnail">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_construction/ex.png"/>
</div>

2번 마을과 4번 마을을 잇는 도로, 3번 마을과 4번 마을을 잇는 도로는 건설할 수 있습니다. 하지만 1번 마을과 2번 마을을 잇는 도로, 1번 마을과 3번 마을을 잇는 도로는 건설할 수 없습니다. (도로는 직사각형의 경계를 포함하는 내부 위를 지나갈 수 없습니다)

첫 번째 건설 회사는 최대 4개의 국제 공항을 한 개 당 7의 비용을 들여 건설할 수 있습니다. 이 경우, 도로를 하나도 건설하지 않고, 모든 마을에 국제 공항을 하나씩 세우는 것이 최선이며, 그때의 비용의 합은 <span class="tex-span">7&thinsp;&times;&thinsp;4&thinsp;=&thinsp;28</span>입니다.

두 번째 건설 회사는 최대 3개의 국제 공항을 한 개 당 10의 비용을 들여 건설할 수 있습니다. 이 경우, 2번 마을과 4번 마을을 잇는 길이가 9인 도로, 3번 마을과 4번 마을을 잇는 길이가 9인 도로를 건설하고, 1번 마을과 2번 마을에 국제 공항을 세우는 것이 최선입니다. 그때의 비용의 합은 <span class="tex-span">10&thinsp;&times;&thinsp;2&thinsp;+&thinsp;9&thinsp;+&thinsp;9&thinsp;=&thinsp;38</span>입니다.

세 번째 건설 회사는 최대 1개의 국제 공항을 한 개 당 1의 비용을 들여 건설할 수 있습니다. 하지만 1번 마을과 다른 어떤 마을을 잇는 도로도 건설할 수 없기 때문에, 문제의 조건을 만족하도록 교통망을 만들기 위해서는 적어도 2개의 국제 공항을 세워야 합니다. 따라서 이 회사는 교통망을 만들 수 없으며, 따라서 <samp>-1</samp>을 출력합니다.