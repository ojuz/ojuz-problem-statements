발리의 길에는 많은 조각상들이 있다. 큰길 하나에 있는 조각상들을 생각해 보자.

그 길에는 <span class="tex-span"><i>N</i></span>개의 조각상들이 있고 1부터 <span class="tex-span"><i>N</i></span>까지 순서대로 번호가 붙어 있다. 조각상 <span class="tex-span"><i>i</i></span>의 나이는 <span class="tex-span"><i>Y</i><sub><i>i</i></sub></span>년이다, 즉, <span class="tex-span"><i>Y</i><sub><i>i</i></sub></span>년 전에 만든 것이다. 길을 더 아름답게 만들기 위해 정부는 조각상들을 몇 개의 그룹으로 나누려고 한다. 그룹이 정해지고 나면 그룹들 사이에 아름다운 나무들을 심어서 관광객이 더 많이 오도록 만들려는 것이다.

조각상을 그룹으로 분할하는 규칙은 다음과 같다.

* 조각상들은 정확히 <span class="tex-span"><i>X</i></span>개의 그룹으로 분할되어야 한다. 단, <span class="tex-span"><i>A</i>&thinsp;&le;&thinsp;<i>X</i>&thinsp;&le;&thinsp;<i>B</i></span>이다. 각 그룹에는 최소한 하나의 조각상이 있어야 한다. 각 조각상은 단 하나의 그룹에만 속해야 한다. 각 그룹의 조각상들은 도로 상에 연속으로 존재해야 한다.
* 각 그룹에 대해서, 그룹에 속한 조각상들의 나이를 더한다.
* 그룹 별 합에 대해서, 모든 그룹 별 합의 비트 OR를 계산한다. 이 값을 분할의 아름다움 정도라고 하자.
* 아름다움 정도를 최소화 한다면 어떤 값이 될 것인가?

주의; 음수가 아닌 두 정수 <span class="tex-span"><i>P</i></span>와 <span class="tex-span"><i>Q</i></span>의 비트 OR는 다음과 같이 계산한다:

* <span class="tex-span"><i>P</i></span>와 <span class="tex-span"><i>Q</i></span>를 2진수로 변환.
* <span class="tex-span"><i>nP</i></span>를 <span class="tex-span"><i>P</i></span>의 비트 수라고 하고, <span class="tex-span"><i>nQ</i></span>를 <span class="tex-span"><i>Q</i></span>의 비트 수라고 하자. <span class="tex-span"><i>M</i></span>은 <span class="tex-span">max(<i>nP</i>,&thinsp;<i>nQ</i>)</span>이다.
* <span class="tex-span"><i>P</i></span>의 이진수 표현이 <span class="tex-span"><i>p</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub><i>p</i><sub class="lower-index"><i>M</i><sub class="lower-index">2</sub></sub>... <i>p</i><sub class="lower-index">1</sub><i>p</i><sub class="lower-index">0</sub></span>이고 <span class="tex-span"><i>Q</i></span>의 이진수 표현이 <span class="tex-span"><i>q</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub><i>q</i><sub class="lower-index"><i>M</i><sub class="lower-index">2</sub></sub>... <i>q</i><sub class="lower-index">1</sub><i>q</i><sub class="lower-index">0</sub></span>라고 하자. 단, <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>q</i><sub class="lower-index"><i>i</i></sub></span>는 각각 <span class="tex-span"><i>P</i></span>와 <span class="tex-span"><i>Q</i></span>의 <span class="tex-span"><i>i</i></span>번째 비트이다. 첨자가 <span class="tex-span">(<i>M</i>&thinsp;-&thinsp;1)</span>인 비트가 가장 높은 자리수이며 첨자가 0인 비트가 가장 낮은 자리수이다.
* 2진수로 <span class="tex-span"><i>P</i>&thinsp;OR&thinsp;<i>Q</i></span>의 결과는 <span class="tex-span">(<i>p</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub><i>&thinsp;OR&thinsp;q</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;1</sub>)(<i>p</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;2</sub><i>&thinsp;OR&thinsp;q</i><sub class="lower-index"><i>M</i>&thinsp;-&thinsp;2</sub>)... (<i>p</i><sub class="lower-index">1</sub><i>&thinsp;OR&thinsp;q</i><sub class="lower-index">1</sub>)(<i>p</i><sub class="lower-index">0</sub><i>&thinsp;OR&thinsp;q</i><sub class="lower-index">0</sub>)</span>이다. 단,
  - 0 OR 0 = 0
  - 0 OR 1 = 1
  - 1 OR 0 = 1
  - 1 OR 1 = 1

### 입력 양식

첫 줄에는 세 개의 정수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>A</i></span>, <span class="tex-span"><i>B</i></span>가 주어진다. 둘째 줄에는 <span class="tex-span"><i>N</i></span>개의 정수 <span class="tex-span"><i>Y</i><sub class="lower-index">1</sub>,&thinsp;<i>Y</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>Y</i><sub class="lower-index"><i>N</i></sub></span>이 주어진다.

### 출력 양식

출력은 단 한 줄이며 최소로 가능한 아름다움 정도를 출력해야 한다.

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>6 1 3<br>8 1 2 1 5 4</samp></td><td><samp>11</samp></td></tr></tbody>
</table>

### 설명

조각상들을 다음의 나이가 되도록 두 그룹으로 나눈다: (8 1 2) and (1 5 4). 그룹 별 합은 11과 10이다. 비트 OR을 계산하면 11이 된다.

### 부분문제

#### 부분 문제 1 (9점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;20</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i>&thinsp;&le;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>N</i></span> 
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000,&thinsp;000,&thinsp;000</span>

#### 부분 문제 2 (16점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;50</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i>&thinsp;&le;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>min</i>(20,&thinsp;<i>N</i>)</span>
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;10</span>

#### 부분 문제 3 (21점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>
* <span class="tex-span"><i>A</i>&thinsp;=&thinsp;1</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>N</i></span>
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;20</span>

#### 부분 문제 4 (25점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i>&thinsp;&le;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>N</i></span>
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000,&thinsp;000,&thinsp;000</span>

#### 부분 문제 5 (29점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;2,&thinsp;000</span>
* <span class="tex-span"><i>A</i>&thinsp;=&thinsp;1</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>N</i></span>
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000,&thinsp;000,&thinsp;000</span>