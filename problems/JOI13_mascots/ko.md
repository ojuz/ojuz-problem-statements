승현이는 친구들과 마스코트를 가지고 놀았습니다. 즐거운 시간은 순식간에 지나갔고, 친구가 돌아간 지금은 뒷정리를 해야 합니다.

승현이는 마스코트를 <span class="tex-span"><i>R</i>&thinsp;&times;&thinsp;<i>C</i></span>개 가지고 있어서, 이들을 정리하기 위해 단위 격자들로 구성된 <span class="tex-span"><i>R</i></span>행 <span class="tex-span"><i>C</i></span>열의 격자판을 사용합니다. 하나의 격자에는 한 개의 마스코트를 넣습니다. 편의상 위에서부터 <span class="tex-span"><i>A</i></span>번째 행, 왼쪽에서부터 <span class="tex-span"><i>B</i></span>번째 열에 있는 격자를 <span class="tex-span">(<i>A</i>,&thinsp;<i>B</i>)</span>로 표현합니다. 정리를 시작할 때, 적어도 마스코트가 들어 있지 않은 격자 하나가 존재함이 보장됩니다.

승현이는 마스코트를 하나씩 두면서 정리합니다. 마스코트 하나를 새로 놓는 순간에, 마스코트가 놓여 있는 격자들 전체가 하나의 직사각형이 되면, 승현이는 행복해합니다. (처음 상태가 직사각형을 이루고 있는 경우에는 행복하지 않습니다) 마스코트가 놓여 있는 격자들 전체가 하나의 직사각형이 된다는 것은, 어떤 4개의 정수 <span class="tex-span"><i>r</i><sub class="lower-index">1</sub>,&thinsp;<i>r</i><sub class="lower-index">2</sub>,&thinsp;<i>c</i><sub class="lower-index">1</sub>,&thinsp;<i>c</i><sub class="lower-index">2</sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>r</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>r</i><sub class="lower-index">2</sub>&thinsp;&le;&thinsp;<i>R</i></span>, <span class="tex-span">1&thinsp;&le;&thinsp;<i>c</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>c</i><sub class="lower-index">2</sub>&thinsp;&le;&thinsp;<i>C</i></span>)가 존재하여, <span class="tex-span"><i>r</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>r</i><sub class="lower-index">2</sub></span>와 <span class="tex-span"><i>c</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>c</i><sub class="lower-index">2</sub></span>를 만족하는 모든 격자 <span class="tex-span">(<i>i</i>,&thinsp;<i>j</i>)</span>에 마스코트가 있고, 이 이외의 격자에는 마스코트가 없다는 것입니다. 승현이가 행복해하는 횟수가 많을수록 승현이는 오늘 밤 푹 잘 수 있습니다.

마스코트들의 종류는 구별하지 않습니다. 승현이가 행복해하는 횟수를 최대화하는, 마스코트를 둘 수 있는 방법은 모두 몇 가지 있을까요?

### 해야 할 일

격자판의 크기 (행과 열)와 이미 놓여 있는 마스코트들에 대한 정보가 주어질 때, 승현이가 행복해하는 횟수를 최대화하는, 마스코트를 둘 수 있는 방법의 수를 <span class="tex-span">1&thinsp;000&thinsp;000&thinsp;007</span>로 나눈 나머지를 구하는 프로그램을 작성하세요.

### 입력 형식

* 첫 번째 줄에 두 개의 정수 <span class="tex-span"><i>R</i></span>, <span class="tex-span"><i>C</i></span>가 공백을 사이로 두고 주어집니다. <span class="tex-span"><i>R</i></span>은 격자판의 행의 수, <span class="tex-span"><i>C</i></span>는 격자판의 열의 수를 나타냅니다.
* 두 번째 줄에는 정수 <span class="tex-span"><i>N</i></span>이 주어집니다. <span class="tex-span"><i>N</i></span>은 정리를 시작하기 전 격자판에 이미 놓여 있는 마스코트의 개수를 나타냅니다.
* 이후 <span class="tex-span"><i>N</i></span>개의 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>)번째 줄에는 두 개의 정수 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다. 이는 <span class="tex-span">(<i>A</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>B</i><sub class="lower-index"><i>i</i></sub>)</span>에 마스코트 하나가 놓여 있음을 의미합니다. 같은 격자가 두 번 이상 주어지지 않습니다.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* <span class="tex-span">2&thinsp;&le;&thinsp;<i>R</i>&thinsp;&le;&thinsp;3&thinsp;000</span>.
* <span class="tex-span">2&thinsp;&le;&thinsp;<i>C</i>&thinsp;&le;&thinsp;3&thinsp;000</span>.
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100&thinsp;000</span>.

### 부분문제

#### 부분문제 1 (10점)

* <span class="tex-span"><i>R</i>&thinsp;&le;&thinsp;3</span>.
* <span class="tex-span"><i>C</i>&thinsp;&le;&thinsp;3</span>.

#### 부분문제 2 (30점)

* <span class="tex-span"><i>R</i>&thinsp;&le;&thinsp;50</span>.
* <span class="tex-span"><i>C</i>&thinsp;&le;&thinsp;50</span>.

#### 부분문제 3 (60점)

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
	
	<tr><td><samp>2 3<br>2<br>1 2<br>2 2</samp></td><td><samp>8</samp></td></tr></tbody>
</table>

처음 격자판의 모습은 아래와 같습니다. (<span class="tex-span">&Delta;</span>는 초기 상태로 마스코트가 놓여 있습니다.)

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_mascots/exp1.png"/>
</center>

6개의 격자 중 (1, 2)와 (2, 2)에는 이미 마스코트가 놓여 있습니다. 승현이가 행복해하는 횟수의 최댓값은 2입니다. 승현이가 행복해하는 횟수가 2회가 되도록 마스코트들을 놓는 방법은 아래 그림과 같이 8가지가 있습니다. (숫자는 마스코트를 놓은 순서를 나타낸다).

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_mascots/exp2.png"/>
</center>

8가지의 방법 모두 2번째로 마스코트를 놓는 순간에 <span class="tex-span">2&thinsp;&times;&thinsp;2</span>의 직사각형이, 4번째로 마스코트를 놓는 순간에  <span class="tex-span">2&thinsp;&times;&thinsp;3</span>의 직사각형이 형성됩니다.

<table class="table table-condensed table-bordered " id="examples_table2">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시 2 </th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시 2</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>3 3<br>2<br>1 1<br>3 3<br></samp></td><td><samp>5040<br></samp></td></tr></tbody>
</table>