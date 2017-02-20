아래 그림과 같이 직선 도로상에 왼쪽부터 오른쪽으로 1번부터 차례대로 번호가 붙여진 마을들이 있다. 마을에 있는 물건을 배송하기 위한 트럭 한 대가 있고, 트럭이 있는 본부는 1번 마을 왼쪽에 있다. 이 트럭은 본부에서 출발하여 1번 마을부터 마지막 마을까지 오른쪽으로 가면서 마을에 있는 물건을 배송한다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/KOI13_delivery/pic1.png?dl=1" style="width: 350px;"/>
</div>

각 마을은 배송할 물건들을 박스에 넣어 보내며, 본부에서는 박스를 보내는 마을번호, 박스를 받는 마을 번호와 보낼 박스의 개수를 알고 있다. 박스들은 모두 크기가 같다. 트럭에 최대로 실을 수 있는 박스의 개수, 즉 트럭의 용량이 있다. 이 트럭 한 대를 이용하여 다음의 조건을 모두 만족하면 서 최대한 많은 박스들을 배송하려고 한다.

* **조건 1: 박스를 트럭에 실으면, 이 박스는 받는 마을에서만 내린다.**
* **조건 2: 트럭은 지나온 마을로 되돌아가지 않는다.**
* **조건 3: 박스들 중 일부만 배송할 수도 있다.**

마을의 개수, 트럭의 용량, 박스 정보(보내는 마을 번호, 받는 마을번호, 박스 개수)가 주어질 때, 트럭 한 대로 배송할 수 있는 최대 박스 수를 구하는 프로그램을 작성하시오. 단, 받는 마을 번호는 보내는 마을번호보다 항상 크다.

예를 들어, 트럭 용량이 40이고 보내는 박스들이 다음 표와 같다고 하자.

<div style="width: inherit; margin-bottom: 10px;">
<table class="table table-bordered table-striped" style="width: 300px; margin: 0 auto;">
	<thead>
		<tr>
			<th style="width: 100px;">보내는 마을</th>
			<th style="width: 100px;">받는 마을</th>
			<th>박스 개수</th>
		</tr>
	</thead>
	<tbody>
		<tr><td>1</td><td>2</td><td>10</td></tr>
		<tr><td>1</td><td>3</td><td>20</td></tr>
		<tr><td>1</td><td>4</td><td>30</td></tr>
		<tr><td>2</td><td>3</td><td>10</td></tr>
		<tr><td>2</td><td>4</td><td>20</td></tr>
		<tr><td>3</td><td>4</td><td>20</td></tr>
	</tbody>
</table>
</div>

이들 박스에 대하여 다음과 같이 배송하는 방법을 고려해 보자.

(1) 1번 마을에 도착하면

* 다음과 같이 박스들을 트럭에 싣는다. (1번 마을에서 4번 마을로 보내는 박스는 30개 중 10개를 싣는다.)

<div style="width: inherit; margin-bottom: 10px;">
<table class = "table table-bordered table-striped" style="width: 300px; margin: 0 auto;">
<thead>
<tr>
<th style="width: 100px;">보내는 마을</th>
<th style="width: 100px;">받는 마을</th>
<th>박스 개수</th>
</tr>
</thead>
<tbody>
<tr><td>1</td><td>2</td><td>10</td></tr>
<tr><td>1</td><td>3</td><td>20</td></tr>
<tr><td>1</td><td>4</td><td>10</td></tr>
</tbody>
</table>
</div>

(2) 2번 마을에 도착하면

* 트럭에 실려진 박스들 중 받는 마을번호가 2인 박스 10개를 내려 배송한다. (이때 트럭에 남아있는 박스는 30개가 된다.)
* 그리고 다음과 같이 박스들을 싣는다. (이때 트럭에 실려 있는 박스는 40개가 된다.)

<div style="width: inherit; margin-bottom: 10px;">
<table class = "table table-bordered table-striped" style="width: 300px; margin: 0 auto;">
<thead>
<tr>
<th style="width: 100px;">보내는 마을</th>
<th style="width: 100px;">받는 마을</th>
<th>박스 개수</th>
</tr>
</thead>
<tbody>
<tr><td>2</td><td>3</td><td>10</td></tr>
</tbody>
</table>
</div>

(3) 3번 마을에 도착하면 

* 트럭에 실려진 박스들 중 받는 마을번호가 3인 박스 30개를 내려 배송한다. (이때 트럭에 남아있는 박스는 10개가 된다.)
* 그리고 다음과 같이 박스들을 싣는다. (이때 트럭에 실려 있는 박스는 30개가 된다.)

<div style="width: inherit;">
<table class = "table table-bordered table-striped" style="width: 300px; margin: 0 auto;">
<thead>
<tr>
<th style="width: 100px;">보내는 마을</th>
<th style="width: 100px;">받는 마을</th>
<th>박스 개수</th>
</tr>
</thead>
<tbody>
<tr><td>3</td><td>4</td><td>20</td></tr>
</tbody>
</table>
</div>

(4) 4번 마을에 도착하면 

* 받는 마을번호가 4인 박스 30개를 내려 배송한다

위와 같이 배송하면 배송한 전체 박스는 70개이다. 이는 배송할 수 있는 최대 박스 개수이다.

수행시간은 1초를 넘을 수 없다. 메모리 제한은 128MB이다.

### 입력 형식

입력의 첫 줄은 마을 수 $N$과 트럭의 용량 $C$가 빈칸을 사이에 두고 주어진다. $N$은 2이상 2,000이하 정수이고, $C$는 1이상 10,000이하 정수이다. 다음 줄에, 보내는 박스 정보의 개수 $M$이 주어진다. $M$은 1이상 10,000이하 정수이다. 다음 $M$개의 각 줄에 박스를 보내는 마을번호, 박스를 받는 마을번호, 보내는 박스 개수(1이상 10,000이하 정수)를 나타내는 양의 정수가 빈칸을 사이에 두고 주어진다. 박스를 받는 마을번호는 보내는 마을번호보다 크다. 

### 출력 형식

트럭 한 대로 배송할 수 있는 최대 박스 수를 한 줄에 출력한다.

### 부분문제의 제약 조건

* **부분문제 1**: 전체 점수 100점 중 15점에 해당하는 데이터에 대해, 보내는 마을번호는 모두 1이고 $N \le 20$이다.
* **부분문제 2**: 전체 점수 100점 중 17점에 해당하는 데이터에 대해, 받는 마을 번호는 $N-1$ 또는 $N$이고 $3 \le N \le 20$이다.
* **부분문제 3**: 전체 점수 100점 중 20점에 해당하는 데이터에 대해 $N \le 5, M \le 5, C \le 10$이다.
* **부분문제 4**: 전체 점수 100점 중 23점에 해당하는 데이터에 대해 $N \le 100, M \le 1,000, C \le 2,000$이다.
* **부분문제 5**: 전체 점수 100점 중 25점에 해당하는 데이터에 대해 추가적인 제약조건은 없다.

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
   <td style="width: 50%;">
4 40<br/>
6<br/>
3 4 20<br/>
1 2 10<br/>
1 3 20<br/>
1 4 30<br/>
2 3 10<br/>
2 4 20<br/></td>
   <td>70</td>
  </tr>
  <tr class="code-font">
   <td style="width: 50%;">
6 60<br/>
5<br/>
1 2 30<br/>
2 5 70<br/>
5 6 60<br/>
3 4 40<br/>
1 6 40</td>
   <td>150</td>
  </tr>
 </tbody>
</table>