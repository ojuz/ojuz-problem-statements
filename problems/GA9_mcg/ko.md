두 자연수의 최대공약수를 구하는 것은 매우 중요합니다. 이 문제에서는 좀더 적은 비용으로 최대공약수를 구하고자 합니다.

석환이와 상수는 **자연수 가공업자**입니다. 이들은 구매자가 두 자연수의 순서쌍 하나를 의뢰하면, 이를 적당히 가공하여 돌려주는 일을 합니다.

<ol type="1"> <li> 석환이는 두 자연수의 순서쌍 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>를 받아, <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_mcg/71dd4c01efb16c5f4aeda0396c384980da7762b9.png"/>로 바꿉니다. 이 작업을 한 번 하는 데 <span class="tex-span"><i>p</i></span>원이 듭니다. </li><li> 상수는 두 자연수의 순서쌍 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>)</span>를 받아, <span class="tex-span"><i>x</i>&thinsp;&ge;&thinsp;<i>y</i></span>라면 <span class="tex-span">(<i>x</i>&thinsp;-&thinsp;<i>y</i>,&thinsp;<i>y</i>)</span>로, <span class="tex-span"><i>x</i>&thinsp;&lt;&thinsp;<i>y</i></span>라면 <span class="tex-span">(<i>x</i>,&thinsp;<i>y</i>&thinsp;-&thinsp;<i>x</i>)</span>로 바꿉니다. 이 작업을 한 번 하는 데 <span class="tex-span"><i>q</i></span>원이 듭니다. </li></ol>

예를 들어, 

* <span class="tex-span">(21, 5)</span>를 석환이에게 맡기면 <span class="tex-span">(5, 1)</span>이 되고, 상수에게 맡기면 <span class="tex-span">(16, 5)</span>가 됩니다. 
* <span class="tex-span">(5, 21)</span>을 석환이에게 맡기면 <span class="tex-span">(21, 5)</span>가 되고, 상수에게 맡기면 <span class="tex-span">(5, 16)</span>이 됩니다.
* <span class="tex-span">(15, 21)</span>을 석환이에게 맡기면 <span class="tex-span">(21, 15)</span>가 되고, 상수에게 맡기면 <span class="tex-span">(15, 6)</span>이 됩니다.

승현이는 두 자연수의 순서쌍 <span class="tex-span">(<i>a</i>,&thinsp;<i>b</i>)</span>를 가지고 있습니다. 수학적 능력이 뛰어난 승현이는, 석환이와 상수에게 자신의 순서쌍을 가공하도록 적당히 의뢰하면, 결국 <span class="tex-span"><i>ab</i>&thinsp;=&thinsp;0</span>을 만족하도록 만들 수 있다는 것을 알게 됩니다. 승현이는 이 때 <span class="tex-span"><i>a</i>&thinsp;+&thinsp;<i>b</i></span>의 값이 원래 두 자연수의 최대공약수라는 것도 알고 있습니다.

이런 식으로 최대공약수를 구하던 승현이는, 문득 <span class="tex-span"><i>a</i>,&thinsp;<i>b</i>,&thinsp;<i>p</i>,&thinsp;<i>q</i></span>의 값이 정해져 있을 때, <span class="tex-span"><i>ab</i>&thinsp;=&thinsp;0</span>을 만족시키기 위해 들여야 할 최소 비용이 얼마일지 궁금해졌습니다. (물론, 승현이는 자연수의 값을 바꿀 수 없습니다.) 의문은 끝없이 생겨, 승현이 스스로 해결할 수 없었고, 결국 승현이는 여러분에게 도움을 요청했습니다.

### 입력 형식

<p>첫 번째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i></span>가 주어집니다.</p><p>다음 <span class="tex-span"><i>T</i></span>개 줄에는 테스트 케이스들이 주어집니다. 이 중 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>T</i></span>)번째 줄에는 네 개의 자연수 <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>b</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>q</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다.</p>

### 출력 형식

<p>각 테스트 케이스에 대해, 승현이가 처음 두 자연수의 순서쌍 <span class="tex-span">(<i>a</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>b</i><sub class="lower-index"><i>i</i></sub>)</span>를 가지고 있고, 석환이에게 한 번 의뢰하는데 <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub></span>원, 상수에게 한 번 의뢰하는 데 <span class="tex-span"><i>q</i><sub class="lower-index"><i>i</i></sub></span>원이 들 때, 가공 의뢰만으로 <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub><i>b</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp;0</span>을 만족시키기 위해 들여야 할 최소 비용을 원 단위로 출력합니다.</p>

### 제약 조건

* <span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;100,&thinsp;000</span>
* 모든 자연수 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>T</i></span>)에 대해, <span class="tex-span">1&thinsp;&le;&thinsp;<i>a</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>b</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>p</i><sub class="lower-index"><i>i</i></sub>,&thinsp; <i>q</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;10<sup class="upper-index">15</sup></span>
* 입력에서 주어지는 모든 수는 자연수입니다.

### 부분문제

<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-1 col-md-1 col-lg-1">부분문제</th>
  <th class="col-sm-2 col-md-2 col-lg-2">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>T</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span">max{<i>a</i><sub class="lower-index"><i>i</i></sub>, <i>b</i><sub class="lower-index"><i>i</i></sub>}       
  <th>추가 제약 조건</th>
</span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>14</td>
  <td><span class="tex-span">&le; 100</span></td>
  <td><span class="tex-span">&le; 100</span></td>
  <td>모든 자연수 <span class="tex-span"><i>i</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>T</i></span>)에 대해, <span class="tex-span"><i>p</i><sub class="lower-index"><i>i</i></sub>, <i>q</i><sub class="lower-index"><i>i</i></sub> &le; 100</span></td>
 </tr>
 <tr>
  <td>2</td>
  <td>16</td>
  <td><span class="tex-span">&le; 100,000</span></td>
  <td><span class="tex-span">&le; 2,000</span></td>
  <td><span class="tex-span"><i>p</i><sub class="lower-index">1</sub>&thinsp;=&thinsp;<i>p</i><sub class="lower-index">2</sub>&thinsp;=&thinsp;...&thinsp;=&thinsp;<i>p</i><sub class="lower-index"><i>T</i></sub> &le; 2,000,&thinsp;<i>q</i><sub class="lower-index">1</sub>&thinsp;=&thinsp;<i>q</i><sub class="lower-index">2</sub>&thinsp;=&thinsp;...&thinsp;=&thinsp;<i>q</i><sub class="lower-index"><i>T</i></sub> &le; 2,000</span></td>
 </tr>
 <tr>
  <td>3</td>
  <td>27</td>
  <td><span class="tex-span">&le; 1,000</span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
  <td>-</td>
 </tr>
 <tr>
  <td>4</td>
  <td>43</td>
  <td><span class="tex-span">&le; 100,000</span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">15</sup></span></td>
  <td>-</td>
 </tr>
</tbody>
</table>
</div>

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>4<br>7 3 1 1<br>8 3 1 1<br>7 3 3 2<br>55 34 10 9</samp></td><td><samp>2<br>3<br>6<br>74</samp></td></tr></tbody>
</table>

### 설명

첫 번째, 두 번째, 세 번째 입력 모두에서 석환이에게만 맡기는 것이 최선입니다.

네 번째 입력에서는 상수와 석환이 모두에게 맡겨야 합니다. 변화를 살펴보자면 아래와 같습니다. 오른쪽으로 향하는 화살표는 상수의 가공을, 아래로 향하는 화살표는 석환이의 가공을 의미합니다.

<center>
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA9_mcg/ex4.png" class="thumbnail"/>
</center>