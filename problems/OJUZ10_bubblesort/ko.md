버블 정렬이란, 두 인접한 원소를 검사하여 자리를 바꾸는 방식으로 길이가 <span class="tex-span"><i>N</i></span>인 수열을 정렬하는 알고리즘이다. 버블 정렬은 아래와 같은 단계를 총 <span class="tex-span"><i>N</i></span>번 진행하면 된다.


- 첫 번째 값과 두 번째 값을 비교하여 첫 번째 값이 더 크면 자리를 바꾼다.
- 두 번째 값과 세 번째 값을 비교하여 두 번째 값이 더 크면 자리를 바꾼다.
- …
- <span class="tex-span"><i>N</i>&thinsp;-&thinsp;1</span>번째 값과 <span class="tex-span"><i>N</i></span>번째 값을 비교하여 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;1</span>번째 값이 더 크면 자리를 바꾼다.


세찬이는 버블 정렬의 결과는 당연히 알기에 버블 정렬의 중간 과정을 알아보려고 한다. 하지만 <span class="tex-span"><i>N</i></span>이 매우 크므로 위와 같은 단계를 <span class="tex-span"><i>K</i></span>번 하면 시간이 오래 걸린다. 세찬이를 도와 버블 정렬의 중간 과정을 구하는 프로그램을 작성하여라.

### 입력 형식

첫 번째 줄에는 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>K</i></span>가 주어진다.

두 번째 줄에는 처음 수열의 상태가 주어진다. 즉, 처음 수열을 이루는 <span class="tex-span"><i>N</i></span>개의 정수가 공백을 사이로 두고 차례대로 주어진다.

### 출력 형식

위 단계를 <span class="tex-span"><i>K</i></span>번 한 후 수열의 상태를 출력한다.

### 부분문제

모든 채점 데이터에 대해,

* <span class="tex-span"><i>N</i>&thinsp;&ge;&thinsp;1</span>
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;<i>N</i></span>
* 수열의 각 항은 1 이상 1,000,000,000 이하의 정수이다.


<div class="row">
<div style="min-width: 320px;" class="col-mg-7 col-sm-7 col-lg-7">
<div class="table-responsive">
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
   <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
   <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>N</i></span></th>
   <th class="col-sm-3 col-md-3 col-lg-3">비고</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">1</td>
   <td class="code-font">11</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;50</span></td>
   <td>-</td>
  </tr>
  <tr>
   <td class="code-font">2</td>
   <td class="code-font">23</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;2,&thinsp;000</span></td>
   <td>-</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">47</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;100,&thinsp;000</span></td>
   <td>수열의 각 항은 서로 다르다.</td>
  </tr>
  <tr>
   <td class="code-font">4</td>
   <td class="code-font">19</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;100,&thinsp;000</span></td>
   <td>-</td>
  </tr>
 </tbody>
</table>
</div>
</div>
</div>

### 입력과 출력의 예

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">4 1<br>
62 23 32 15</td>
   <td class="code-font">23 32 15 62</td>
  </tr>
 </tbody>
</table>