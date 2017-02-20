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

형석이는 너무 심심했기 때문에 큰 원 위에 일정한 간격으로 <span class="tex-span"><i>N</i></span>개의 못을 박았다. 그리고 어느 한 못을 <span class="tex-span"><i>P</i><sub class="lower-index">0</sub></span>라고 하고, 이 못에서부터 시계방향으로 다른 못들을 <span class="tex-span"><i>P</i><sub class="lower-index">1</sub></span>에서 <span class="tex-span"><i>P</i><sub class="lower-index"><i>N</i>&thinsp;-&thinsp;1</sub></span>이라고 이름 붙였다. 그리고 이 못들을 철사로 연결하는 놀이를 시작했다. 얼마간 이 놀이를 반복하던 형석이는 그렸던 철사들을 모두 없애고 다음과 같이 철사를 연결하기로 했다.

1. <span class="tex-span"><i>Q</i><sub class="lower-index">0</sub>&thinsp;=&thinsp;<i>P</i><sub class="lower-index">0</sub></span>이라고 하자. 그리고 다음을 1단계에서부터 <span class="tex-span"><i>N</i><sup class="upper-index">2</sup></span>단계까지 반복한다. 
2. <span class="tex-span"><i>p</i></span> 단계에서는 <span class="tex-span"><i>Q</i><sub class="lower-index"><i>p</i>&thinsp;-&thinsp;1</sub>&thinsp;=&thinsp;<i>P</i><sub class="lower-index"><i>k</i></sub></span>이면, <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_W/eq1.png"/>으로 하여, <span class="tex-span"><i>Q</i><sub class="lower-index"><i>p</i>&thinsp;-&thinsp;1</sub></span>에서 <span class="tex-span"><i>Q</i><sub class="lower-index"><i>p</i></sub></span>까지를 철사로 연결한다. 만약 이미 두 못 이미 연결되어 있다면 연결하지 않는다. 또한, <span class="tex-span"><i>Q</i><sub class="lower-index"><i>p</i>&thinsp;-&thinsp;1</sub></span>과 <span class="tex-span"><i>Q</i><sub class="lower-index"><i>p</i></sub></span>가 같은 못이라면 연결하지 않는 것으로 취급한다.

형석이가 연결하게 될 철사의 개수는 몇 개가 될 것인지 구해주자.

### 입력 형식

첫 번째 줄에 자연수 <span class="tex-span"><i>N</i></span>이 주어진다.

쉬운 문제에서는 <span class="tex-span">3&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;1,000</span>인 입력이 주어진다.

어려운 문제에서는 <span class="tex-span">3&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;10<sup class="upper-index">12</sup></span>인 입력이 주어진다.

### 출력 형식

첫 번째 줄에 형석이가 연결하게 될 철사의 개수를 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">3</td>
   <td class="code-font">1</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">4</td>
   <td class="code-font">3</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">5</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>