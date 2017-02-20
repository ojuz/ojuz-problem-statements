세 명의 친구 승현이, 지학이와 석환이는 다음과 같은 놀이를 하는 것을 좋아합니다. 승현이는 문자열 $S$를 고릅니다. 그 다음 지학이는 $S$를 두 번 복사한 것(two copies of the string $S$) 문자열 $T$를 만듭니다. 마지막으로 석환이는 $T$의 맨 앞, 맨 뒤, 또는 아무 곳에나 글자 하나를 끼워넣은 문자열 $U$를 만듭니다.

### 해야 할 일

여러분에게 문자열 $U$가 주어집니다. 여러분이 할 일은 원래 문자열 $S$를 다시 만드는 것입니다.

### 입력 형식

첫 번째 줄에 최종 문자열 $U$의 길이 $N$이 주어집니다. 두 번째 줄에 문자열 $U$가 주어집니다. $U$는 알파벳 대문자 ('A', 'B', 'C', ..., 'Z')만을 포함합니다.

### 출력 형식

여러분의 프로그램은 원래 문자열 $S$를 출력해야 합니다. 하지만, 두 개의 예외가 있습니다:

1. 위에서 기술한 방법대로 최종 문자열 $U$를 만들 수 없다면, 여러분은 `NOT POSSIBLE`을 출력해야 합니다.
2. 원래 문자열 $S$가 유일하지 않은 경우, 여러분은 `NOT UNIQUE`를 출력해야 합니다.

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
   <td class="code-font">7<br/>
ABXCABC</td>
   <td class="code-font">ABC</td>
  </tr>
  <tr>
   <td class="code-font">6<br/>
ABCDEF</td>
   <td class="code-font">NOT POSSIBLE</td>
  </tr>
  <tr>
   <td class="code-font">9<br/>
ABABABABA
</td>
   <td class="code-font">NOT UNIQUE</td>
  </tr>
 </tbody>
</table>

### 채점

#### 서브태스크 1 (35점)

$2 \le N \le 2,001$

#### 서브태스크 2 (65점)

$2 \le N \le 2,000,001$

### 제약 조건

**시간 제한**: 0.5 초

**메모리 제한**: 256 MB