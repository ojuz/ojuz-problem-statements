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

당신에게 <span class="tex-span"><i>R</i></span> 행 <span class="tex-span"><i>C</i></span> 열의 행렬이 주어질 것이다. 행렬의 각 칸에는 하나의 정수가 적혀 있으며, 당신은 행렬에 다음의 네 가지 연산을 할 수 있다.

<div class="table-responsive">
<table class="table table-bordered">
 <thead>
  <tr>
   <th class="col-sm-4 col-md-4 col-lg-4">연산</th>
   <th class="col-sm-2 col-md-2 col-lg-2">표기법</th>
   <th class="col-sm-6 col-md-6 col-lg-6">예</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="vertical-align: middle;">행렬의 <span class="tex-span"><i>i</i></span> 번째 행을 <span class="tex-span"><i>k</i></span> 칸 오른쪽으로 회전시킨다.<br/>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>R</i>,&thinsp;1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&lt;&thinsp;<i>C</i></span>)</td>
   <td style="vertical-align: middle;">rotR <span class="tex-span"><i>i</i></span> <span class="tex-span"><i>k</i></span></td>
   <td style="vertical-align: middle;">rotR 3 1　　<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_S/exrotR.png"></td>
  </tr>
  <tr>
   <td style="vertical-align: middle;">행렬의 <span class="tex-span"><i>j</i></span> 번째 열을 <span class="tex-span"><i>k</i></span> 칸 아래로 회전시킨다.<br/>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>C</i>,&thinsp;1&thinsp;&le;&thinsp;<i>k</i>&thinsp;&lt;&thinsp;<i>R</i></span>)</td>
   <td style="vertical-align: middle;">rotC <span class="tex-span"><i>j</i></span> <span class="tex-span"><i>k</i></span></td>
   <td style="vertical-align: middle;">rotC 1 2　　<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_S/exrotC.png"></td>
  </tr>
  <tr>
   <td style="vertical-align: middle;">행렬의 <span class="tex-span"><i>i</i></span> 번째 행의 모든 원소에 -1을 곱한다.<br/>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>R</i></span>)</td>
   <td style="vertical-align: middle;">negR <span class="tex-span"><i>i</i></span></td>
   <td style="vertical-align: middle;">negR 2　　<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_S/exnegR.png"></td>
  </tr>
  <tr>
   <td style="vertical-align: middle;">행렬의 <span class="tex-span"><i>j</i></span> 번째 열의 모든 원소에 -1을 곱한다.<br/>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>j</i>&thinsp;&le;&thinsp;<i>C</i></span>)</td>
   <td style="vertical-align: middle;">negC <span class="tex-span"><i>j</i></span></td>
   <td style="vertical-align: middle;">negC 2　　<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_S/exnegC.png"></td>
  </tr>
 </tbody>
</table>
</div>

<span class="tex-span">50,000</span>번 이하의 연산을 사용하여 행렬의 모든 원소의 합을 최대화하는 프로그램을 작성하라.

### 입력 형식

첫 번째 줄에 두 자연수 <span class="tex-span"><i>R</i></span>, <span class="tex-span"><i>C</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>R</i>,&thinsp;<i>C</i>&thinsp;&le;&thinsp;100</span>)가 공백으로 구분되어 주어진다.

다음 <span class="tex-span"><i>R</i></span>개의 줄의 각 줄에는 <span class="tex-span"><i>C</i></span>개의 정수가 공백으로 구분되어 주어진다. 각 정수의 절댓값은 <span class="tex-span">10<sup class="upper-index">4</sup></span>을 넘지 않는다.

### 출력 형식

첫 번째 줄에 최대화된 원소 합과 이 행렬을 만드는 데 필요한 연산의 횟수(<span class="tex-span"><i>T</i></span>)를 공백으로 구분하여 출력한다. 만약 연산의 횟수가 <span class="tex-span">50,000</span>번을 초과한다면 무조건 정답으로 인정되지 않는다.

다음 <span class="tex-span"><i>T</i></span>개의 줄에는 사용한 연산을 순서대로 위의 **표기법**을 이용하여 출력한다. 출력된 인자의 범위가 비정상적인 경우 오답으로 처리된다.

쉬운 문제에서는 연산을 제대로 출력하지 않고 최대화된 원소의 합만 맞아도 정답으로 인정된다.

어려운 문제에서는 출력된 순서대로 연산한 후에 행렬의 모든 원소의 합이 최대화가 되지 않으면 정답으로 인정되지 않는다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">3 4<br>
1 -2 5 200<br>
-8 0 -4 -10<br>
11 4 0 100</td>
   <td class="code-font">345 2<br>
rotC 2 1<br>
negR 2</td>
  </tr>
 </tbody>
</table>