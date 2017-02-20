JOIOJI씨는 JOI군의 작은아버지입니다. JOIOJI씨는 J, O, I가 각각 두 글자씩 들어가 있는 자신의 이름을 마음에 들어합니다.

최근 JOIOJI씨에게 아이가 태어났습니다. JOIOJI씨는 아이에게도 자신과 마찬가지로 J, O, I로 구성되며 각각의 문자가 정확히 같은 횟수만큼 들어간 이름을 지어 주려고 생각하고 있습니다.

JOIOJI씨는 집안 대대로 전해져 오는 두루마리를 가지고 있습니다. 이 두루마리에는 시 한 편이 쓰여 있습니다. 시는 J, O, I로만 이루어진 길이가 $N$인 문자열입니다. JOIOJI씨는 시에 포함된 연속하는 부분문자열들 중, J, O, I가 같은 횟수만큼 들어가 있는 문자열들 중, 그 길이가 가장 긴 것을 이름으로 붙일 예정입니다.

### 해야 할 일

JOIOJI씨가 가지고 있는 두루마리에 쓰여 있는 시가 주어집니다. 시에 포함된 연속한 문자열들 중 J, O, I가 같은 횟수만큼 나타나는 가장 긴 문자열의 길이를 구하는 프로그램을 작성하세요.

### 입력

표준 입력에서 아래 입력을 받으세요.

* 첫 번째 줄에 정수 $N$이 주어집니다. $N$은 두루마리에 적혀 있는 시의 길이를 나타냅니다.
* 두 번째 줄에는 길이가 $N$인 문자열 $S$가 주어집니다. $S$는 두루마리에 적혀 있는 시를 나타내며, 각 문자는 J, O, I 중 하나입니다.

### 출력

표준 출력의 첫 번쨰 줄에 시에 포함된 연속하는 부분문자열 중 J, O, I가 같은 횟수만큼 나타나는 가장 긴 문자열의 길이를 출력하세요. 단 그러한 문자열이 존재하지 않는다면 0을 출력하세요.

### 제약 조건

모든 입력 데이터는 아래 조건을 만족합니다.

* $1 \le N \le 200,000$

### 서브태스크

#### 서브태스크 1 [5점]

* $N \le 200$

#### 서브태스크 2 [15점]

* $N \le 4,000$

#### 서브태스크 3 [80점]

* $N \le 200,000$

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">10<br/>
JOIIJOJOOI</td>
   <td class="code-font">6</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">8<br/>
IOIIJIIO
</td>
   <td class="code-font">0</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">20<br/>
JJIOOIJIJOIOJIOJOOIJ</td>
   <td class="code-font">15</td>
  </tr>
 </tbody>
</table>