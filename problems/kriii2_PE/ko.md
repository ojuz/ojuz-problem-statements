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

제2회 kriiICPC의 페널티 계산 방식은 너무 복잡하다. 따라서 운영진은 여러분에게 페널티 계산을 맡기고자 한다.

당신이 어느 한 문제에 답안을 <span class="tex-span"><i>n</i></span>개 제출했다고 하자. 이 중 <span class="tex-span"><i>i</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>n</i></span>) 답안은 대회가 시작한 지 <span class="tex-span"><i>t</i><sub class="lower-index"><i>i</i></sub></span>분 뒤에 제출하였고, 채점 결과 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>점을 받았다고 가정하자. 

이 문제에 대한 페널티 <span class="tex-span"><i>P</i></span>는 다음과 같이 계산한다. 우선, <span class="tex-span">max{<i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>s</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>s</i><sub class="lower-index"><i>n</i></sub>}&thinsp;=&thinsp;<i>s</i><sub class="lower-index"><i>k</i></sub></span>를 만족하는 가장 작은 <span class="tex-span"><i>k</i></span> (즉, 가장 높은 점수를 받은 답안들 중 가장 빨리 제출한 것의 번호)를 <span class="tex-span"><i>f</i></span>로 두자. 이제 <span class="tex-span"><i>P</i></span>는 아래 공식을 이용하여 계산할 수 있다.

* <span class="tex-span"><i>s</i><sub class="lower-index"><i>f</i></sub>&thinsp;=&thinsp;0</span> : <span class="tex-span"><i>P</i>&thinsp;=&thinsp;0</span>
* <span class="tex-span"><i>s</i><sub class="lower-index"><i>f</i></sub>&thinsp;=&thinsp;1</span> 또는 <span class="tex-span"><i>s</i><sub class="lower-index"><i>f</i></sub>&thinsp;=&thinsp;4</span> : <span class="tex-span"><i>P</i>&thinsp;=&thinsp;<i>t</i><sub class="lower-index"><i>f</i></sub>&thinsp;+&thinsp;(<i>f</i>&thinsp;-&thinsp;1)&thinsp;&times;&thinsp;20</span>

당신이 어느 한 문제에 제출한 답안들의 정보가 주어질 때, 이 문제에서 받는 페널티를 계산하는 프로그램을 작성하라.

### 입력 형식

첫 번째 줄에 이 문제에 제출한 답안의 수 <span class="tex-span"><i>n</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>n</i>&thinsp;&le;&thinsp;100</span>)이 주어진다.

이후 <span class="tex-span"><i>n</i></span>개의 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span>번째 (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>n</i></span>)번째 줄에는 두 개의 정수 <span class="tex-span"><i>t</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어진다. <span class="tex-span">1&thinsp;&le;&thinsp;<i>t</i><sub class="lower-index">1</sub>&thinsp;&lt;&thinsp;<i>t</i><sub class="lower-index">2</sub>&thinsp;&lt;&thinsp;...&thinsp;&lt;&thinsp;<i>t</i><sub class="lower-index"><i>n</i></sub>&thinsp;&le;&thinsp;300</span>, <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_PE/3b1e58b06d4ac8944976a4d01a8938c2ba18c4bd.png"/>임이 보장된다.

쉬운 문제에서는 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_PE/7e81625a2ddf947291b2ea827a1cbfa282ab2f0c.png"/>이다.

어려운 문제에서는 추가 제약 조건이 없다.

### 출력 형식

첫 번째 줄에 <span class="tex-span"><i>P</i></span>의 값을 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">1<br>
300 4</td>
   <td class="code-font">300</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">2<br>
1 1<br>
2 4</td>
   <td class="code-font">22</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">4<br>
1 0<br>
2 1<br>
3 0<br>
5 4</td>
   <td class="code-font">65</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">3<br>
1 0<br>
10 0<br>
100 0</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>