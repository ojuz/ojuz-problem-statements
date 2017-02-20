승현이는 아래와 같은 수열을 만들고 좋아서 히죽거리고 있다.

* <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;<i>S</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>N</i></span>) 
* <span class="tex-span"><i>B</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;<i>B</i><sub class="lower-index">1</sub>,&thinsp;<i>B</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>B</i><sub class="lower-index"><i>i</i>&thinsp;-&thinsp;1</sub></span> 에 있는 서로 다른 수의 개수 (<span class="tex-span"><i>N</i>&thinsp;&lt;&thinsp;<i>i</i></span>)

여기서 <span class="tex-span"><i>S</i></span>는 승현이가 혼자서 생각한 길이 <span class="tex-span"><i>N</i></span>인 수열이다. 

승현이는 수열 <span class="tex-span"><i>B</i></span>의 <span class="tex-span"><i>M</i></span>번째 항을 계산하고 싶어 한다. 하지만 이런 일은 승현이에게는 너무 쉽기 때문에 승현이는 귀찮아한다. 승현이 대신 수열의 <span class="tex-span"><i>M</i></span>번째 항을 구하는 프로그램을 작성하여라.

### 입력 형식

첫 번째 줄에는 수열 <span class="tex-span"><i>S</i></span>의 길이 <span class="tex-span"><i>N</i></span>이 주어진다.

두 번째 줄에는 <span class="tex-span"><i>S</i><sub class="lower-index">1</sub>,&thinsp;<i>S</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>S</i><sub class="lower-index"><i>N</i></sub></span>이 공백을 사이로 두고 차례대로 주어진다.

세 번째 줄에는 <span class="tex-span"><i>M</i></span>이 주어진다.

### 출력 형식

수열 <span class="tex-span"><i>B</i></span>의 <span class="tex-span"><i>M</i></span>번째 항의 값을 출력한다.

### 부분문제

모든 채점 데이터에 대해,

* <span class="tex-span"><i>N</i>&thinsp;&ge;&thinsp;1</span>
* <span class="tex-span"><i>M</i></span>은 자연수
* 수열 <span class="tex-span"><i>S</i></span>의 각 원소는 정수
* <span class="tex-span">&thinsp;-&thinsp;1,&thinsp;000,&thinsp;000&thinsp;&le;&thinsp;<i>S</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;1,&thinsp;000,&thinsp;000</span>

<div class="row">
<div style="min-width: 300px;" class="col-mg-6 col-sm-7 col-lg-6">
<div class="table-responsive">
<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
   <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
   <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>N</i></span></th>
   <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>M</i></span></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">1</td>
   <td class="code-font">8</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;500</span></td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;<i>N</i></span></td>
  </tr>
  <tr>
   <td class="code-font">2</td>
   <td class="code-font">24</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;500</span></td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;10<sup>3</sup></span></td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">30</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;50,&thinsp;000</span></td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;10<sup>5</sup></span></td>
  </tr>
  <tr>
   <td class="code-font">4</td>
   <td class="code-font">38</td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;50,&thinsp;000</span></td>
   <td><span class="tex-span">&thinsp;&le;&thinsp;10<sup>9</sup></span></td>
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
   <td class="code-font">4<br>
2 13 -7 2<br>
9</td>
   <td class="code-font">7</td>
  </tr>
 </tbody>
</table>

### 예제 설명

주어진 수열을 9번째 수까지 나타내면 아래와 같다.

2, 13, -7, 2, 3, 4, 5, 6, 7