나나는 기다림이 많아 지루한 출근 시간을 면하기 위해, 기다림이 적은 출근을 해 보기로 했습니다.

나나는 지하철 0호선을 타고 출근합니다. 0호선에는 총 <span class="tex-span"><i>N</i>&thinsp;+&thinsp;1</span>개의 역이 있으며, 각 역에는 <span class="tex-span">0</span> 이상 <span class="tex-span"><i>N</i></span> 이하의 정수 번호가 시발역에서부터 종착역까지 차례대로 붙어 있습니다. 나나의 집은 <span class="tex-span">0</span>번 역에, 회사는 <span class="tex-span"><i>N</i></span>번 역에 있습니다. 이 노선은 매우 광활한 영토를 가로지르기 때문에, 열차들은 서로 인접한 두 역 사이만 지나다닙니다.

각 열차에는 번호가 붙어있는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번 열차는 <span class="tex-span">(<i>i</i>&thinsp;-&thinsp;1)</span>번 역에서 출발하여 <span class="tex-span"><i>i</i></span>번 역에 도착합니다. (안타깝게도, 이 열차를 타고 <span class="tex-span"><i>i</i></span>번 역에서 <span class="tex-span">(<i>i</i>&thinsp;-&thinsp;1)</span>번 역으로 갈 수는 없습니다.) 이 열차는 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>분을 기준으로 그 이전에나 그 이후에나 <span class="tex-span"><i>C</i><sub class="lower-index"><i>i</i></sub></span>분 간격으로 <b style="color:red"><span class="tex-span">(<i>i</i>&thinsp;-&thinsp;1)</span>번 역</b>에서 출발합니다. 예를 들어서 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;5</span>,  <span class="tex-span"><i>C</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;3</span>이라면 ... -4, -1, 2, 5, 8, 11, 14 ... 분에 출발한다는 것입니다. 두 역 사이를 이동하는 데에는 <span class="tex-span"><i>D</i><sub class="lower-index"><i>i</i></sub></span>분이 걸립니다. 즉, 출발한 지 <span class="tex-span"><i>D</i><sub class="lower-index"><i>i</i></sub></span>분이 지났을 때 <b style="color:red"><span class="tex-span"><i>i</i></span>번 역</b>에 도착합니다.

어떤 역에서 열차 <span class="tex-span"><i>X</i></span>가 도착하는 시각을 <span class="tex-span"><i>t</i><sub class="lower-index">1</sub></span>, 열차 <span class="tex-span"><i>Y</i></span>가 출발하는 시각을 <span class="tex-span"><i>t</i><sub class="lower-index">2</sub></span>로 둘 때, <span class="tex-span"><i>t</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>t</i><sub class="lower-index">2</sub></span>를 만족한다면, 나나는 열차 <span class="tex-span"><i>X</i></span>에서 내려 <span class="tex-span"><i>t</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>t</i><sub class="lower-index">1</sub></span>분을 기다린 후 열차 <span class="tex-span"><i>Y</i></span>로 갈아탈 수 있습니다. 나나는 번호가 1 이상 N 이하인 열차들만을 이용하여, <strong>{(<span class="tex-span"><i>N</i></span>번 열차에서 내린 시각) - (1번 열차를 탄 시각)}</strong>의 값을 최소화하여 출근하고 싶습니다. 이 값은 대체 얼마일까요??

### 입력 형식

첫 번째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;1,000</span>)가 주어집니다.

각 테스트 케이스의 첫 번째 줄에는 지하철 노선 수 <span class="tex-span"><i>N</i></span>이 주어집니다. 그 다음 <span class="tex-span"><i>N</i></span>개의 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 세 개의 자연수 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>C</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>D</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다.

### 출력 형식

각 테스트 케이스마다, 답을 분 단위로 한 줄에 하나씩 출력합니다.

### 입력 파일 정보

<div class="row">
<div class="col-sm-12 col-md-10 col-lg-8">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">입력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">출력 파일명</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>N</i></span></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>C</i><sub class="lower-index"><i>i</i></sub></span></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>D</i><sub class="lower-index"><i>i</i></sub></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>A1.in</samp></td>
  <td><samp>A1.out</samp></td>
  <td>15</td>
  <td><span class="tex-span">&le; 2</span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
 </tr>
 <tr>
  <td><samp>A2.in</samp></td>
  <td><samp>A2.out</samp></td>
  <td>25</td>
  <td><span class="tex-span">&le; 50</span></td>
  <td><span class="tex-span">&le; 20</span></td>
  <td><span class="tex-span">&le; 20</span></td>
  <td><span class="tex-span">&le; 20</span></td>
 </tr>
 <tr>
  <td><samp>A3.in</samp></td>
  <td><samp>A3.out</samp></td>
  <td>60</td>
  <td><span class="tex-span">&le; 50</span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 답안 생성 및 제출 방법

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_A/a_input.zip)에서 입력 파일을 내려받아서, 위 표에 따라 출력 파일을 만듭니다. 제출하는 방법은 두 가지가 있습니다.

* 모든 출력 파일을 하나의 zip 파일에 압축하여 제출합니다. 다른 폴더 안에 출력 파일을 넣고 압축하는 등의 행위를 할 시 업로드 공격으로 의심되어 업로드가 즉시 차단됩니다.
* 각 출력 파일을 하나씩 업로드하여 제출합니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>2<br>2<br>0 6 2<br>6 6 2<br>2<br>0 6 2<br>2 6 2</samp></td><td><samp>8<br>4</samp></td></tr></tbody>
</table>