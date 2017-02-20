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

Mirko는 수학 시간에 산술 연산들을 연습하고 있습니다. 우선, 그는 정수들로 구성된 수열 <span class="tex-span"><i>A</i></span>를 적습니다. 그 다음, 첫 번째 수열을 이용해, 그는 또다른 정수로 구성된 수열 <span class="tex-span"><i>B</i></span>를 적습니다. 이 수열은 수열 <span class="tex-span"><i>A</i></span>의 모든 수들을 그 수 이전(자신 포함)에 적혀 있는 수들의 평균으로 대체하면 만들 수 있습니다.

예를 들어, 만약 수열 <span class="tex-span"><i>A</i></span>가 아래와 같다면

<center>
<span class="tex-span">1, 3, 2, 6, 8,</span>
</center>

수열 <span class="tex-span"><i>B</i></span>는 아래와 같을 것입니다.

<center>
<img align="middle" class="tex-formula" src="http://geniusainta.hubweb.net/problems/COCI14_prosjek/6fb79974d50ffb0bf5916c8d517a59e99e10cafc.png"/>
</center>

다시 말해,

<center>
<span class="tex-span">1, 2, 2, 3, 4,</span>
</center>

와 같습니다.

여러분에게 수열 <span class="tex-span"><i>B</i></span>가 주어집니다. Mirko의 계산이 올바른지 확인하기 위해 수열 <span class="tex-span"><i>A</i></span>를 찾으세요.

### 입력 형식

첫 번째 줄에는 수열 <span class="tex-span"><i>B</i></span>의 길이 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>)이 주어집니다.

두 번째 줄에는 <span class="tex-span"><i>N</i></span>개의 공백으로 구분된 정수들 <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;10<sup class="upper-index">9</sup></span>)가 주어집니다.

### 출력 형식

첫 번째 줄에 <span class="tex-span"><i>N</i></span>개의 정수들 <span class="tex-span"><i>A</i><sub class="lower-index"><i>i</i></sub></span>를 공백으로 구분하여 출력합니다. 

**주의**: 입력 데이터는 <span class="tex-span"><i>A</i></span>의 원소들이 정수가 되도록 주어질 것입니다.

### 예제

<table class="table table-bordered table-condensed">
 <thead>
 <tr>
  <th style="width: 50%;">예제 입력</th>
  <th>예제 출력</th>
 </tr>
 </thead>
 <tbody>
 <tr>
  <td class="code-font">1<br>2
  </td>
  <td class="code-font">2
  </td>
 </tr>
 <tr>
  <td class="code-font">4<br>3 2 3 5
  </td>
  <td class="code-font">3 1 5 11
  </td>
 </tr>
 <tr>
  <td class="code-font">5<br>1 2 2 3 4
  </td>
  <td class="code-font">1 3 2 6 8
  </td>
 </tr>
 </tbody>
</table>