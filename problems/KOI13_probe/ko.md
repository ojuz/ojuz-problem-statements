직선 모양의 도로에 특별한 물체가 묻혀있다. 우리는 직선구간을 탐색할 수 있는 장비를 이용해서 이 물체가 어디에 있는지를 조사하고자 한다. 직선도로를 일차원 배열로 생각해보자. 아래 그림에서 숫자는 단위 구간의 번호이며 그 안에 ▲ 기호로 표시된 것은 우리가 찾아낼 물체이다.


<div style="width: 100%; text-align: center; margin-bottom: 10px;">
<table class="table table-condensed" style="margin: 0 auto; width: 240px;">
	<thead>
	<tr>
    	<th style="width: 20px; text-align: center">1</th>
    	<th style="width: 20px; text-align: center">2</th>
    	<th style="width: 20px; text-align: center">3</th>
    	<th style="width: 20px; text-align: center">4</th>
    	<th style="width: 20px; text-align: center">5</th>
    	<th style="width: 20px; text-align: center">6</th>
    	<th style="width: 20px; text-align: center">7</th>
    	<th style="width: 20px; text-align: center">8</th>
    	<th style="width: 20px; text-align: center">9</th>
    	<th style="width: 20px; text-align: center">10</th>
    	<th style="width: 20px; text-align: center">11</th>
    	<th style="width: 20px; text-align: center">12</th>
    </tr>
    </thead>
    <tbody>
	<tr>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;">▲</td>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;">▲</td>
    	<td style="text-align: center;">▲</td>
    	<td style="text-align: center;">▲</td>
    	<td style="text-align: center;">▲</td>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;"></td>
    	<td style="text-align: center;">▲</td>
    </tr>
    </tbody>
</table>
</div>

그런데 우리는 어떤 연속된 구간에 포함되어 있는 물체의 개수를 $Probe[x,y]$를 이용하여 확인할 수 있다. $x$부터 $y$까지의 구간에 물체가 $r$개가 있음은 $Probe[x,y]=r$ 로 표현된다. (단 $x \le y$ 이다.) 예를 들어 그림 1과 같은 상황이라면 $Probe[2,7]=3$, $Probe[2,2]=0$, $Probe[6,9]=4$, $Probe[5,12]=5$임을 알 수 있다.

여러분은 제시된 탐사작업의 결과가 모두 만족되는 구간을 재구성하는 프로그램을 작성해야 한다. 수행시간은 2초이며 부분점수는 없다.

### 입력 형식

첫 줄에는 두 개의 정수 $K$와 $N$이 주어져 있다. $K$는 전체 구간의 길이이며, N은 조사한 $Probe[x,y]=r$ 결과의 개수이다. 이어 나타나는 $N$개의 각 줄에는 하나의 탐사결과 $Probe[x,y]=r$ 를 나타내는 세 개의 숫자 $x$, $y$, $r$이 공백문자로 분리되어 제시되어 있다. 단 입력변수에 대한 제한 범위는 다음과 같다. $3 \le K \le 40, 2 \le N \le 1000, 1 \le x \le y \le K$.

### 출력 형식

여러분은 $N$개의 탐사결과를 만족하는 전체 구간을 길이 $K$인 문자열로 표시해야 한다. 물체가 있는 단위 구간은 문자 `'#'`으로 표시해야 하고, 없는 단위 구간은 마이너스 기호 `'-'`로 표시해야 한다. 답이 여러 개 존재할 때에는 그 중 하나만 출력하면 된
다. 만일 탐사결과를 모두 만족하는 답이 존재하지 않을 경우에는 문자열 "`NONE`"을 출력해야 한다.

### 입력과 출력의 예

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr class="code-font">
   <td style="width: 50%;">12 7<br/>
1 8 4<br/>
6 10 4<br/>
2 12 6<br/>
9 12 2<br/>
4 6 1<br/>
1 4 1<br/>
11 11 0</td>
   <td>--#--####--#</td>
  </tr>
  <tr class="code-font">
   <td style="width: 50%;">12 2<br/>
1 10 1<br/>
4 7 3</td>
   <td>NONE</td>
  </tr>
 </tbody>
</table>