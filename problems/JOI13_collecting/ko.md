승현이는 사진 수집을 좋아하여 하드 디스크에 많은 사진들을 가지고 있습니다. 사진을 모으면 모을 수록 그 용량은 커졌습니다. 어느 날 승현이는 '이렇게 사진을 계속 수집하다 보면 하드 디스크의 용량이 부족하지 않을까?' 하는 걱정이 들었습니다. 새로운 하드디스크를 구입하면 해결되겠지만, 가난한 승현이에게는 너무 부담스러웠습니다. 그렇다고 이미 수집한 사진을 삭제하는 것은 너무나 고통스러운 일이었습니다. 따라서 승현이는 사진을 잘 압축하여 총 용량을 줄이기로 했습니다.

사진은 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>행 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>열의 정사각형 격자판 모양이며, 총 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup>&thinsp;&times;&thinsp;2<sup class="upper-index"><i>N</i></sup></span>개의 픽셀들로 구성되어 있습니다. 각 픽셀은 흰색 또는 검은색입니다.

승현이는 이 사진을 다음과 같은 방법으로 압축하기로 했습니다.

* 픽셀들의 색이 모두 같다면, 그 색만을 기록합니다. 이 때 압축된 사진의 크기는 1입니다.
* 그렇지 않다면, 사진을 4개의 작은 사진들로 나눕니다. 원래 사진이 <span class="tex-span">2<sup class="upper-index"><i>k</i></sup></span>행 <span class="tex-span">2<sup class="upper-index"><i>k</i></sup></span>열이었다고 하면, 가로의 중심과 세로의 중심을 기준으로 사진을 분할하여, <span class="tex-span">2<sup class="upper-index"><i>k</i>&thinsp;-&thinsp;1</sup></span>행 <span class="tex-span">2<sup class="upper-index"><i>k</i>&thinsp;-&thinsp;1</sup></span>열의 사진 4개를 얻습니다. 사진들을 나눈 이후에는 작은 사진들을 같은 방법으로 압축합니다. 이 때 압축된 사진의 크기는 (4개의 작은 사진들을 압축했을 때의 크기)<span class="tex-span">&thinsp;+&thinsp;1</span>입니다. 

승현이는 '이 방법으로 과연 사진을 압축할 수 있을까?' 하는 생각이 들어, 다양한 사진들에 대해 실험을 해보기로 했습니다. 실험 방법은 아래와 같습니다.

* 우선 모든 픽셀이 흰색인 사진 하나를 준비합니다. 
* 모든 <span class="tex-span"><i>i</i>&thinsp;=&thinsp;1,&thinsp;2,&thinsp;...,&thinsp;<i>Q</i></span>에 대해, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;0</span>이면 위에서부터 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>번째 행의 픽셀들을 각각 반전시키고, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;1</span>이면 왼쪽에서부터 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>번째 열의 픽셀들을 각각 반전시키는 작업을 수행합니다. 어떤 픽셀을 반전시킨다는 것은, 픽셀이 흰색이었다면 검정색으로, 검정색이었다면 흰색으로 바꾼다는 것입니다. 다시 말해, 위에서부터 <span class="tex-span"><i>a</i></span>번째 행, 왼쪽에서부터 <span class="tex-span"><i>b</i></span>번째 열에 있는 픽셀을 <span class="tex-span">(<i>a</i>,&thinsp;<i>b</i>)</span>로 나타냈을 때, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;0</span>이라면 <span class="tex-span">1&thinsp;&le;&thinsp;<i>b</i>&thinsp;&le;&thinsp;2<sup class="upper-index"><i>N</i></sup></span>을 만족하는 모든 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>b</i>)</span>를 반전시키고, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;1</span>이라면 <span class="tex-span">1&thinsp;&le;&thinsp;<i>a</i>&thinsp;&le;&thinsp;2<sup class="upper-index"><i>N</i></sup></span>을 만족하는 모든 <span class="tex-span">(<i>a</i>,&thinsp;<i>X</i><sub class="lower-index"><i>i</i></sub>)</span>를 반전시키는 작업을 수행해야 합니다. 

승현이는 실험을 가능한 한 많이 하기 위해, 압축된 사진의 크기를 최대한 빨리 알아내고자 합니다.

### 해야 할 일

사진의 크기를 나타내는 정수 <span class="tex-span"><i>N</i></span>, 작업 횟수 <span class="tex-span"><i>Q</i></span>와 <span class="tex-span"><i>Q</i></span>번의 작업 명령이 주어졌을 때, 각 작업이 끝난 후, 사진을 승현이의 방법대로 압축했을 때, 압축된 사진의 크기를 구하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에 사진의 크기를 나타내는 정수 <span class="tex-span"><i>N</i></span>과 작업 횟수 <span class="tex-span"><i>Q</i></span>가 공백을 사이로 두고 주어집니다. 사진의 크기는 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>행 <span class="tex-span">2<sup class="upper-index"><i>N</i></sup></span>열입니다.

다음 <span class="tex-span"><i>Q</i></span>개 줄에는 작업 명령이 주어집니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>Q</i></span>)번째 줄에는 두 개의 정수 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;1&thinsp;&le;&thinsp;<i>X</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;2<sup class="upper-index"><i>N</i></sup></span>)이 공백을 사이로 두고 주어집니다. 이는 <span class="tex-span"><i>i</i></span>번째 작업이 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;0</span>이라면 위에서부터 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>번째 행의 픽셀들을, <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;1</span>이라면 왼쪽에서부터 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>번째 열의 픽셀들을 반전시키는 것임을 나타냅니다.

### 출력 형식

<span class="tex-span"><i>Q</i></span>개의 줄을 출력합니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>Q</i></span>)번째 줄에는 <span class="tex-span"><i>i</i></span>번째 작업이 끝난 후, 사진을 승현이의 방법대로 압축했을 때, 압축된 사진의 크기를 나타내는 정수 하나를 출력합니다.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;20</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>Q</i>&thinsp;&le;&thinsp;2&thinsp;000&thinsp;000</span>

### 부분문제

#### 부분문제 1 [10점]

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;6</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>Q</i>&thinsp;&le;&thinsp;128</span>

#### 부분문제 2 [20점]

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>Q</i>&thinsp;&le;&thinsp;2&thinsp;048</span>

#### 부분문제 3 [70점]

* 추가 제약 조건이 없습니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>2 3<br>0 1<br>1 2<br>0 3</samp></td><td><samp>13<br>17<br>21</samp></td></tr></tbody>
</table>

이 예제에서 <span class="tex-span"><i>Q</i>&thinsp;=&thinsp;3</span>번의 작업은 다음과 같이 이루어집니다.

<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_collecting/ex.png"/>