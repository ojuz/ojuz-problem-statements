<style type="text/css">
.tex-span {
    font-size: 125%;
    font-family: times new roman;
}
.tex-formula {
    vertical-align: middle;
    margin: 0;
    border:medium none;
    position: relative;
    bottom: 2px;
}
</style>

<b>사원수(Quaternion)</b>는 복소수를 확장해 만든 수 체계이다. 사원수는 <span class="tex-span"><i>i</i><sup class="upper-index">2</sup>&thinsp;=&thinsp;<i>j</i><sup class="upper-index">2</sup>&thinsp;=&thinsp;<i>k</i><sup class="upper-index">2</sup>&thinsp;=&thinsp;<i>ijk</i>&thinsp;=&thinsp;&thinsp;-&thinsp;1</span>을 만족하는 세 복소수 <span class="tex-span"><i>i</i>, &thinsp;<i>j</i>, &thinsp;<i>k</i></span>를 이용해 표현되어 네 개의 실수 성분을 가지는데, 우리는 앞으로 아래 집합에 속하는 사원수만을 고려할 것이다. 이를 <b>제한된 사원수</b>라고 하자.

<center> <span class="tex-span"><i>a</i>&thinsp;+&thinsp;<i>bi</i>&thinsp;+&thinsp;<i>cj</i>&thinsp;+&thinsp;<i>dk</i></span> (<span class="tex-span"><i>a</i>,&thinsp;<i>b</i>,&thinsp;<i>c</i>,&thinsp;<i>d</i></span>는 <span class="tex-span">0</span> 이상 <span class="tex-span"><i>M</i></span> 미만의 정수) </center>

다음으로 두 사원수의 곱셈에 관하여 생각해 보자. <span class="tex-span"><i>i</i>, &thinsp;<i>j</i>, &thinsp;<i>k</i></span> 사이의 성질 때문에, 두 일반적인 사원수를 곱하면 아래와 같은 결과가 나온다.

<center>
<div style="text-align: left; max-width: 450px;">
<span class="tex-span">(<i>a</i><sub class="lower-index">1</sub>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">1</sub><i>i</i>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">1</sub><i>j</i>&thinsp;+&thinsp;<i>d</i><sub class="lower-index">1</sub><i>k</i>)&thinsp;&times;&thinsp;(<i>a</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">2</sub><i>i</i>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">2</sub><i>j</i>&thinsp;+&thinsp;<i>d</i><sub class="lower-index">2</sub><i>k</i>)<br>
&thinsp;=&thinsp;(<i>a</i><sub class="lower-index">1</sub><i>a</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>b</i><sub class="lower-index">1</sub><i>b</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>c</i><sub class="lower-index">1</sub><i>c</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>d</i><sub class="lower-index">1</sub><i>d</i><sub class="lower-index">2</sub>)&thinsp;+&thinsp;(<i>a</i><sub class="lower-index">1</sub><i>b</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">1</sub><i>a</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">1</sub><i>d</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>d</i><sub class="lower-index">1</sub><i>c</i><sub class="lower-index">2</sub>) <i>i</i><br>
&thinsp;+&thinsp;(<i>a</i><sub class="lower-index">1</sub><i>c</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>b</i><sub class="lower-index">1</sub><i>d</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>c</i><sub class="lower-index">1</sub><i>a</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>d</i><sub class="lower-index">1</sub><i>b</i><sub class="lower-index">2</sub>) <i>j</i>&thinsp;+&thinsp;(<i>a</i><sub class="lower-index">1</sub><i>d</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>b</i><sub class="lower-index">1</sub><i>c</i><sub class="lower-index">2</sub>&thinsp;-&thinsp;<i>c</i><sub class="lower-index">1</sub><i>b</i><sub class="lower-index">2</sub>&thinsp;+&thinsp;<i>d</i><sub class="lower-index">1</sub><i>a</i><sub class="lower-index">2</sub>) <i>k</i></span>
</div>
</center>

우리는 두 제한된 사원수를 곱한 결과를 이 두 사원수를 일반적인 사원수로 취급하여 곱하였을 때의 결과에서 각 정수 성분을 <span class="tex-span"><i>M</i></span>으로 나눈 나머지로 치환한 것으로 생각할 것이다. <span class="tex-span"><i>M</i></span>과 제한된 사원수 <span class="tex-span"><i>A</i></span>가 주어질 때, <span class="tex-span"><i>AB</i>&thinsp;=&thinsp;1</span>이 되는 제한된 사원수 <span class="tex-span"><i>B</i></span> 중 하나를 구하여라.

### 입력 형식

첫 번째 줄에 자연수 <span class="tex-span"><i>M</i></span>과 <span class="tex-span"><i>T</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;100,000</span>)가 공백으로 구분되어 주어진다. <span class="tex-span"><i>M</i></span>은 소수이다. (즉 약수가 1과 자기 자신밖에 없다.)

다음 <span class="tex-span"><i>T</i></span>개의 줄의 각 줄에는 <span class="tex-span"><i>A</i></span>를 나타내는 네 개의 정수 <span class="tex-span"><i>a</i>,&thinsp;<i>b</i>,&thinsp;<i>c</i>,&thinsp;<i>d</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>a</i>,&thinsp;<i>b</i>,&thinsp;<i>c</i>,&thinsp;<i>d</i>&thinsp;&lt;&thinsp;<i>M</i></span>)가 공백으로 구분되어 주어지며, 이 경우 <span class="tex-span"><i>A</i>&thinsp;=&thinsp;<i>a</i>&thinsp;+&thinsp;<i>bi</i>&thinsp;+&thinsp;<i>cj</i>&thinsp;+&thinsp;<i>dk</i></span>이다.

쉬운 문제에서는 <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;7</span>인 입력이 주어진다.

어려운 문제에서는 <span class="tex-span">2&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;100,000</span>인 입력이 주어진다.

### 출력 형식

각 <span class="tex-span"><i>A</i></span>가 주어질 때마다, <span class="tex-span"><i>AB</i>&thinsp;=&thinsp;1</span>을 만족하는 <span class="tex-span"><i>B</i>&thinsp;=&thinsp;<i>a</i>&thinsp;+&thinsp;<i>bi</i>&thinsp;+&thinsp;<i>cj</i>&thinsp;+&thinsp;<i>dk</i></span>들 중 하나를 나타내는 네 개의 정수 <span class="tex-span"><i>a</i>,&thinsp;<i>b</i>,&thinsp;<i>c</i>,&thinsp;<i>d</i></span>를 공백으로 구분하여 <span class="tex-span"><i>T</i></span> 줄에 걸쳐 출력하면 된다. 만약 이런 <span class="tex-span"><i>B</i></span>가 존재하지 않으면 0을 공백으로 구분하여 네 번 출력하면 된다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">5 3<br>
2 3 2 1<br>
3 1 3 2<br>
3 2 4 1
</td>
   <td class="code-font">4 4 1 3<br>
1 3 4 1<br>
0 0 0 0
</td>
  </tr>
 </tbody>
</table>