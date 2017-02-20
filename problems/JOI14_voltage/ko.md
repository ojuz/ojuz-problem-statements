여러분은 Just Odd Inventions라는 회사를 알고 있나요? 이 회사의 업무는 "그냥 이상한 발명 (just odd inventions)"을 하는 것입니다. 앞으로 편의상 JOI 사라고 부르겠습니다.

JOI 사의 한 실험실에는 복잡한 전기 회로가 있습니다. 이 회로는 $N$개의 접점과 $M$개의 길쭉한 전기 저항으로 구성됩니다. 접점들에는 $1$ 이상 $N$ 이하의 자연수 번호가 붙어 있습니다. 각 접점은 "고전압"과 "저전압" 중 하나의 상태로 설정될 수 있습니다. 각 전기 저항은 두 개의 접점을 이으며, 이 접점들 중 하나가 "고전압" 상태이고 다른 하나가 "저전압" 상태에 있을 때 전류가 흐릅니다. "고전압" 절점끼리 또는 "저전압" 절점끼리 연결되어 있는 저항에는 전류가 흐르지 않습니다.

어느 날 JOI 사는 회로의 유지 보수를 위해 하나의 전기 저항을 선택하여 그 저항에만 전류가 흐르지 않도록, 그리고 나머지 $M-1$개의 저항에는 전류가 흐르도록 각 접점의 전압을 설정하기로 했습니다. 이를 위해 어떤 저항들을 선택할 수 있을까요?

또한 JOI 사가 이 이상한 회로를 사용하여 어떤 발명을 하는지는 사내에서도 극비인지라 사장 말고는 아무도 모른다고 합니다.

### 해야 할 일

회로의 정보가 주어질 때, 유지 보수를 할 때 전류를 흘려 보내지 않을 전기 저항으로 선택할 수 있는 전기 저항의 수를 출력하는 프로그램을 작성하세요.

### 입력 형식

표준 입력에서 아래 입력을 받습니다.

* 첫 번째 줄에 두 개의 정수 $N$과 $M$이 공백을 사이로 두고 주어집니다. $N$은 접점의 수이고, $M$은 전기 저항의 수입니다.
* 다음에 $M$개 줄이 주어집니다. 이 중 $i$($1 \le i \le M$)번째 줄에는 두 개의 정수 $A_{i}$와 $B_{i}$ ($1 \le A_{i} \le N$, $1 \le B_{i} \le N$)가 공백을 사이로 두고 주어집니다. 이것은 $i$번째 전기 저항이 $A_{i}$번 접점과 $B_{i}$번 접점을 연결하고 있다는 것을 의미합니다.

### 출력 형식

첫 번째 줄에 유지 보수를 할 때 전류를 흘려 보내지 않을 전기 저항으로 선택할 수 있는 전기 저항의 수를 출력하세요.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* $2 \le N \le 100,000$
* $1 \le M \le 200,000$

### 서브태스크 

#### 서브태스크 1 [10점]

* $N \le 1,000$
* $M \le 2,000$

#### 서브태스크 2 [10점]

* 한 접점에서 다른 모든 접점으로 한 개 이상의 전기 회로를 따라 이동할 수 있습니다.
* $M = N$

#### 서브태스크 3 [35점]

* 한 접점에서 다른 모든 접점으로 한 개 이상의 전기 회로를 따라 이동할 수 있습니다.
* $M \le N + 100$

#### 서브태스크 4 [45점]

추가 제약 조건이 없습니다.

### 입출력 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 1</th>
   <th>출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4 5<br>
1 2<br>
1 3<br>
1 4<br>
2 4<br>
3 4</td>
   <td class="code-font">1</td>
  </tr>
 </tbody>
</table>

이 예제에서는 세 번째 전기 저항에만 전류가 흐르지 않게 할 수 있습니다. 예를 들어, 1번 접점과 4번 접점을 "고전압"으로, 2번 접점과 3번 접점을 "저전압"으로 설정하면 됩니다. 세 번째 전기 저항은 1번 접점과 4번 접점을 연결하고 있기 때문에, 전류가 흐르지 않습니다.

세 번째 전기 저항을 제외하고는 전류를 흘리지 않을 전기 저항을 선택할 수 없습니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI14_voltage/ex1.png"/>
</div>

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 2</th>
   <th>출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4 4<br>
1 2<br>
2 3<br>
3 2<br>
4 3</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>

이 예제에서는 첫 번째 전기 저항 또는 네 번째 전기 저항을 유지 보수할 때 전류를 흘리지 않을 전기 저항으로 선택할 수 있습니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/JOI14_voltage/ex2.png"/>
</div>

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력 3</th>
   <th>출력 3</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">13 16<br>
1 6<br>
2 6<br>
3 1<br>
3 2<br>
4 7<br>
4 7<br>
5 9<br>
6 5<br>
8 2<br>
8 13<br>
9 11<br>
10 3<br>
11 10<br>
11 12<br>
12 8<br>
13 6</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>