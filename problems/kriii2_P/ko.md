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

**피보나치(Fibonacci) 수**는 아래의 점화식으로 정의되는 수열이다.

<center>
<img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_P/fibdef.png"/>
</center>

피보나치 수와 <span class="tex-span"><i>x</i><sup class="upper-index">2</sup>&thinsp;=&thinsp;<i>x</i>&thinsp;+&thinsp;1</span>의 두 근 중 하나인 황금비 <img align="middle" class="tex-formula" src="http://espresso.codeforces.com/a446282ddf3ca6973cc9c7fdba1ad786fac664e6.png"/>는 매우 연관이 깊은 수이다. 이에 관한 예를 들자면 피보나치 수의 일반항을 <img align="middle" class="tex-formula" src="http://espresso.codeforces.com/7e0effa09eb89f6b24fab5743e84cba3b333828d.png"/>로 나타낼 수 있다는 점 등이 있다. 이제 <span class="tex-span">&phi;</span>를 이용해 **파이보나치(Phibonacci) 수**를 아래의 점화식으로 정의하고자 한다.

<center>
<img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_P/phibdef.png"/>
</center>

편의를 위해 <span class="tex-span"><i>F</i><sub class="lower-index">-1</sub>&thinsp;=&thinsp;1</span>이라고 하면, 놀랍게도 <span class="tex-span"><i>P</i><sub class="lower-index"><i>n</i></sub>&thinsp;=&thinsp;<i>F</i><sub class="lower-index"><i>n</i></sub>&phi;&thinsp;+&thinsp;<i>F</i><sub class="lower-index"><i>n</i>&thinsp;-&thinsp;1</sub></span> (<span class="tex-span"><i>n</i>&thinsp;&ge;&thinsp;0</span>)로 나타낼 수 있다! 이제 우리가 관심 있는 것은 <span class="tex-span">(<i>P</i><sub class="lower-index"><i>n</i></sub>)<sup class="upper-index"><i>k</i></sup></span>를 두 정수 <span class="tex-span"><i>A</i></span>, <span class="tex-span"><i>B</i></span>를 이용해 <span class="tex-span"><i>A</i>&phi;<sup class="upper-index"><i>k</i></sup>&thinsp;+&thinsp;<i>B</i></span> 꼴로 표현할 수 있느냐는 것이다. 표현 가능하다면, <span class="tex-span"><i>A</i></span>와 <span class="tex-span"><i>B</i></span>를 출력하고, 불가능하다면 -1을 출력하라.

### 입력 형식

첫 번째 줄에 두 정수 <span class="tex-span"><i>n</i></span> (<span class="tex-span">0&thinsp;&le;&thinsp;<i>n</i>&thinsp;&le;&thinsp;10<sup class="upper-index">12</sup></span>), <span class="tex-span"><i>k</i></span>가 공백으로 구분되어 주어진다. 

쉬운 문제에서는 <span class="tex-span"><i>k</i>&thinsp;=&thinsp;1</span>인 입력이 주어진다. 

어려운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&le;&thinsp;10<sup class="upper-index">12</sup></span>인 입력이 주어진다.

### 출력 형식

첫 번째 줄에 <span class="tex-span">(<i>P</i><sub class="lower-index"><i>n</i></sub>)<sup class="upper-index"><i>k</i></sup>&thinsp;=&thinsp;<i>A</i>&phi;<sup class="upper-index"><i>k</i></sup>&thinsp;+&thinsp;<i>B</i></span>가 되는 두 정수 <span class="tex-span"><i>A</i></span>, <span class="tex-span"><i>B</i></span>를 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 공백으로 구분하여 출력한다. 만약 이런 두 정수가 존재하지 않는 경우 -1을 출력한다

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font"> 5 1 </td>
   <td class="code-font">5 3</td>
  </tr>	
  <tr>
   <td style="width: 50%;" class="code-font"> 3 2 </td>
   <td class="code-font">8 1000000004</td>
  </tr>	
 </tbody>
</table>

두 번째 예제의 경우 <span class="tex-span">(<i>P</i><sub class="lower-index">3</sub>)<sup class="upper-index">2</sup> = (2&phi;+1)<sup class="upper-index">2</sup> = 4&phi;<sup class="upper-index">2</sup>+4&phi;+1 = 8&phi;<sup class="upper-index">2</sup>-3</span>이며, <span class="tex-span">-3</span>을 <span class="tex-span">1,000,000,007</span>로 나눈 나머지는 <span class="tex-span">1,000,000,004</span>이므로, 위와 같은 출력이 나온다.