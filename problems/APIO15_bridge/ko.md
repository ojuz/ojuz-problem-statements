도시 팔렘방 시에는 무시강이라는 이름의 강이 있어 도시가 두 구역으로 나뉘어 있다. 두 구역을 구역 A와 구역 B라고 부르자.

각 구역에는 강변을 따라 정확히 1,000,000,001개의 빌딩이 있고, 순서 대로 0 부터 1,000,000,000까지 번호가 붙어 있다. 인접한 빌딩 간의 거리는 정확히 1 단위거리이다. 강의 폭도 1단위거리이다. 구역 A의 빌딩 i는 구역 B의 빌딩 i의 정확히 강 건너편에 위치한다.

<span class="tex-span"><i>N</i></span>명의 시민이 도시에서 살면서 일하고 있다. 시민 <span class="tex-span"><i>i</i></span>는 구역 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>의 빌딩 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>에 살고 있고 사무실은 구역 <span class="tex-span"><i>Q</i><sub class="lower-index"><i>i</i></sub></span>의 빌딩 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>에 있다. 사는 곳과 사무실이 다른 구역에 있는 경우에는 배를 타고 강을 건넜어야 했다. 물론 배를 타는 것이 불편하기 때문에 정부는 최대 <span class="tex-span"><i>K</i></span>개의 다리를 건설해서 모든 시민이 배를 타지 않고 자동차로 출근이 가능하도록 만들고 싶다. 다리는 강 방향에 수직이라야 하며 겹칠 수 없다.

<span class="tex-span"><i>D</i><sub class="lower-index"><i>i</i></sub></span>를 최대 <span class="tex-span"><i>K</i></span>개의 다리들이 건설된 후 시민 <span class="tex-span"><i>i</i></span>가 사는 곳에서 사무실 까지 운전해서 갈 수 있는 최소 거리라고 하자. <span class="tex-span"><i>D</i><sub class="lower-index">1</sub>&thinsp;+&thinsp;<i>D</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;...&thinsp;+&thinsp;<i>D</i><sub class="lower-index"><i>N</i></sub></span>의 값 최소가 되도록 다리를 건설하는 방법을 알아내는 프로그램을 작성하라.

### 입력 양식

입력의 첫 줄에는 <span class="tex-span"><i>K</i></span>와 <span class="tex-span"><i>N</i></span>이 주어진다. 이후 <span class="tex-span"><i>N</i></span>개의 줄에는 4개의 값 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>Q</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>가 각각 주어진다.

### 출력 양식

출력은 단 한줄이며 출근 거리 합의 최소값을 출력해야 한다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>1 5<br>B 0 A 4<br>B 1 B 3<br>A 5 B 7<br>B 2 A 6<br>B 1 A 7</samp></td><td><samp>24</samp></td></tr><tr><td><samp>2 5<br>B 0 A 4<br>B 1 B 3<br>A 5 B 7<br>B 2 A 6<br>B 1 A 7</samp></td><td><samp>22</samp></td></tr></tbody>
</table>

### 설명

두 입력 예 모두에 대한 그림이다.

<div class="row">
 <div class="col-sm-12 col-md-12 col-lg-12">
  <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/APIO15_bridge/bridge_initial.png" class="thumbnail"/>
 </div>
</div>

입력 예 1에 대한 가능한 해답이다. 분홍색 부분이 다리이다.

<div class="row">
 <div class="col-sm-12 col-md-12 col-lg-12">
  <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/APIO15_bridge/bridge_1.png" class="thumbnail"/>
 </div>
</div>

입력 예 2에 대한 가능한 해답이다.

<div class="row">
 <div class="col-sm-12 col-md-12 col-lg-12">
  <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/APIO15_bridge/bridge_2.png" class="thumbnail"/>
 </div>
</div>

### 부분 문제

모든 부분 문제에 대해서,

* <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>Q</i><sub class="lower-index"><i>i</i></sub></span>는 한글자 'A' 혹은 'B'이다.
* <span class="tex-span">0&thinsp;&le;&thinsp;<i>S</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000,&thinsp;000,&thinsp;000</span> 사는 곳이나 사무실이 서로 다른 시민에 대해서 같은 빌딩에 위치할 수 있고, 한 시민의 사는 곳이 다른 시민의 사무실과 같은 빌딩에 위치하는 것도 가능하다.

#### 부분 문제 1 (8점) 

* <span class="tex-span"><i>K</i>&thinsp;=&thinsp;1</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;1,000</span>

#### 부분 문제 2 (14점) 

* <span class="tex-span"><i>K</i>&thinsp;=&thinsp;1</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100,000</span>

#### 부분 문제 3 (9점)

* <span class="tex-span"><i>K</i>&thinsp;=&thinsp;2</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>

#### 부분 문제 4 (32점) 

* <span class="tex-span"><i>K</i>&thinsp;=&thinsp;2</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;1,000</span>

#### 부분 문제 5 (37점) 

* <span class="tex-span"><i>K</i>&thinsp;=&thinsp;2</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100,000</span>