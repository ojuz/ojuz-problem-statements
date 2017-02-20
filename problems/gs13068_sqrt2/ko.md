승현이는 어릴 때부터 수학을 매우 잘했다고 합니다.

어느 날, 중학생인 승현이는 수학 공부를 하다가 매우 작은 $X$에 대해서 다음이 성립한다는 것을 깨우쳤습니다.

$ 1 + X \approx 1 + X + \frac{1}{4}X^2 = ( 1 + \frac{1}{2}X )^2 $

승현이는 똑똑해서, 이를 확장하여 제곱근을 근사할 수 있는 방법을 고안했다고 합니다. 그러나 오랜 시간이 지난 지금의 승현이는 그때의 방법이 기억나지 않습니다. 다행히도, 그 때 노트에 적어 놓은 $N$과 제곱근 $N$의 순서쌍들은 남아 있습니다. 승현이의 근사법을 찾아주세요.


### 입력 형식

첫 번째 줄에 자연수 $N$이 주어집니다. ( $ 1 \le N \le 10^{10} $ )

### 출력 형식

첫 번째 줄에 제곱근 $N$을 소수점 6번째 자리까지 출력한다.

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
   <td class="code-font">1</td>
   <td class="code-font">1.000000</td>
  </tr>
  <tr>
   <td class="code-font">2</td>
   <td class="code-font">1.500000</td>
  </tr>
  <tr>
   <td class="code-font">3</td>
   <td class="code-font">1.750000</td>
  </tr>
  <tr>
   <td class="code-font">5</td>
   <td class="code-font">2.250000</td>
  </tr>
  <tr>
   <td class="code-font">8</td>
   <td class="code-font">2.833333</td>
  </tr>
 </tbody>
</table>