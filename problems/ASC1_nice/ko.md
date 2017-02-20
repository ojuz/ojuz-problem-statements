요즘 부자들 사이에는 마당을 검정색과 흰색 타일로 패턴이 보이도록 칠하는 것이 유행입니다. 부자인 석환이는 유행에 동참하기로 하여 승현이에게 돈을 주고 색칠을 부탁했습니다. 패턴에서 모두 같은 색으로 칠해진 $2 \times 2$ 크기의 정사각형이 존재하지 않으면, 석환이는 이 패턴을 *좋은 패턴*이라고 부릅니다. 따라서 [그림 1]의 패턴들은 *좋은 패턴*이고, [그림 2]의 패턴들은 좋은 패턴이 아닙니다.

<div style="text-align: center; margin-bottom: 5px; font-size: 12px;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC1_nice/figure1.png"/>
 <p>[그림 1]</p>
</div>
<div style="text-align: center; margin-bottom: 5px; font-size: 12px;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC1_nice/figure2.png"/>
 <p>[그림 2]</p>
</div>

타일을 색칠하던 승현이는 석환이의 뜰에 칠할 수 있는 좋은 패턴의 종류가 몇 가지나 되는지 알고 싶어졌습니다. 석환이의 뜰은 $N \times M$ 크기의 직사각형입니다. 석환이는 매우 부자이기 때문에 $N \le 10^{100}$입니다. 하지만 큰 수를 다루는 것은 언제나 귀찮으므로 답을 $P$로 나눈 나머지를 찾도록 합시다.

### 입력 형식

첫 번째 줄에 세 개의 정수 $N$ ($1 \le N \le 10^{100}$), $M$ ($1 \le M \le 5$), $P$ ($1 \le P \le 10 000$)이 공백을 사이로 두고 주어집니다.

### 출력 형식

$N \times M$ 크기의 뜰에 칠할 수 있는 좋은 패턴의 수를 출력합니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">2 2 5</td>
   <td class="code-font">4</td>
  </tr>
  <tr>
   <td class="code-font">3 3 23</td>
   <td class="code-font">0</td>
  </tr>
 </tbody>
</table>
