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

<span class="tex-span"><i>N</i></span>개의 부서를 하나의 부서로 합치고자 한다. 이 부서들에 <span class="tex-span">1</span>에서 <span class="tex-span"><i>N</i></span>까지의 번호를 붙이고, 부서 <span class="tex-span"><i>i</i></span>의 크기를 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>라고 하도록 하자. 한 번에 많은 부서를 합치면 혼란이 커질 것이라고 예상되었기 때문에, 두 개의 부서를 하나로 합치는 것을 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;1</span>번 반복하여 통합된 하나의 부서를 만들기로 하였다. 반복하는 과정은 아래와 같다.

1. 남은 부서들 중에 하나의 부서 <span class="tex-span"><i>a</i></span>를 정한다.
2. 남은 부서들 중에 <span class="tex-span"><i>a</i></span>가 아닌 하나의 부서 <span class="tex-span"><i>b</i></span>를 정한다. 
3. 두 부서 <span class="tex-span"><i>a</i></span>와 <span class="tex-span"><i>b</i></span>를 합친다. <span class="tex-span"><i>S</i><sub class="lower-index"><i>a</i></sub></span>는 <span class="tex-span"><i>S</i><sub class="lower-index"><i>a</i></sub>&thinsp;+&thinsp;<i>S</i><sub class="lower-index"><i>b</i></sub></span>가 되며, 부서 <span class="tex-span"><i>b</i></span>는 사라진다. 
4. 합친 부서의 쌍 <span class="tex-span">(<i>a</i>,&thinsp;<i>b</i>)</span>를 현재까지 기록된 합친 부서 쌍의 목록의 가장 뒤에 붙인다.

두 부서를 합치는 데에는 비용이 발생한다. 이때 합치는 방법에 따라 드는 비용이 다르지만 우리는 비용이 <span class="tex-span"><i>S</i><sub class="lower-index"><i>a</i></sub>&thinsp;&times;&thinsp;<i>S</i><sub class="lower-index"><i>b</i></sub></span>인 방법을 알고 있고, 이를 사용할 것이다. 이때 드는 총비용의 최솟값과, 최소한의 비용이 들게 하는 서로 다른 과정의 가짓수를 구해보자. 두 과정이 서로 다르다는 것은, 기록된 쌍들을 순서대로 하나씩 비교했을 때 한 쌍이라도 다르다는 것이다.

### 입력 형식

첫 번째 줄에 부서의 수를 의미하는 자연수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100,000</span>)이 주어진다.

두 번째 줄에는 각 부서의 크기를 의미하는 <span class="tex-span"><i>N</i></span>개의 자연수 <span class="tex-span"><i>S</i><sub class="lower-index">1</sub>,&thinsp;<i>S</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>S</i><sub class="lower-index"><i>N</i></sub></span>이 공백으로 구분되어 주어진다. 이 수들은 <span class="tex-span">1</span> 이상 <span class="tex-span">100</span> 이하이다.

### 출력 형식

첫 번째 줄에는 총비용의 최솟값을 출력한다.

두 번째 줄에는 최소한의 비용이 들게 하는 서로 다른 과정의 가짓수를 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력한다.

쉬운 문제에서는 첫 번째 줄만 맞으면 정답으로 인정된다. 

어려운 문제에서는 두 번째 줄도 맞아야 정답으로 인정된다.

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
2 3</td>
   <td class="code-font">6<br>
2</td>
  </tr>
 </tbody>
</table>

<span class="tex-span">(1,2)</span>와 <span class="tex-span">(2,1)</span>은 서로 다른 경우이다.