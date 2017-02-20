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

셀 수 없을 정도로 많은 달리기 선수들은 올해 [Zagreb Marathon](http://www.zagreb-marathon.com/)에 참가하고 싶어했습니다. 이 대회는 42125m 길이의 전통적인 달리기 경주입니다. 흥미로운 통계적인 정보는, 매년 **한 사람만 제외하고** 모든 참가자가 경주를 마무리해냈다는 것입니다.

마라톤들은 참가에 의의가 있기 때문에, 주최 측이 등록된 선수들의 목록과 순위표를 기반으로 경주를 마무리하지 않은 참가자의 신원을 찾아낼 수 있도록 도와주세요.

### 입력 형식

첫 번째 줄에 참가자의 수 <span class="tex-span"><i>N</i></span> (<span class="tex-span">1 &le; <i>N</i> &le; 10<sup>5</sup></span>)이 주어집니다.

다음 <span class="tex-span"><i>N</i></span>개의 줄에는 등록된 선수들의 이름이 한 줄에 하나씩 주어집니다. 그 다음 <span class="tex-span"><i>N</i> - 1</span>개의 줄에는 경주를 마무리한 선수들의 이름이 빨리 끝낸 순으로 한 줄에 하나씩 주어집니다.

참가자들의 이름은 영문 알파벳 소문자로, 최소 1글자, 최대 20글자입니다. 참가자들의 이름이 반드시 서로 다르다는 보장은 없습니다.

### 출력 형식

첫 번째 줄에 경주를 끝내지 못한 선수의 이름을 출력합니다.

### 채점

50%의 점수에 해당하는 테스트 케이스들은 <span class="tex-span">1 &le; <i>N</i> &le; 1 000</span>을 만족합니다.


<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">3<br>
leo<br>
kiki<br>
eden<br>
eden<br>
kiki</td>
   <td class="code-font">leo</td>
  </tr>
  <tr>
   <td class="code-font">5<br>
marina<br>
josipa<br>
nikola<br>
vinko<br>
filipa<br>
josipa<br>
filipa<br>
marina<br>
nikola</td>
   <td class="code-font">vinko</td>
  </tr>
  <tr>
   <td class="code-font">4<br>
mislav<br>
stanko<br>
mislav<br>
ana<br>
stanko<br>
ana<br>
mislav</td>
   <td class="code-font">mislav</td>
  </tr>
 </tbody>
</table>