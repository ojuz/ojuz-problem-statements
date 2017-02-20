자카르타 시에는 <span class="tex-span"><i>N</i></span>개의 큰빌딩이 일직선 위에 위치하고 있다. 이들은 왼쪽부터 <span class="tex-span">0,&thinsp;1,&thinsp;...,&thinsp;<i>N</i>&thinsp;-&thinsp;1</span>까지 번호가 붙어 있다. 자카르타에는 이들 말고 다른 큰빌딩은 없다.

자카르타에는 "<span class="tex-font-style-it">도게</span>"라고 불리는 신비한 생명체들이 살고 있다. 도게들은 <span class="tex-span">0,&thinsp;1,&thinsp;...,&thinsp;<i>M</i>&thinsp;-&thinsp;1</span> 까지 번호가 붙어 있다. 도게 <span class="tex-span"><i>i</i></span>는 최초에 빌딩 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>에 위치하고 있다. 도게 <span class="tex-span"><i>i</i></span>가 가진 신비한 힘은 그 능력치가 양의 정수 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>로 표시된다. 도게는 이 신비한 힘으로 큰 빌딩들 간에 점프를 할 수 있다. 큰 빌딩 <span class="tex-span"><i>b</i></span>에 있는 능력치가 <span class="tex-span"><i>p</i></span>인 도게는 한번의 점프로 큰빌딩 <span class="tex-span"><i>b</i>&thinsp;+&thinsp;<i>p</i></span>(<span class="tex-span">0&thinsp;&le;&thinsp;<i>b</i>&thinsp;+&thinsp;<i>p</i>&thinsp;&lt;&thinsp;<i>N</i></span>이라야 함) 혹은 큰빌딩 <span class="tex-span"><i>b</i>&thinsp;-&thinsp;<i>p</i></span>(<span class="tex-span">0&thinsp;&le;&thinsp;<i>b</i>&thinsp;-&thinsp;<i>p</i>&thinsp;&lt;&thinsp;<i>N</i></span>이라야 함)로 이동할 수 있다.

도게 0이 가장 대단한 도게이며 모든 도게들의 지도자이다. 도게 0은 급한 소식이 있어 이 소식을 도게 1에게 전해야 한다. 물론 가장 빨리 소식이 전해지기를 바란다. 뉴스를 전해 들은 도게는 다음의 두가지 중 하나를 할 수 있다.

* 다른 큰 빌딩으로 점프.
* 현재 위치한 빌딩의 다른 도게에게 소식을 전달

도게들을 도와주는 프로그램을 작성해야 한다. 이 프로그램은 소식을 도게 1에게 전할 수 있는 최소한의 점프 횟수를 계산해야 한다. 만약 소식을 전달하는 것이 불가능한 경우라면 그것도 알아내야 한다.

### 입력 형식

입력의 첫 줄에는 정수 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>M</i></span>이 주어진다. 이후 <span class="tex-span"><i>M</i></span>개의 줄에는 두 자연수 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>가 주어진다.

### 출력 형식

출력은 단 한 줄이며, 최소의 점프 횟수라야 한다. 불가능한 경우 -1을 출력한다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>5 3<br>0 2<br>1 1<br>4 1</samp></td><td><samp>5</samp></td></tr></tbody>
</table>

### 설명

다음 경우가 5 번의 점프로 가능한 시나리오이다.

* 도게 0이 큰빌딩 2로 점프, 또 큰빌딩 4로 점프 (2번 점프).
* 도게 0이 소식을 도게 2에게 전함.
* 도게 2가 큰빌딩 3으로 점프, 또 큰빌딩 2로 점프, 또 큰빌딩 1로 점프 (3번 점프).
* 도게 2가 도게 1에게 소식을 전함.

### 부분문제

모든 부분문제에서,

* <span class="tex-span">0&thinsp;&le;&thinsp;<i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>N</i></span>

#### 부분문제 1 (10점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;10</span> 
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;3</span>

#### 부분문제 2 (12점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;100</span>
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;2,000</span>

#### 부분문제 3 (14점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;2,000</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;2,000</span> 
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;2,000</span>

#### 부분문제 4 (21점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;2,000</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;2,000</span> 
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;30,000</span>

#### 부분문제 5 (43점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;30,000</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;30,000</span>
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;30,000</span>