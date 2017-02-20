<span class="tex-span"><i>N</i></span>명의 사람들이 꿀을 먹고 싶어 하는데, 각 사람들은 <span class="tex-span"><i>H</i><sub class="lower-index"><i>i</i></sub></span>만큼의 꿀을 먹으려고 한다.

마법사 프니는 <span class="tex-span"><i>N</i></span>명의 사람들 중 2명의 사람들을 꿀벌로 변신시켜서 그 두 벌이 나머지 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;2</span>명의 사람들이 먹을 꿀을 만들게 하려고 한다. 한편, 각 사람들은 귀여운 정도가 다르기 때문에 꿀벌로 변신한 상태에서 꿀을 만드는 능력이 다르다. 각 사람들은 꿀벌로 변했을 경우 1의 꿀을 생산하는 데 <span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub></span>초의 시간이 걸린다.

예를 들어, 프니가 아래 6명의 사람들 중에서 2명의 사람들을 변신시킨다고 하자.

<div class="row">
<div style="min-width: 360px;" class="col-mg-6 col-sm-6 col-lg-6">
<div class="table-responsive">
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 60px;">사람</th>
   <th style="width: 60px;">은광</th>
   <th style="width: 60px;">민혁</th>
   <th style="width: 60px;">창섭</th>
   <th style="width: 60px;">현식</th>
   <th style="width: 60px;">일훈</th>
   <th style="width: 60px;">성재</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th>꿀</th>
   <td>7</td>
   <td>2</td>
   <td>8</td>
   <td>5</td>
   <td>4</td>
   <td>9</td>
  </tr>
  <tr>
   <th>생산력</th>
   <td>2</td>
   <td>1</td>
   <td>3</td>
   <td>3</td>
   <td>1</td>
   <td>4</td>
  </tr>
 </tbody>
</table>
</div>
</div>
</div>


프니가 창섭과 성재를 꿀벌로 변신시키면 그들이 나머지 사람들이 먹을 꿀을 생산하는 데에는 약 30.857초의 시간이 걸린다. 하지만 프니가 민혁과 일훈을 꿀벌로 변신시키면 14.5초의 시간이 걸리며, 이 방법이 가장 빠른 방법이다.

프니는 가장 빠른 시간 안에 <span class="tex-span"><i>N</i>&thinsp;-&thinsp;2</span>명의 사람들의 꿀을 생산하는 방법을 잘 모른다. 프니를 도와 누구를 꿀벌로 변신시켜야 하는지 구하는 프로그램을 작성하여라.

※ 주의 : 계산 값이 매우 커서 소수를 표현할 때 소수점 아래 자릿수가 적을 수 있으므로 유의하여라.

### 입력 형식

첫 번째 줄에는 사람의 수 <span class="tex-span"><i>N</i></span>이 주어진다.

두 번째 줄에는 각 사람이 먹을 꿀의 양 <span class="tex-span"><i>H</i><sub class="lower-index">1</sub>,&thinsp;<i>H</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>H</i><sub class="lower-index"><i>N</i></sub></span>이 공백을 사이로 두고 차례대로 주어진다.

세 번째 줄에는 각 사람이 꿀벌이 되었을 때 꿀의 생산 속도 <span class="tex-span"><i>T</i><sub class="lower-index">1</sub>,&thinsp;<i>T</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>T</i><sub class="lower-index"><i>N</i></sub></span>이 공백을 사이로 두고 차례대로 주어진다.

### 출력 형식

첫 번째 줄에 프니가 변신시켜야 할 두 사람의 번호 <span class="tex-span"><i>A</i></span>, <span class="tex-span"><i>B</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>A</i>&thinsp;&lt;&thinsp;<i>B</i>&thinsp;&le;&thinsp;<i>N</i></span>)를 출력한다. 답이 여러 개이면 그 중 아무거나 출력한다.

### 부분문제

모든 채점 데이터에 대해,

* <span class="tex-span"><i>N</i>&thinsp;&ge;&thinsp;3</span>
* <span class="tex-span"><i>H</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>T</i><sub class="lower-index"><i>i</i></sub></span>는 정수
* <span class="tex-span">1&thinsp;&le;&thinsp;<i>H</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;100,&thinsp;000</span>

<div class="row">
<div style="min-width: 300px;" class="col-mg-6 col-sm-6 col-lg-6">
<div class="table-responsive">
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
   <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
   <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>N</i></span></th>
   <th class="col-sm-2 col-md-2 col-lg-2">비고</th>
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
   <td class="code-font">22</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;1,&thinsp;000</span></td>
   <td>-</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">28</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;100,&thinsp;000</span></td>
   <td><span class="tex-span"><i>T</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000</span></td>
  </tr>
  <tr>
   <td class="code-font">4</td>
   <td class="code-font">39</td>
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
   <td class="code-font">6<br>
7 2 8 5 4 9<br>
2 1 3 3 1 4</td>
   <td class="code-font">2 5</td>
  </tr>
 </tbody>
</table>
