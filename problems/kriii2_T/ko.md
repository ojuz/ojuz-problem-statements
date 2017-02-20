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

이 세상의 마지막 마법사 재의에게 마지막 순간이 다가오려고 하고 있다. 온갖 자연현상을 이해하고 광대한 마나를 몸에 담아 인간을 초월한 대마법사인 재의도 원인을 알 수 없는 불치병에 대해서는 손을 쓸 수 있는 방법이 없었다. 고통에 몸부림치면서도 재의는 세상에 마법의 맥이 끊어지지 않게 하기 위한 안배를 준비해 왔고, 이제는 마치기 직전에 왔다. 이 안배는 그의 가장 친한 친구인 태현이가 받게 될 것이다.

재의는 필수적으로 수련해야 한다고 여긴 10가지의 마나(0번에서 9번이라고 이름 붙였다.)를 수련할 수 있도록 할 수 있게 했다. 평범한 사람인 태현이는 이 10가지의 마나를 모두 1의 양만큼 가지고 있다. 마나가 증가하게 되는 경우는 총 <span class="tex-span"><i>N</i></span> 가지 있는데, 각 경우를 1에서 <span class="tex-span"><i>N</i></span>까지의 번호를 붙이면 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub>&thinsp;/&thinsp;<i>A</i></span>의 확률로 <span class="tex-span"><i>i</i></span> 번째 경우가 걸린다. <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_T/9a597dcf386491f54b90669976e37803acc532b6.png"/>가 <span class="tex-span"><i>A</i></span>보다 작을 수도 있다.	 즉 수련을 해도 마나가 증가하지 않을 수도 있다. 재의는 수련이 끝난 후에 모든 마나의 양을 곱한 값이 마법의 강한 정도라고 생각하고 있다.

안배를 끝내는 마지막 단계로 재의는 수련을 <span class="tex-span"><i>T</i></span> 번 했을 때 마법의 강한 정도의 기댓값을 구해보고자 한다. 이를 위해 재의는 친하지 않은 친구인 당신에게 이 일을 맡겼다. 불쌍한 재의를 도와주자.

### 입력 형식

첫 번째 줄에 세 자연수 <span class="tex-span"><i>T</i></span>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;10<sup class="upper-index">12</sup></span>), <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>A</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>,&thinsp;<i>A</i>&thinsp;&le;&thinsp;10,000</span>)이 공백으로 구분되어 주어진다.

다음 <span class="tex-span"><i>N</i></span> 개의 줄의 각 줄에는 11개의 정수가 공백으로 구분되어 주어지는데, 가장 첫 번째 정수는 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>를 의미하는 정수이고, 나머지 10개의 정수는 각각 0번 마나의 증가량, 1번 마나의 증가량, ..., 9번 마나의 증가량을 의미한다. 모든 <span class="tex-span"><i>P</i><sub class="lower-index"><i>i</i></sub></span>의 합이 <span class="tex-span"><i>A</i></span> 이하임은 보장되며, 마나의 증가량은 0 이상 9,999 이하의 정수로 적어도 하나는 1 이상이다.

쉬운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>(N+1)</i><sup class="upper-index"><i>T</i></sup>&thinsp;&le;&thinsp;1,000,000</span>을 만족하는 입력이 주어진다.

어려운 문제에서는 별 다른 제약이 없다.

### 출력 형식

첫 번째 줄에 <span class="tex-span"><i>T</i></span>번의 수련을 마치고 난 후 10가지 마나의 양을 모두 곱한 값의 기댓값을 출력한다. <strong>이 값에 <span class="tex-span"><i>A</i><sup class="upper-index"><i>T</i></sup></span>를 곱한 값은 정수가 되는 것이 보장되므로, <span class="tex-span"><i>A</i><sup class="upper-index"><i>T</i></sup></span>를 곱한 후 1,000,000,007로 나눈 나머지를 출력한다.</strong>

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">1 2 3<br>
1 1 1 1 1 0 0 0 0 0 0<br>
1 0 0 0 0 1 0 0 0 0 0
</td>
   <td class="code-font">19
</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">10 3 22<br>
4 1 4 2 5 0 0 0 1 0 1<br>
7 2 0 3 2 0 7 1 0 2 0<br>
9 0 1 0 0 1 0 1 1 7 0
</td>
   <td class="code-font">313884062
</td>
  </tr>
 </tbody>
</table>
