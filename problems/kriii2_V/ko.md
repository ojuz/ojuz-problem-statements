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

위대한 사이버 국방학과에 다니는 원철이는 대한민국의 국방을 위한 암호학 시간에 카이사르 암호에 대해 배웠다. 카이사르 암호는 매우 유명한 암호체계로 매우 간단한 치환암호의 일종이다. 간단히 설명하면 다음과 같다.

1. <span class="code-font">a</span>를 0, <span class="code-font">b</span>를 1, ..., <span class="code-font">z</span>를 25로 취급한다.
2. 어떤 키 <span class="tex-span"><i>n</i></span>을 가지고 번호 <span class="tex-span"><i>x</i></span>를 암호화하면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_V/eq1.png"/>이 된다. 예를 들어 <span class="tex-span"><i>n</i>&thinsp;=&thinsp;1</span>인 경우 <span class="code-font">a</span>는 <span class="code-font">b</span>가 되고, <span class="code-font">b</span>는 <span class="code-font">c</span>가 되고, ..., <span class="code-font">z</span>는 <span class="code-font">a</span>가 된다.
3. 암호화된 번호 <span class="tex-span"><i>y</i></span>를 복호화하면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_V/eq2.png"/>이 된다.

원철이는 이 암호의 단점도 같이 배웠다. 그것은 글자의 빈도수를 분석해 보는 것으로 암호가 쉽게 파악될 수 있다는 것이다. 똑똑한 원철이는 한 글자를 두 글자로 암호화하여 이러한 단점을 피할 수 있을 것이라고 생각했다. 즉 "<span class="tex-span"><i>x</i></span>"를 어떤 "<span class="tex-span"><i>yz</i></span>"로 암호화하겠다는 것이다. 원철이는 카이사르 암호와 비슷하게 "<span class="tex-span"><i>x</i></span>"를 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_V/eq3.png"/>이 되는 "<span class="tex-span"><i>y</i><i>z</i></span>"로 암호화하는 방식을 *원철 암호*라고 하기로 했다. 만약 암호화해야 할 것이 글자가 아닌 단어라면, 단어의 맨 앞에서부터 차례대로 한 글자씩 암호화한 것을 순서대로 붙여서 사용하기로 했다.

그러나 원철이는 이런 식으로 암호화를 하게 되면 단어의 길이가 모두 짝수가 되므로 이 암호문이 원철 암호를 사용했다는 사실이 파악될 수 있다는 사실을 깨달았다. 그러므로 원철이는 암호화된 단어의 맨 뒤에 마음대로 더미(dummy) 글자를 한 글자 붙일 수도 있다.

원철이는 원철 암호를 생각한 뒤부터 일상생활의 모든 대화를 원철 암호로 하기 시작했다. 당신은 원철이가 하는 말을 알아 들을 수 있을까?

### 입력 형식

첫 번째 줄에는 암호화에 사용되는 키를 의미하는 정수 <span class="tex-span"><i>n</i></span> (<span class="tex-span">0 &le; <i>n</i> &lt; 26</span>)이 주어진다.

두 번째 줄은 100개 이하의 단어로 구성되어 있다. 각 단어의 길이는 2 이상 101 이하이고 영어 소문자('<span class="code-font">a</span>'-'<span class="code-font">z</span>')로만 구성되어 있으며 공백 하나로 구분되어 있다. 이 단어는 모두 원철 암호로 암호화된 단어이다.

쉬운 문제에서는 단어가 하나만 주어진다.

어려운 문제에서는 별다른 제약조건이 없다.

### 출력 형식

입력에서 주어진 순서대로 원철 암호로 암호화된 단어를 복호화하여 공백 하나로 구분하여 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2<BR>
axcexseg yzkansuqe mlssltqu</td>
   <td class="code-font">veni vidi vici</td>
  </tr>
 </tbody>
</table>
