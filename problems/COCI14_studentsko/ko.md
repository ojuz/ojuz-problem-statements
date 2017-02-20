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


Zagreb 대학 학생들의 연례 팀 탁구 대회가 다음 주 토요일에 열립니다! 각 팀은 <span class="tex-span"><i>K</i></span>명의 학생들로 구성되어 있습니다. <span class="tex-span"><i>N</i></span>명의 신이 난 학생들은, 등록을 위해 대기하고 있습니다.

상수는 접수 창구에서 일하고 있습니다. 그는 그의 직업이 마음에 들지 않아서 학생들이 팀을 고르는 것을 허용하지 않기로 했습니다. 그는 첫 번째 팀은 줄에 서 있는 처음 <span class="tex-span"><i>K</i></span>명의 학생들로, 두 번째 팀은 그 다음으로 서 있는 <span class="tex-span"><i>K</i></span>명의 학생들로, ... 구성하기로 했습니다. (<span class="tex-span"><i>N</i></span>은 <span class="tex-span"><i>K</i></span>로 나누어 떨어지기 때문에, 줄에 서지 않은 학생은 없습니다.)

승현이는 각 선수의 기술을 정수 값으로 추정했습니다. 이 값이 적을수록 학생의 능력이 더 좋습니다. 그는 첫 번째 팀에는 가장 강한 <span class="tex-span"><i>K</i></span>명의 학생들이, 두 번째 팀에는 그 다음으로 가장 강한 <span class="tex-span"><i>K</i></span>명의 학생들이, ... 속하도록 하고자 합니다.

상수는 막 휴식을 취했고, 승현이는 줄을 서 있는 학생들을 움직여 그의 목표를 달성하고자 합니다. 승현이는 어떤 학생을 줄에서의 다른 위치 (맨 앞과 맨 뒤 포함)로 움직이게 할 수 있습니다. 이 작업에는 1분이 걸립니다.

상수가 언제 돌아올지 모르기 때문에 승현이는 자신의 목표를 달성하기 위해 가능한 한 빨리 작업을 끝내야 합니다. 승현이가 자신의 목표를 달성하기 위해 필요한 **최소한의 시간(분 단위)**를 구하세요.

### 입력 형식

첫 번째 줄에 두 개의 정수 <span class="tex-span"><i>N</i></span>과 <span class="tex-span"><i>K</i></span> (<span class="tex-span">1 &le; <i>K</i> &le; <i>N</i> &le; 5 000</span>)이 주어집니다. <span class="tex-span"><i>N</i></span>은 <span class="tex-span"><i>K</i></span>로 나누어떨어집니다.

두 번째 줄에는 <span class="tex-span"><i>N</i></span>개의 정수들 <span class="tex-span"><i>v<sub>i</sub></i></span> ( <span class="tex-span">1 &le; <i>v<sub>i</sub></i> &le; 10<sup>9</sup></span>)이 공백을 사이로 두고 주어집니다. <span class="tex-span"><i>i</i></span>번째 수는 줄에서 <span class="tex-span"><i>i</i></span>번째로 서 있는 학생의 능력을 나타냅니다.

모든 참가자들의 능력은 서로 다릅니다.

### 출력 형식

첫 번째 줄에 승현이가 자신의 목표를 달성하기 위해 필요한 가장 적은 시간을 분 단위로 출력합니다.

### 채점 방식

30%의 점수에 해당하는 테스트 케이스들은 <span class="tex-span"><i>N</i> &le; 20</span>을 만족합니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">4 1<br>
9 12 5 13</td>
   <td class="code-font">1</td>
  </tr>
  <tr>
   <td class="code-font">6 2<br>
16 2 1 7 5 10</td>
   <td class="code-font">1</td>
  </tr>
  <tr>
   <td class="code-font">6 3<br>
7 9 8 3 6 5</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>

**세 번째 예제의 설명**: 승현이는 능력치가 5, 6, 3인 학생들을 줄 맨 앞으로 움직여야 합니다. 이는 3분이 걸립니다.