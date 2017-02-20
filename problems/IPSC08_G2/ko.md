* [쉬운 버전 풀기](/problems/view/IPSC08_G1)
* [**어려운 입력 - G2**](http://ipsc.ksp.sk/2008/real/problems/g2.in)

* 번역자 주 : 의역했습니다.

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

승현이는 영어 단어를 가지고 놀기를 좋아합니다. 오늘, 승현이는 친구 지학이를 초대하여 두 명의 참가자가 진행하는 게임을 같이 하기로 했습니다. 하지만 지학이는 게임광인 승현이를 절대로 이길 수 없기 때문에, 여러분의 도움이 필요합니다.

### 문제

처음에, 두 참가자는 그들이 게임에서 사용할 단어 목록을 정합니다. 이 목록은 영문 알파벳 소문자로만 구성된 단어들로 이루어져 있어야 합니다.

게임은 텅 빈 문자 <span class="tex-span"><i>S</i></span>로 시작합니다. 차례는 지학이부터 시작하여 번갈아 가며 진행됩니다. 각 차례마다, 자신의 차례인 참가자는 반드시 <span class="tex-span"><i>S</i></span>의 마지막에 문자 하나를 추가해야 합니다.

단어 목록에 있는 단어를 만들거나, <span class="tex-span"><i>S</i></span>가 단어 목록에 있는 어떤 단어의 접두사도 아니도록 문자를 추가한 참가자는 집니다.

여러분이 할 일은 서버와 맞서 이 게임을 진행하여, 이기는 것입니다.

### 입력 형식

입력 파일은 게임에서 사용될 단어 목록을 포함합니다. 첫 번째 줄에는 단어 목록에 있는 단어의 수 <span class="tex-span"><i>N</i></span>이 주어집니다. 이후 <span class="tex-span"><i>N</i></span>개의 줄에는 단어들이 한 줄에 하나씩 주어집니다. 단어들은 서로 다르며, 모든 단어들은 영문 알파벳 소문자로만 구성되어 있습니다.

### 출력 형식

당신의 차례에서 하고 싶은 작업을 나타내는 텍스트 파일을 제출하세요.

만약 여러분이 게임을 계속 진행하고 싶다면, 여러분이 제출할 파일은 단 한 개의 줄에 문자열 끝에 추가할 영문 소문자 하나를 포함하고 있어야 합니다.

만약 여러분이 이번 게임을 포기하고 새로 시작하고 싶다면, 여러분이 제출할 파일은 단 한 개의 줄에 "`RESTART x`"와 같은 형태의 문자열을 포함하고 있어야 합니다. 여기서 `x`는 게임을 초기화한 후 첫 번째 차례에서 여러분이 추가하고 싶은 문자를 나타냅니다.

### 평가 결과

제출한 답안이 유효하지 않다면, 여러분은 오류 메시지를 받게 되며, 게임의 상태는 바뀌지 않습니다.

게임에서 진다면, 여러분은 오류 메시지를 받게 되며, 게임은 재시작됩니다.

게임에서 이긴다면, 정답 처리되며, 해당 입력에 대한 점수를 받습니다.

나머지의 경우에는 (게임을 종료하지 않는 유효한 답안), 여러분은 게임의 진행 상황에 대한 정보를 받게 됩니다.

### 제출 방법

여러분은 **어려운 입력**의 단어 목록으로 게임을 하게 됩니다. 이 입력에 해당하는 텍스트 파일을 제출하세요.

### 예제

#### 단어 목록

<pre>
5
cats
contest
dog
done
dragon
</pre>

#### 상황 1

<pre>
submit: c 
answer: After your move: ’c’. After my move: ’co’. 
submit: n 
answer: After your move: ’con’. After my move: ’cont’. 
submit: e 
answer: After your move: ’conte’. After my move: ’contes’. 
submit: t 
answer: You lost (created a banned word). A new game starts.
</pre>

#### 상황 2

<pre>
submit: c 
answer: After your move: ’c’. After my move: ’co’. 
submit: x 
answer: You lost (nothing starts with ’cox’). A new game starts. 
submit: c 
answer: After your move: ’c’. After my move: ’co’. 
submit: RESTART d 
answer: After your move: ’d’. After my move: ’do’. 
submit: n 
answer: OK
</pre>