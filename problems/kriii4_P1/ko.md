음이 아닌 두 정수 <span class="tex-span"><i>A</i>, <i>X</i>&thinsp;</span>가 있을 때 <span class="tex-span"><i>A</i><sup class="upper-index"><i>X</i></sup></span>을 구하는 방법을 생각해보자. 물론 이 수는 매우 클 수 있기에, <span class="tex-span">1,000,000,007</span> (<span class="tex-span">=&thinsp;10<sup>9</sup>&thinsp;+&thinsp;7</span>)로 나눈 나머지를 구할 것이다. <span class="tex-span"><i>a</i> mod <i>x</i></span>를 <span class="tex-span"><i>a</i></span>를 <span class="tex-span"><i>x</i></span>로 나눴을 때의 나머지라고 표현하면,

<center><span class="tex-span">(<i>a&thinsp;&times;&thinsp;b</i>) mod <i>x</i> = {(<i>a</i> mod <i>x</i>) &times; (<i>b</i> mod <i>x</i>)} mod <i>x</i></span></center>

가 성립하기 때문에, 어떤 두 정수를 <span class="tex-span">1,000,000,007</span>로 나눈 나머지만 알고 있어도 그 두 정수의 곱을 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 쉽게 계산할 수 있다.

본 문제로 돌아가서, 그렇다면 이제 <span class="tex-span"><i>A</i></span>를 <span class="tex-span"><i>X</i>&thinsp;</span>번 곱하면 <span class="tex-span"><i>A</i><sup class="upper-index"><i>X</i></sup></span>을 쉽게 구할 수 있을 것 같아 보인다. 그러나 안타깝게도 <span class="tex-span"><i>X</i></span>가 상당히 커서 64비트 정수의 범위에 있다면 <span class="tex-span"><i>A</i></span>를 하나하나씩 곱하는 방식으로는 상상할 수 없을 정도로 긴 시간이 흘러야 답을 찾을 수 있을 것이다. 그래서 다음과 같이 곱셈의 횟수를 줄이는 방법을 사용한다.

1. 먼저 <span class="tex-span"><i>A</i><sup class="upper-index">1</sup></span>, <span class="tex-span"><i>A</i><sup class="upper-index">2</sup></span>, <span class="tex-span"><i>A</i><sup class="upper-index">4</sup></span>, <span class="tex-span"><i>A</i><sup class="upper-index">8</sup></span>, ...을 순서대로 계산한다. 각 수는 이전에 있는 수를 제곱함으로써 계산할 수 있고, 지수가 <span class="tex-span"><i>X</i>&thinsp;</span>를 딱 넘지 않을 시점까지만 계산하면 충분할 것이다. <span class="tex-span"><i>X</i></span>가 64비트 정수의 범위에 있으므로 계산하는 수는 64개보다 작을 것이다.
2. 이제 <span class="tex-span"><i>X</i>&thinsp;</span>를 이진수로 나타내 보자. 예를 들어 <span class="tex-span"><i>X</i></span>를 <span class="tex-span">11</span>로 두면, <span class="tex-span"><i>X</i>&thinsp;=&thinsp;11&thinsp;=&thinsp;1&thinsp;+&thinsp;2&thinsp;+&thinsp;8</span>이다. 그런데 지수법칙에 의해, <span class="tex-span"><i>A</i><sup class="upper-index">11</sup>&thinsp;=&thinsp;<i>A</i><sup class="upper-index">1+2+8</sup>&thinsp;=&thinsp;<i>A</i><sup class="upper-index">1</sup>&thinsp;&times;&thinsp;<i>A</i><sup class="upper-index">2</sup>&thinsp;&times;&thinsp;<i>A</i><sup class="upper-index">8</sup></span>이 성립한다. 이를 통해 1번 단계에서 미리 계산해 놓았던 수 몇 개만 곱해서 <span class="tex-span"><i>A</i><sup class="upper-index"><i>X</i>&thinsp;</sup></span>을 계산할 수 있음을 알 수 있다.

즉, 차례로 <span class="tex-span"><i>A</i></span>를 곱해 나간다면 시간이 <span class="tex-span"><i>X</i></span>에 비례하게 걸리겠지만, 위의 방법을 이용하면 시간이 <span class="tex-span">log(<i>X</i>)</span>에 비례하게 걸리게 된다. <span class="tex-span"><i>A</i><sup class="upper-index"><i>X</i></sup></span>를 구하는 프로그램을 작성하라.

<br>

### 입력

첫 번째 줄에는 정수 <span class="tex-span"><i>A</i>(1&thinsp;&leq;&thinsp;<i>A</i>&thinsp;&leq;&thinsp;10<sup class="upper-index">18</sup>)</span>이 주어진다.

두 번째 줄에는 정수 <span class="tex-span"><i>X</i>(1&thinsp;&leq;&thinsp;<i>X</i>&thinsp;&leq;&thinsp;10<sup class="upper-index">18</sup>)</span>가 주어진다.

<br>

### 출력

<span class="tex-span"><i>A</i><sup class="upper-index"><i>X</i></sup></span>을 출력한다. 이 수는 매우 커질 수 있으므로 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력해야 한다.

<br>

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예제</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예제</th>
		</tr>
	</thead>
	<tbody>
		<tr><td><samp>3<br>3</samp></td><td><samp>27</samp></td></tr>
		<tr><td><samp>100<br>100</samp></td><td><samp>424090053</samp></td></tr>
    </tbody>
</table>