당신은 Just Odd Inventions 사를 알고 있나요? 이 회사의 업무는 "그냥 이상한 발명(just odd inventions)"를 하는 것입니다. 이 문제에서는 편의상 JOI 사라고 부르겠습니다.

그런데, 당신은 Incredibly Odd Inventions 사를 알고 있나요? 이 회사의 업무는 "믿을 수 없을 정도로 이상한 발명(incredibly odd inventions)"를 하는 것입니다. 이 문제에서는 편의상 IOI 사라고 부르겠습니다.

JOI 사와 IOI 사에는 각각 <span class="tex-span"><i>N</i></span>명의 사원이 있습니다. JOI 사의 사원은 각각 <span class="tex-span"><i>j</i><sub class="lower-index">1</sub>,&thinsp;<i>j</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>j</i><sub class="lower-index"><i>N</i></sub></span> 중 하나로 불리며, IOI 사의 사원은 각각 <span class="tex-span"><i>i</i><sub class="lower-index">1</sub>,&thinsp;<i>i</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>i</i><sub class="lower-index"><i>N</i></sub></span> 중 하나로 불립니다. 또한, JOI 사의 사원 중 한 명은 JOI 사의 사장이며, IOI 사의 사원 중 한 명은 IOI 사의 사장입니다. 두 회사 모두, 사장을 제외한 각 사원에 대해, 그 사원을 직계 부하로 삼은 사원이 정확히 한 명 존재합니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_spy/pic1.png"/>
<p>[그림 1] JOI 사와 IOI 사의 조직의 예. 원은 사원을 나타냅니다. 사원에서 나오는 화살표는, 그 사원의 직계 부하를 가리킵니다.</p>
</center>

IOI 사는 언제나 JOI 사의 정보를 몰래 빼내어, "믿을 수 없을 만큼 이상한 발명(incredibly odd inventions)"을 하고 있습니다. 지금 JOI 사에서는, <span class="tex-span"><i>r</i><sub class="lower-index">1</sub>,&thinsp;<i>r</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>r</i><sub class="lower-index"><i>M</i></sub></span>으로 명명된 <span class="tex-span"><i>M</i></span>개의 연구 팀을 결성했습니다. IOI 사는 이에 따라, <span class="tex-span"><i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>s</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>s</i><sub class="lower-index"><i>M</i></sub></span>으로 명명된 <span class="tex-span"><i>M</i></span>개의 스파이 팀을 결성했습니다. IOI 사의 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index"><i>b</i></sub></span>는 JOI 사의 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index"><i>b</i></sub></span>의 정보를 빼내야 합니다.

두 회사 모두 각 팀에 소속될 사원을 결정하는 방식은 같습니다. 각 팀마다 한 사람의 리더가 결정됩니다. 먼저, 리더는 자신의 직계 부하들에게 명령을 내립니다. 이후, 명령을 받은 사원들은 자신의 직계 부하들에게 명령을 내립니다. 명령을 받은 모든 사원들과 리더는 해당 팀에 소속되고, 명령을 받지 않은 리더가 아닌 모든 사원들은 해당 팀에 소속되지 않습니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI13_spy/pic2.png"/>
<p>[그림 2] 그림 1의 JOI 사와 IOI 사에서 결성된 팀의 예</p>
</center>


IOI 사의 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>a</i></sub></span>는 JOI 사의 사원 <span class="tex-span"><i>j</i><sub class="lower-index"><i>a</i></sub></span>로부터 정보를 빼냅니다. 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index"><i>b</i></sub></span>에 소속된 IOI 사의 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>a</i></sub></span>는, JOI 사의 사원 <span class="tex-span"><i>j</i><sub class="lower-index"><i>a</i></sub></span>가 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index"><i>b</i></sub></span>에 소속되어 있다면, 스파이 활동에 성공합니다. 두 회사의 모든 사원은 여러 개의 팀에 소속되어 있을 가능성이 있고, IOI 사의 사원은 여러 개의 스파이 팀에서 스파이 활동에 성공할 가능성이 있습니다.

### 해야 할 일

JOI 사와 IOI 사의 사원의 정보와 팀에 대한 정보가 주어졌을 때, IOI 사의 각 사원에 대해, 이 사원이 몇 개의 스파이 팀에서 스파이 활동에 성공할지를 구하는 프로그램을 작성하세요.

### 입력 형식

* 첫 번째 줄에 두 개의 정수 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>M</i></span>이 주어집니다. 이는 IOI 사와 JOI 사의 사원이 각각 <span class="tex-span"><i>N</i></span>명이며, 연구 팀과 스파이 팀이 각각 <span class="tex-span"><i>M</i></span>개임을 나타냅니다.
* 이후 <span class="tex-span"><i>N</i></span>개의 줄이 주어집니다. 이 중 <span class="tex-span"><i>a</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>a</i>&thinsp;&le;&thinsp;<i>N</i></span>) 줄에는 두 개의 정수 <span class="tex-span"><i>P</i><sub class="lower-index"><i>a</i></sub>,&thinsp;<i>Q</i><sub class="lower-index"><i>a</i></sub></span>가 주어집니다. 이는 JOI 사의 사원 <span class="tex-span"><i>j</i><sub class="lower-index"><i>a</i></sub></span>가 사원 <span class="tex-span"><i>j</i><sub class="lower-index"><i>P</i><sub class="lower-index"><i>a</i></sub></sub></span>의 직계 부하이며, IOI 사의 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>a</i></sub></span>가 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>Q</i><sub class="lower-index"><i>a</i></sub></sub></span>의 직계 부하임을 나타냅니다. 또한 <span class="tex-span"><i>P</i><sub class="lower-index"><i>a</i></sub>&thinsp;=&thinsp;0</span>이라면 사원 <span class="tex-span"><i>j</i><sub class="lower-index"><i>a</i></sub></span>는 JOI 사의 사장이며, <span class="tex-span"><i>Q</i><sub class="lower-index"><i>a</i></sub>&thinsp;=&thinsp;0</span>이라면 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>a</i></sub></span>는 IOI 사의 사장입니다.
* 이후 <span class="tex-span"><i>M</i></span>개의 줄이 주어집니다. 이 중 <span class="tex-span"><i>b</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>b</i>&thinsp;&le;&thinsp;<i>M</i></span>) 줄에는 두 개의 정수 <span class="tex-span"><i>R</i><sub class="lower-index"><i>b</i></sub>,&thinsp;<i>S</i><sub class="lower-index"><i>b</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i><sub class="lower-index"><i>b</i></sub>&thinsp;&le;&thinsp;<i>N</i>,&thinsp;1&thinsp;&le;&thinsp;<i>S</i><sub class="lower-index"><i>b</i></sub>&thinsp;&le;&thinsp;<i>N</i></span>이 주어집니다. 이는 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index"><i>b</i></sub></span>의 리더가 <span class="tex-span"><i>j</i><sub class="lower-index"><i>R</i><sub class="lower-index"><i>b</i></sub></sub></span>이고, 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index"><i>b</i></sub></span>의 리더가 <span class="tex-span"><i>i</i><sub class="lower-index"><i>S</i><sub class="lower-index"><i>b</i></sub></sub></span>임을 나타냅니다.

### 출력 형식

<span class="tex-span"><i>N</i></span>개의 줄을 출력합니다. 이 중 <span class="tex-span"><i>a</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>a</i>&thinsp;&le;&thinsp;<i>N</i></span>) 줄에는 IOI 사의 사원 <span class="tex-span"><i>i</i><sub class="lower-index"><i>a</i></sub></span>가 몇 개의 스파이 팀에서 스파이 활동에 성공할지를 나타내는 정수 하나를 출력합니다.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;2&thinsp;000</span>.
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;500&thinsp;000</span>.

### 부분문제

#### 부분문제 1 (10점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;200</span>.
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;200</span>.

#### 부분문제 2 (20점)

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;2&thinsp;000</span>.

#### 부분문제 3 (70점)

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
	
	<tr><td><samp>3 4<br>0 2<br>1 0<br>2 2<br>1 1<br>2 1<br>2 3<br>3 2<br></samp></td><td><samp>1<br>0<br>2<br></samp></td></tr></tbody>
</table>

이 예제는 위 그림과 같습니다. 이 때,

* 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>s</i><sub class="lower-index">2</sub></span>, <span class="tex-span"><i>s</i><sub class="lower-index">4</sub></span>에 속하는 사원 <span class="tex-span"><i>i</i><sub class="lower-index">1</sub></span>은, 사원 <span class="tex-span"><i>j</i><sub class="lower-index">1</sub></span>이 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index">1</sub></span>에 속하기 때문에, 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index">1</sub></span>에서 스파이 활동에 성공합니다. 
* 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index">4</sub></span>에 속하는 사원 <span class="tex-span"><i>i</i><sub class="lower-index">2</sub></span>는, 사원 <span class="tex-span"><i>j</i><sub class="lower-index">2</sub></span>가 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index">4</sub></span>에 속하지 않기 때문에, 스파이 활동에 실패합니다. 
* 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index">3</sub></span>, <span class="tex-span"><i>s</i><sub class="lower-index">4</sub></span>에 속하는 사원 <span class="tex-span"><i>i</i><sub class="lower-index">3</sub></span>는, 사원 <span class="tex-span"><i>j</i><sub class="lower-index">3</sub></span>이 연구 팀 <span class="tex-span"><i>r</i><sub class="lower-index">3</sub></span>, <span class="tex-span"><i>r</i><sub class="lower-index">4</sub></span>에 속하기 때문에, 스파이 팀 <span class="tex-span"><i>s</i><sub class="lower-index">3</sub></span>, <span class="tex-span"><i>s</i><sub class="lower-index">4</sub></span>에서 스파이 활동에 성공합니다.
