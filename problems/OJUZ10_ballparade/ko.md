5월 5일 ‘방긋 스마일스’와의 어린이날 프로야구 경기에서 ‘GA 아인타즈’의 감독 성균이는 테스트 겸으로 창석이를 선발 투수로 등판시켰다. 그러나 창석이는 스트라이크를 못 던지는 치명적인 단점이 있다. 그는 경기 때 '볼', '몸에 맞는 공', '폭투' 이렇게 3가지 종류의 공을 던진다. 창석이가 너무나도 터무니없는 공을 던지기 때문에 타자가 배트를 휘두를 일은 없다.

<center>
<img class="thumbnail" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/OJUZ10_ballparade/depiction.jpg">
</center>

한 타자를 상대로 '볼'을 4번 던지거나 '몸에 맞는 공'을 던질 경우, 타자는 1루로 간다. 기존 주자는 아래 조건에 의하여 이동한다.

- 1루 주자는 무조건 2루로 간다.
- 2루 주자는 1루에 주자가 있는 경우에만 한해서 3루로 간다.
- 3루 주자는 1, 2루에 주자가 있는 경우에만 한해서 홈으로 간다. 이 때 3루 주자는 1득점을 한다.

한편, '폭투'를 던지면 주자는 아래 조건에 의하여 이동한다.

- 1, 2루에 있던 주자는 각각 2, 3루로 간다.
- 3루 주자는 홈으로 들어오면서 1득점을 한다.

'폭투'도 '볼'의 한 종류이므로, '볼'-'폭투'-'볼'-'볼'도 4개의 '볼'로 인정이 되며, 4번째 '볼'이 폭투라면 타자도 1루로 간다.

창석이는 1회 초에 <span class="tex-span"><i>N</i></span>개의 공을 던지고 다른 투수로 교체되었다. 창석이가 던진 공의 종류가 주어질 때 창석이의 총 실점을 구하는 프로그램을 작성하여라. 단, 한 타자를 상대하는 도중에 창석이가 다른 투수로 교체될 수도 있음에 유의하여라.

### 입력 형식

첫 번째 줄에는 창석이가 강판당할 때까지 던진 공의 수 <span class="tex-span"><i>N</i></span>이 주어진다.

두 번째 줄에는 창석이가 던진 공의 종류가 주어진다. '볼', '몸에 맞는 공', '폭투'는 각각 1, 2, 3으로 주어진다.

### 출력 형식

창석이의 총 실점을 출력한다.

### 부분문제

모든 채점 데이터에 대해,

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;50,&thinsp;000</span>

<div class="row">
<div style="min-width: 300px;" class="col-mg-7 col-sm-7 col-lg-7">
<div class="table-responsive">
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
   <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
   <th class="col-sm-4 col-md-4 col-lg-4">비고</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">1</td>
   <td class="code-font">22</td>
   <td>창석이가 폭투를 던지지 않는다.</td>
  </tr>
  <tr>
   <td class="code-font">2</td>
   <td class="code-font">25</td>
   <td>창석이가 몸에 맞는 공을 던지지 않는다.</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">53</td>
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
   <td class="code-font">16<br>
1 1 2 1 3 3 1 2 1 1 3 1 1 1 3 3</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>

### 예제 설명

1번 타자 : 볼-볼-몸에 맞는 공 (주자 1루)

2번 타자 : 볼-폭투(주자 2루)-폭투(주자 3루)-볼 (주자 1, 3루)

3번 타자 : 몸에 맞는 공 (주자 1, 2, 3루)

4번 타자 : 볼-볼-폭투(1실점, 주자 2, 3루)-볼 (주자 1, 2, 3루)

5번 타자 : 볼-볼-폭투(1실점, 주자 2, 3루)-폭투(1실점, 주자 1, 3루)