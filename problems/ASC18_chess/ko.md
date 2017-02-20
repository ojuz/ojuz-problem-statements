자연수 $n$을 더 작은 자연수들의 합으로 표현해 봅시다: $n = m_{1} + m_{2} + \cdots + m_{k} (단 $m_{1} \ge m_{2} \ge \cdots \ge m_{k}$ 이 분할은 *Young diagram*으로 표현할 수 있습니다. - $n$개의 정사각형이 $k$개의 줄에 걸쳐 나열되어 있습니다. (여기서 $k$는 분할된 수들의 개수입니다.) $m_{i}$를 나타내는 행에는 $m_{i}$개의 정사각형이 나열됩니다. 모든 정사각형은 왼쪽에 붙어있으며, 위에서부터 아래로 내림차순 정렬되어 있습니다. 정의가 헷갈리시다면 아래 그림을 참고하세요.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC18_chess/diag1.png"/>
</div>

Young diagram의 각 정사각형 안에 $1$ 이상 $n$ 이하의 자연수 번호를 넣으면 *Young tableau*가 됩니다. 이 때 적혀 있는 숫자는 왼쪽에서 오른쪽으로 갈 수록 증가하고, 위에서 아래로 갈 수록 증가해야 합니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC18_chess/diag2.png"/>
</div>

Young tableau의 정사각형들을 체스판과 같이 색칠했을 때, 검은색으로 칠해진 칸들에 홀수 번호가, 흰색으로 칠해진 칸들에 짝수 번호가 쓰여 있다면 *chess tableau*라고 합니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC18_chess/diag3.png"/>
</div>

당연하지만 모든 Young diagram을 chess tableau로 바꿀 수 있는 것은 아닙니다.  예로 들어, 아래의 두 그림은 chess tableau가 될 수 없습니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/ASC18_chess/diag4.png"/>
</div>

$n$이 주어질 때, $n$을 적절히 분할하여 만들어진 Young diagram을 chess tableau로 바꿀 수 있는 경우의 수를 찾는 프로그램을 작성하세요.

### 입력 형식

$n$이 주어집니다. ($1 \le n \le 50$)

### 출력 형식

chess tableau가 만들어지도록 $n$을 분할할 수 있는 경우의 수를 출력합니다.

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
   <td class="code-font">10</td>
   <td class="code-font">36</td>
  </tr>
 </tbody>
</table>