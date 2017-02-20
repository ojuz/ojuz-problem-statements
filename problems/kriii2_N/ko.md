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
축에 평행한 <span class="tex-span"><i>N</i></span>-orthotope란 다음에 속하는 어떤 <span class="tex-span"><i>N</i></span> 차원 점들의 집합이다.

<center> <big> <span class="tex-span">[<i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>e</i><sub class="lower-index">1</sub>]&thinsp;&times;&thinsp;[<i>s</i><sub class="lower-index">2</sub>,&thinsp;<i>e</i><sub class="lower-index">2</sub>]&thinsp;&times;&thinsp;...&thinsp;&times;&thinsp;[<i>s</i><sub class="lower-index"><i>N</i></sub>,&thinsp;<i>e</i><sub class="lower-index"><i>N</i></sub>]</span> (<span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>e</i><sub class="lower-index"><i>i</i></sub></span>)</big><br>
(즉, <span class="tex-span"><i>N</i></span>차원 점 <span class="tex-span">(<i>x</i><sub class="lower-index">1</sub>,&thinsp;<i>x</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>x</i><sub class="lower-index"><i>N</i></sub>)</span>의 각 <span class="tex-span"><i>x</i><sub class="lower-index"><i>i</i></sub></span> 가 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>e</i><sub class="lower-index"><i>i</i></sub></span> 인 점들의 집합이다.)</center>

<span class="tex-span"><i>N</i>&thinsp;=&thinsp;0</span>인 경우는 특별히 0차원의 점이라고 정의하자. <br>
<span class="tex-span"><i>N</i>&thinsp;=&thinsp;1</span>인 경우는 1차원에서 어느 선분을 의미한다. <br>
<span class="tex-span"><i>N</i>&thinsp;=&thinsp;2</span>인 경우는 2차원에서 축에 평행한 어느 직사각형 형태의 영역이 된다. <br>
<span class="tex-span"><i>N</i>&thinsp;=&thinsp;3</span>인 경우는 3차원에서 축에 평행한 어느 직육면체 형태의 영역이 된다. <br>
...

조금 더 일반화하면,

<center> <big> <span class="tex-span">[<i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>e</i><sub class="lower-index">1</sub>]&thinsp;&times;&thinsp;[<i>s</i><sub class="lower-index">2</sub>,&thinsp;<i>e</i><sub class="lower-index">2</sub>]&thinsp;&times;&thinsp;...&thinsp;&times;&thinsp;[<i>s</i><sub class="lower-index"><i>K</i></sub>,&thinsp;<i>e</i><sub class="lower-index"><i>K</i></sub>]</span> (<span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;<i>e</i><sub class="lower-index"><i>i</i></sub></span>)</big> </center>

를 만족하는 점들은 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>e</i><sub class="lower-index"><i>i</i></sub></span>를 만족하는 <span class="tex-span"><i>i</i></span>의 개수가 <span class="tex-span"><i>N</i></span>개라면 축에 평행한 <span class="tex-span"><i>N</i></span>-orthotope가 된다. 앞으로 '평행한'을 생략할 것이지만 앞으로 등장하는 orthotope도 평행한 orthotope라고 생각하면 된다.

어떤 <span class="tex-span"><i>N</i></span>에 대해 두 개의 <span class="tex-span"><i>N</i></span>-orthotope가 주어져 있다고 하자. 이때 두 영역에 동시에 속하는 점들이 있다면, 이 점들은 축에 <span class="tex-span"><i>M</i></span>-orthotope가 된다. 이때 <span class="tex-span"><i>M</i></span>이 무엇인지 구하는 프로그램을 작성하라. 예를 들어 <span class="tex-span">2</span>-orthotope의 경우 아래의 네 가지 경우가 있을 수 있다.

<center>
 <a class="thumbnail">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_N/ex.png">
 </a>
</center>

**A**는 두 2-orthotope의 공통된 영역이 똑같이 2-orthotope가 되는 경우이다. <br>
**B**는 두 2-orthotope의 공통된 영역이 1-orthotope(선분)가 되는 경우이다.<br>
**C**는 두 2-orthotope의 공통된 영역이 0-orthotope(점)가 되는 경우이다.<br>
**D**는 두 2-orthotope의 공통된 영역이 없는 경우이다. 이 경우 -1을 출력하면 된다.

### 입력 형식

첫 번째 줄에 자연수 <span class="tex-span"><i>N</i></span>이 주어진다.

두 번째 줄에는 첫 번째 영역의 <span class="tex-span"><i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>e</i><sub class="lower-index">1</sub>,&thinsp;<i>s</i><sub class="lower-index">2</sub>,&thinsp;<i>e</i><sub class="lower-index">2</sub>,&thinsp;?,&thinsp;<i>s</i><sub class="lower-index"><i>N</i></sub>,&thinsp;<i>e</i><sub class="lower-index"><i>N</i></sub></span>이 공백으로 구분되어 주어진다.

세 번째 줄에는 두 번째 영역의 <span class="tex-span"><i>s</i><sub class="lower-index">1</sub>,&thinsp;<i>e</i><sub class="lower-index">1</sub>,&thinsp;<i>s</i><sub class="lower-index">2</sub>,&thinsp;<i>e</i><sub class="lower-index">2</sub>,&thinsp;?,&thinsp;<i>s</i><sub class="lower-index"><i>N</i></sub>,&thinsp;<i>e</i><sub class="lower-index"><i>N</i></sub></span>이 공백으로 구분되어 주어진다.

이 수들은 모두 절댓값이 <span class="tex-span">11</span> 이하이며, 각 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub></span>, <span class="tex-span"><i>e</i><sub class="lower-index"><i>i</i></sub></span>는 <span class="tex-span"><i>s</i><sub class="lower-index"><i>i</i></sub>&thinsp;&lt;&thinsp;<i>e</i><sub class="lower-index"><i>i</i></sub></span>를 만족한다.

쉬운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;2</span>인 입력이 주어진다.

어려운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;11</span>인 입력이 주어진다.

### 출력 형식

첫 번째 줄에 두 영역의 공통된 영역이 <span class="tex-span"><i>M</i></span>-orthotope이면 <span class="tex-span"><i>M</i></span>을 출력한다. 단 공통된 영역이 없는 경우 -1을 출력한다.

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
0 5 0 5<br>
2 9 2 9
</td>
   <td class="code-font">2</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">2<br>
0 5 0 5<br>
5 10 5 10
</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>
