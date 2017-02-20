IOI 산에서는 조난 사고가 끊임없이 발생하고 있습니다. 이에 IOI 나라의 정부는 IOI 산에 전문 산악 구조대를 설립했습니다. 설립한지 며칠이 지난 어느 날, 구조대에게 조난 사고를 알리는 통보가 왔습니다. 통보에 따르면 조난당한 사람들은 해발 고도가 <span class="tex-span"><i>X</i></span>인 곳에 머물고 있다고 합니다.

IOI 산은 <span class="tex-span"><i>R</i></span>행 <span class="tex-span"><i>C</i></span>열의 격자판으로 표시되고 각 격자에 해발 고도가 적혀 있습니다. <span class="tex-span"><i>r</i></span>번째 행과 <span class="tex-span"><i>c</i></span>번째 열의 교차점에 있는 격자는 <span class="tex-span">(<i>r</i>,&thinsp;<i>c</i>)</span>로 나타냅니다. 구조대는 산의 모양이 다음과 같이 되어 있다는 것을 알고 있습니다.

* 고도가 같은 서로 다른 두 격자는 존재하지 않습니다.
* 모든 칸의 고도는 1 이상 1,000,000,000 이하의 정수입니다.
* 산의 정상 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>S</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>S</i></sub>)</span>가 존재합니다. 즉 고도가 가장 큰 격자는 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>S</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>S</i></sub>)</span>입니다.
* 두 격자 <span class="tex-span">(<i>r</i><sub class="lower_index">1</sub>,&thinsp;<i>c</i><sub class="lower_index">1</sub>)</span>과 <span class="tex-span">(<i>r</i><sub class="lower_index">2</sub>,&thinsp;<i>c</i><sub class="lower_index">2</sub>)</span> 사이의 거리를 <span class="tex-span">|<i>r</i><sub class="lower-index">1</sub>&thinsp;-&thinsp;<i>r</i><sub class="lower-index">2</sub>|&thinsp;+&thinsp;|<i>c</i><sub class="lower-index">1</sub>&thinsp;-&thinsp;<i>c</i><sub class="lower-index">2</sub>|</span>로 정합니다. 이 때, 인접한 두 격자에 대해, 정상에서부터의 거리가 먼 격자가 고도가 더 작습니다. 두 격자가 인접하다는 것은 한 변을 공유하고 있다는 것을 말합니다. 

산악 구조대는 설립된지 얼마 안 되었기 때문에, IOI 산을 많이 조사하지 않았고 따라서 꼭짓점을 포함한 각 격자의 해발 고도는 알려져 있지 않습니다. 전문 측정 장비를 이용하여 어떤 한 격자의 해발 고도를 알아낼 수 있습니다. 그러나 고도를 측정하는 데에는 일정한 시간이 걸립니다. 구조대는 이 측정 기기를 사용하여 조난자가 있는 고도가 <span class="tex-span"><i>X</i></span>인 격자의 위치를 특정하고 싶으나, 이 측정 장치의 사용 횟수는 1000회 이하로 하고 싶습니다.

### 해야 할 일

IOI 산을 나타내는 격자판의 크기를 나타내는 두 정수 <span class="tex-span"><i>R</i></span>과 <span class="tex-span"><i>C</i></span>, 정상의 위치를 나타내는 두 정수 <span class="tex-span"><i>R</i><sub class="lower_index"><i>S</i></sub></span>, <span class="tex-span"><i>C</i><sub class="lower_index"><i>S</i></sub></span>, 조난자가 있는 격자의 해발 고도 <span class="tex-span"><i>X</i></span>가 주어집니다. 측정 기기를 최대 1,000번 이용하여 조난자가 있는 격자의 위치를 특정할 수 있는 프로그램을 작성하세요.

### 구현 세부 사항

여러분은 측정 장비를 사용하는 방법을 구현한 프로그램을 작성해야 합니다. 이 프로그램은 아래 함수를 구현해야 합니다.

```
void Rescue (int R, int C, int RS, int CS, int X)
```

이 함수는 각 테스트 케이스(실행)에 대해 단 한 번만 호출됩니다. 인수 `R`과 `C`는 각각 산을 나타내는 격자판의 행의 수 <span class="tex-span"><i>R</i></span>과 열의 수 <span class="tex-span"><i>C</i></span>입니다. 인수 `RS`와 `CS`는 각각 산 정상의 행 번호와 열 번호 <span class="tex-span"><i>R</i><sub class="lower_index"><i>S</i></sub></span>, <span class="tex-span"><i>C</i><sub class="lower_index"><i>S</i></sub></span>입니다. 인수 `X`는 조난자가 있는 격자의 해발 고도 <span class="tex-span"><i>X</i></span>입니다.

또한 이 함수는 아래 함수들을 호출할 수 있습니다.

```
int Measure (int RM, int CM);
```

이 함수는 측정 기기를 사용하고자 할 때 호출됩니다. 인수 `RM`과 `CM`은 측정 기기가 고도를 확인할 격자의 행 번호 <span class="tex-span"><i>R</i><sub class="lower_index"><i>M</i></sub></span>과 열 번호 <span class="tex-span"><i>C</i><sub class="lower_index"><i>M</i></sub></span>입니다. <span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower_index"><i>M</i></sub>&thinsp;&le;&thinsp;<I>R</I></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i><sub class="lower_index"><i>M</i></sub>&thinsp;&le;&thinsp;<I>C</I></span>를 만족해야 합니다. 이 함수의 반환값은 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>M</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>M</i></sub>)</span>의 고도를 나타내는 1 이상 1,000,000,000 이하의 정수입니다. 

<span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower_index"><i>M</i></sub>&thinsp;&le;&thinsp;<I>R</I></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i><sub class="lower_index"><i>M</i></sub>&thinsp;&le;&thinsp;<I>C</I></span>를 만족하지 않는 인자로 이 함수를 호출하면 **Wrong Answer [1]**이 판정되며 프로그램은 즉시 종료됩니다.

또한 이 함수의 호출 횟수가 1000회를 초과할 시 **Wrong Answer [2]**가 판정되며 프로그램은 즉시 종료됩니다.

```
void Pinpoint (int RP, int CP);
```

이 함수는 조난자가 있는 격자의 위치를 측정하고자 할 때 단 한 번 호출해야 합니다. 인수 `RP`와 `CP`는 각각 조난자가 있는 격자의 행 번호 <span class="tex-span"><i>R</i><sub class="lower_index"><i>P</i></sub></span>와 열 번호 <span class="tex-span"><i>C</i><sub class="lower_index"><i>P</i></sub></span>입니다. <span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower_index"><i>P</i></sub>&thinsp;&le;&thinsp;<I>R</I></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i><sub class="lower_index"><i>P</i></sub>&thinsp;&le;&thinsp;<I>C</I></span>를 만족해야 합니다. 이 함수는 반환값이 없습니다.

<span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower_index"><i>P</i></sub>&thinsp;&le;&thinsp;<I>R</I></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i><sub class="lower_index"><i>P</i></sub>&thinsp;&le;&thinsp;<I>C</I></span>를 만족하지 않는 인자로 이 함수를 호출하면 **Wrong Answer [3]**이 판정되며 프로그램은 즉시 종료됩니다.

프로그램이 이 함수를 호출했을 때 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>P</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>P</i></sub>)</span>의 해발 고도가 <span class="tex-span"><i>X</i></span>와 같다면 정답, 그렇지 않으면 **Wrong Answer [4]**가 판정되며, 프로그램은 즉시 종료됩니다.

`Pinpoint` 함수를 단 한 번도 호출하지 않고 종료한 경우, **Wrong Answer [5]**가 판정되며 프로그램의 실행은 종료됩니다.

### 컴파일 및 실행 방법

작성한 프로그램을 시험해 보기 위한 예제 채점 프로그램은 [여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_mountain/grader.zip)를 클릭하시면 내려받을 수 있습니다. 이 파일에는 제출해야 할 파일인 `mountain.c(pp)` 역시 포함되어 있습니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_mountain/download.png">
</center>

예제 채점 프로그램은 위 사진과 같이 문제 제목 오른쪽에 있는, 아랫방향 화살표를 클릭하시면 쉽게 내려받을 수 있습니다. (모든 문제에 적용되어 있습니다!)

예제 채점 프로그램은 1개의 파일로 구성되어 있습니다. 그 파일은 `grader.c` 또는 `grader.cpp`이다. 작성한 프로그램을 컴파일하려면, 다음과 같이 명령을 실행해야 합니다.

* C의 경우: <samp>gcc -O2 -lm grader.c mountain.c -o grader</samp>
* C++의 경우: <samp>g++ -O2 grader.cpp mountain.cpp -o grader</samp>

컴파일에 성공하면, `grader`라는 실행 파일이 생성됩니다.

실제 채점 프로그램은 예제 채점 프로그램과 다르다는 점에 유의하세요.. 이 프로그램은 표준 입력(`stdin`)으로부터 입력을 받고, 표준 출력(`stdout`)에 출력합니다. 단 입력 파일이 이상한 등, 프로그램의 실행과 관련 없는 비정상적인 오류가 발생했을 시 `stderr`에 출력합니다.

### 입력 형식

예제 채점 프로그램은 표준 입력(`stdin`)으로부터 아래와 같이 입력을 받습니다.

* 첫 번째 줄에는 네 개의 정수 <span class="tex-span"><i>R</i></span>, <span class="tex-span"><i>C</i></span>, <span class="tex-span"><i>R</i><sub class="lower_index"><i>S</i></sub></span>, <span class="tex-span"><i>C</i><sub class="lower_index"><i>S</i></sub></span>, <span class="tex-span"><i>X</i></span>가 주어집니다. <span class="tex-span"><i>R</i></span>과 <span class="tex-span"><i>C</i></span>는 산을 나타내는 격자판의 크기를 나타내고, 정상의 위치는 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>S</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>S</i></sub>)</span>이며, <span class="tex-span"><i>X</i></span>는 조난자가 있는 격자의 높이입니다.
* 다음 <span class="tex-span"><i>R</i></span>개 줄에는 산의 고도의 정보가 주어집니다. 이 중 <span class="tex-span"><i>i</i></span>번째 줄 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>R</i></span>)에는 <span class="tex-span"><i>C</i></span>개의 정수가 공백을 사이로 두고 주어집니다. 그 중 <span class="tex-span"><i>j</i></span>번째 정수 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>C</i></span>)는 격자 <span class="tex-span">(<i>i</i>,&thinsp;<i>j</i>)</span>의 고도를 나타냅니다.

### 출력 형식

프로그램 실행이 정상적으로 종료된다면, 예제 채점 프로그램은 표준 출력(`stdout`)에 프로그램의 실행 결과를 나타내는 메시지를 한 줄에 출력합니다.

* 정답의 경우, "<samp>Accepted</samp>"으로 출력됩니다.(따옴표는 실제로는 출력되지 않습니다.)
* 오답의 경우, "<samp>Wrong Answer[1]</samp>"과 같이 출력됩니다. 괄호 안의 숫자는 위에서 기술한 오류 번호와 같습니다. <samp>Wrong Answer[4]</samp>에 대해서는, 조난자의 위치 <span class="tex-span">(<i>R</i><sub class="lower_index"><i>X</i></sub>,&thinsp;<i>C</i><sub class="lower_index"><i>X</i></sub>)</span>와 `Pinpoint` 함수의 인자 `RP`, `CP`의 값이 "<samp>Wrong Answer[4]:(RX, CX)=(3, 2),(RP, CP)=(4, 1)</samp>"과 같이 출력됩니다.

### 제약 조건

모든 데이터는 아래 조건을 만족합니다.

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i>&thinsp;&le;&thinsp;200</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i>&thinsp;&le;&thinsp;200</span> 
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower-index"><i>S</i></sub>&thinsp;&le;&thinsp;<i>R</i></span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>C</i><sub class="lower-index"><i>S</i></sub>&thinsp;&le;&thinsp;<i>C</i></span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>X</i>&thinsp;&le;&thinsp;1&thinsp;000&thinsp;000&thinsp;000</span>

### 부분문제

#### 부분문제 1 [20점]

* <span class="tex-span"><i>R</i>&thinsp;&le;&thinsp;50</span> 
* <span class="tex-span"><i>C</i>&thinsp;&le;&thinsp;50</span> 

#### 부분문제 2 [80점]

추가 제약 조건이 없습니다.

### 예시

<div class="row">
<div class="col-sm-10 col-md-6 col-lg-4">
<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-12 col-md-12 col-sm-12">입력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>5 5 3 3 76<br>14 59 84 62 28<br>15 73 92 76 35<br>68 97 100 89 75<br>58 67 86 79 55<br>17 25 71 10 5</samp></td></tr></tbody>
</table>
</div>
</div>

<div class="row">
<div class="col-sm-12 col-md-6 col-lg-4">
<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">호출</th>
			<th class="col-lg-6 col-md-6 col-sm-6">반환값</th>
		</tr>
	</thead>
	<tbody>
	<tr><td><code>Measure(1, 1)</code></td><td>14</td></tr>
	<tr><td><code>Measure(3, 5)</code></td><td>75</td></tr>
	<tr><td><code>Measure(2, 4)</code></td><td>76</td></tr>
	<tr><td><code>Pinpoint(2, 4)</code></td><td>-</td></tr>
    </tbody>
</table>
</div>
</div>

위 예시는 단순히 이해를 돕기 위한 것이며, 올바른 방법과는 관계가 없습니다.
