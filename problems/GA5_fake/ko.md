승현이는 남을 속이는 것을 참 좋아합니다. 오늘 승현이는 수열을 가지고 우리를 속여 보려고 합니다.

승현이는 길이가 $n$인 자연수로 구성된 수열 $a_{1}, a_{2}, \cdots, a_{n}$을 들고 왔습니다. 그러더니 갑자기 이 수열의 각 원소를 두 그룹 $X$나 $Y$ 중 하나에 넣으라고 합니다. 편의상 $X$의 모든 원소를 $X_{1}, X_{2}, \cdots, X_{k}$, $Y$의 모든 원소를 $Y_{1}, Y_{2}, \cdots, Y_{n-k}$로 둡시다. (단 $k > 0, n-k > 0$)

승현이는 $X_{1} \oplus X_{2} \oplus \cdots \oplus X_{k}$의 값과 $Y_{1} \oplus Y_{2} \oplus \cdots \oplus Y_{n-k}$의 값이 같으면 우리에게 $X_{1} + X_{2} + \cdots + X_{k}$원을 준다고 합니다.

승현이에게 너무 많이 속은 여러분은 믿기지 않지만, 돈을 잃을 일은 없으니 한 번 시도해 보기로 했습니다. 승현이가 제시한 수열 $a$가 주어질 때, 여러분이 돈을 받을 수 있는지, 돈을 받을 수 있다면 최대 얼마나 받을 수 있는지 구하는 프로그램을 작성하세요.

참고: $\oplus$는 배타적 논리합(XOR)를 뜻합니다. 자세한 설명은 [여기](http://ko.wikipedia.org/wiki/%EB%B0%B0%ED%83%80%EC%A0%81_%EB%85%BC%EB%A6%AC%ED%95%A9#.EB.B9.84.ED.8A.B8.EA.B0.84_.EB.B0.B0.ED.83.80.EC.A0.81_.EB.85.BC.EB.A6.AC.ED.95.A9)와 [여기](http://ko.wikipedia.org/wiki/XOR_%EC%8A%A4%EC%99%91_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98#.EC.A6.9D.EB.AA.85)를 참고하세요.

### 입력 형식

첫 번째 줄에 $n$이 주어지고, 두 번째 줄에 $a_{1}, a_{2}, \cdots, a_{n}$ ($1 \le a_{1}, a_{2}, \cdots, a_{n} \le 10^6)$이 공백을 사이로 두고 주어집니다.

### 출력 형식

첫 번째 줄에 여러분이 받을 수 있는 돈의 최댓값을 출력합니다. 만약 돈을 받을 수 없다면 0을 출력합니다.

### 서브태스크

#### 서브태스크 1 (10점)

* $1 \le n \le 15$.

#### 서브태스크 2 (20점)

* $1 \le n \le 50$.

#### 서브태스크 3 (30점)

* $1 \le n \le 100$.

#### 서브태스크 4 (40점)

* $1 \le n \le 1,000$.

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
   <td class="code-font">3<br/>
1 2 3</td>
   <td class="code-font">5</td>
  </tr>
  <tr>
   <td class="code-font">4<br/>
1 2 3 4</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>