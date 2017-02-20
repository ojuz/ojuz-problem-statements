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

<span class="tex-span">2</span>차원 세상에는 <span class="tex-span">1</span>에서 <span class="tex-span"><i>N</i></span>까지의 번호가 붙은 <span class="tex-span"><i>N</i></span>개의 신호소가 있다. 신호소 <span class="tex-span"><i>i</i></span>는 어떤 좌표 <span class="tex-span">(<i>x</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>y</i><sub class="lower-index"><i>i</i></sub>)</span>를 중심으로 하는 원 영역에 신호를 보낼 수 있는데, 신호소에 들어오게 되는 전력량에 따라 그 세기와 반경이 달라진다. 정확히는 신호소 <span class="tex-span"><i>i</i></span>는 <span class="tex-span">(<i>i</i>,&thinsp;1),&thinsp;...,&thinsp;(<i>i</i>,&thinsp;<i>M</i><sub class="lower-index"><i>i</i></sub>)</span>로 이름 붙여진 <span class="tex-span"><i>M</i><sub class="lower-index"><i>i</i></sub></span>개의 서로 다른 신호를 보낼 수 있다. 신호 <span class="tex-span">(<i>i</i>,&thinsp;<i>j</i>)</span>는 <span class="tex-span"><i>r</i><sub class="lower-index"><i>i</i>,&thinsp;<i>j</i></sub></span>의 반경을 가지는 세기 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i>,&thinsp;<i>j</i></sub></span>의 신호이며, <span class="tex-span"><i>w</i><sub class="lower-index"><i>i</i>,&thinsp;<i>j</i></sub></span>이상의 전력이 신호소 <span class="tex-span"><i>i</i></span>에 들어오게 될 때 무조건적으로  신호를 보내게 되어 있다.

어떤 좌표 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>에 전해지는 신호의 세기는 현재 존재하는 신호들 중에서 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>를 포함하는 신호들 중 세기가 가장 큰 신호의 세기가 된다. 정부는 아래의 값 <span class="tex-span"><i>A</i></span>가 신호가 세상에 퍼진 정도를 나타낼 수 있다고 생각한다.

<center><BIG> <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_R/eq1.png"/> (신호 세기 <span class="tex-span"><i>s</i></span>) <span class="tex-span">&thinsp;&times;&thinsp;</span> (신호 세기가 <span class="tex-span"><i>s</i></span>인 부분의 넓이)</BIG> </center>

그리고 얼마 전부터 정부는 정책적으로 신호소 <span class="tex-span"><i>i</i></span>에 들일 전력량을 매일 <span class="tex-span">[<i>L</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>U</i><sub class="lower-index"><i>i</i></sub>]</span> 구간의 정수 중 하나를 동일한 확률로 선택한다. 이 때 <span class="tex-span"><i>A</i></span>의 기댓값을 구하여 보자.

### 입력 형식

첫 번째 줄에 신호소의 개수를 의미하는 자연수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;20</span>)이 주어진다.

다음에는 <span class="tex-span"><i>N</i></span>개의 신호소에 대한 정보가 주어진다. 각 신호소 마다 첫 번째 줄에는 다섯 개의 정수 <span class="tex-span"><i>x</i></span>, <span class="tex-span"><i>y</i></span> (<span class="tex-span">&thinsp;-&thinsp;10<sup class="upper-index">4</sup>&thinsp;&le;&thinsp;<i>x</i>,&thinsp;<i>y</i>&thinsp;&le;&thinsp;10<sup class="upper-index">4</sup></span>), <span class="tex-span"><i>M</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;20</span>), <span class="tex-span"><i>L</i></span>, <span class="tex-span"><i>U</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>L</i>&thinsp;&le;&thinsp;<i>U</i>&thinsp;&le;&thinsp;10<sup class="upper-index">4</sup></span>)가 공백으로 구분되어 주어지고 다음 <span class="tex-span"><i>M</i></span>개의 줄에는 세 개의 정수 <span class="tex-span"><i>r</i></span> ,<span class="tex-span"><i>s</i></span> ,<span class="tex-span"><i>w</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>r</i>,&thinsp;<i>s</i>,&thinsp;<i>w</i>&thinsp;&le;&thinsp;10<sup class="upper-index">4</sup></span>)가 공백으로 구분되어 주어진다.

쉬운 문제에서는 모든 신호소에 대해 <span class="tex-span"><i>M</i> = 1</span>인 입력이 주어진다.

어려운 문제에서는 별 다른 제약이 없다.

### 출력 형식

<span class="tex-span"><i>A</i></span>의 기댓값을 출력한다. 정답과의 절대오차 혹은 상대오차가 <span class="tex-span">&thinsp;10<sup class="upper-index">-8</sup></span>이하인 경우 정답으로 인정된다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2<br>
0 0 2 1 2<br>
1 2 1<br>
2 1 2<br>
1 0 2 1 2<br>
1 2 1<br>
2 1 2</td>
   <td class="code-font">16.732780900043</td>
  </tr>	
  <tr>
   <td style="width: 50%;" class="code-font">2<br>
0 0 1 1 2<br>
1 1 2<br>
0 0 1 1 2<br>
1 1 2
</td>
   <td class="code-font">2.356194490192</td>
  </tr>	
 </tbody>
</table>