<style type="text/css">
.tex-span {
    font-size: 125%;
    font-family: times new roman;
}
.tex-formula {
    vertical-align: middle;
    margin: 0;
    border:medium none;
    position: relative;
    bottom: 2px;
}
</style>


Bob는 유명한 건축업자입니다. 그는 땅을 샀고 집을 짓고 싶습니다. 불운하게도, 문제는 그 섬의 지형으로, 고도의 변동이 심합니다.

그 땅은 좌우로 <span class="tex-span"><i>N</i></span>미터, 위아래로 <span class="tex-span"><i>M</i></span>미터 길이의 직사각형처럼 생겼습니다. 그 땅은 <span class="tex-span"><i>N</i> &times; <i>M</i></span>개의 정사각형들로 분할될 수 있습니다. (그림을 보세요) Bob의 집은, 변이 땅의 가장자리와 **평행**하고, 꼭짓점들이 정사각형들의 꼭짓점들과 **일치하는** 직사각형 모양일 것입니다. 승현이의 집이 지어지는 부분은, 붕괴를 방지하기 위해 **높이가 모두 같아야 합니다.**

<div style="text-align: center;">
<div><img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/COCI14_bob/land.PNG"></div>
<small><i>정사각형들로 분할된 땅. 집을 지을 수 있는 두 가지 방법이 빨강색과 파랑색으로 색칠되어 있습니다.</i></small>
</div>

### 입력 형식

첫 번째 줄에 두 개의 정수 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>M</i></span> (<span class="tex-span">1 &le; <i>N</i>, <i>M</i> &le; 1 000</span>)이 주어집니다. 

다음 <span class="tex-span"><i>N</i></span>개의 줄에는 각각 <span class="tex-span"><i>M</i></span>개의 정수들 <span class="tex-span"><i>a<sub>i,j</sub></i></span> ( <span class="tex-span">1 &le; <i>a<sub>i,j</sub></i> &le; 10<sup>9</sup></span>)이 공백을 사이로 두고 주어집니다. 이 정수들은 땅의 각 정사각형의 해발 고도를 나타냅니다.

**주의** 입력량이 매우 크므로 빠른 입출력 방식을 사용하세요

### 출력 형식

첫 번째 줄에 문제에서 요구하는 답을 출력합니다.

### 채점 방식

20%의 점수에 해당하는 테스트 케이스들은 <span class="tex-span"><i>N, M</i> &le; 50</span>을 만족합니다.

60%의 점수에 해당하는 테스트 케이스들은 <span class="tex-span"><i>N, M</i> &le; 500</span>을 만족합니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">5 3<br>
2 2 2<br>
2 2 1<br>
1 1 1<br>
2 1 2<br>
1 2 1</td>
   <td class="code-font">27</td>
  </tr>
  <tr>
   <td class="code-font">4 3<br>
1 1 1<br>
1 1 1<br>
2 2 2<br>
2 2 2</td>
   <td class="code-font">36</td>
  </tr>
 </tbody>
</table>

**첫 번째 예제의 설명**: 집을 지을 수 있는 가능한 방법들에는 (0, 0)-(1, 1), (0, 0)-(0, 2), (2, 0)-(2, 2), (1, 2)-(2, 2) 등이 있습니다. 괄호 내의 첫 번째 수는 열 번호를, 두 번째 수는 행 번호를 나타내며, 번호는 0에서부터 시작하여 차례대로 붙습니다. (a, b)-(c, d)는 왼쪽 위 꼭짓점이 (a, b)이고 오른쪽 아래 꼭짓점이 (c, d)인 직사각형을 나타냅니다.