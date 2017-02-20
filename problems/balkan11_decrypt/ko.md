승현이가 여자 친구와 문자 메시지를 주고받기 위해 특수한 장치를 이용한다는 소문이 돌고 있습니다. 만약 여러분이 이 장치를 깰 수만 있다면 승현이가 여자 친구에게 보내는 손발이 오그라드는 문장들을 모두에게 알릴 수 있게 됩니다. 어제 저는 승현이를 만났고, 승현이는 운 좋게도 장치가 든 가방을 두고 갔습니다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/balkan11_decrypt/bag.png" alt="" />
</div>

모든 연산은 8비트로 처리됩니다. XOR는 배타적 논리합 함수 (C에서 `^` 연산자)입니다. `R`은 의사 난수로 구성된 수열로 아래와 같이 정의됩니다.

* `R[0]`, `R[1]`, `R[2]`는 승현이만 알고 있는 특수한 값을 가집니다.
* `n = 3, 4, ...`에 대해 `R[n] = R[n-2] XOR R[n-3]`

또한, 함수 $M : [0...255] \rightarrow [0..255]$이 있습니다. 함수 $M$은 전단사함수라서 $x \neq y$라면 $M(x) \neq M(y)$를 만족해야 합니다.

승현이가 쓰는 장치는 한 번에 숫자 하나를 읽고 그 즉시 암호화된 숫자를 출력합니다. 장치를 `N`번 쓴 후, 장치에 숫자 `INPUT`를 입력하면, 아래와 같이 암호화됩니다.

* `OUTPUT = M(INPUT XOR R[N])`

여러분이 승현이의 장치가 어떻게 돌아가는지 이해했다고 하더라도, `R[0]`, `R[1]`, `R[2]`의 값은 알 수 없습니다. 또한, 여러분은 함수 `M`이 어떻게 생겼는지 모르기 때문에, 문자 메시지를 읽을 수가 없습니다. 그 대신 여러분은 제가 찾은 기계에 직접 값을 넣어 보고 기계가 돌려주는 값을 읽을 수 있습니다.

### 해야 할 일

여러분은 승현이의 기계 속에 숨겨진 값들 `R[0], R[1], R[2], M[0], M[1], ..., M[255]`를 모두 찾아야 합니다.

### 제한

* 기계에 값을 입력한 횟수가 320번 이하여야 점수를 받을 수 있습니다.
* `R[0], R[1], R[2], M[0], M[1], ..., M[255]`의 값은 무작위하게 채택되었습니다.
* `0 ≤ INPUT, OUTPUT, R, M ≤ 255`

### 구현

이 문제는 인터렉티브 문제로 여러분은 숨겨진 값들을 알아내는 함수 `crackDevice()`를 구현한 파일을 제출해야 합니다. 이 함수는 그레이더 함수 `get()`을 최대 320번 호출할 수 있습니다. 숨겨진 값들을 모두 찾아냈다면 첫 번째 줄에 **`SOLUTION`**을 출력한 뒤 `R[0], R[1], R[2], M[0], M[1], ..., M[255]`의 값을 표준 출력(stdout)으로 한 줄에 하나씩 (259줄) 출력한 후 종료해야 합니다.

#### 그레이더 함수 : `get()`

```
int get (int x);
```

##### 설명

이 함수는 그레이더에 포함되어 있습니다. 이 함수는 위에서 서술한 기계의 동작 원리를 이용하여 `x`를 암호화한 값을 돌려줍니다. 이 함수는 `O(1)` 시간에 동작하며, 최대 320번 호출할 수 있습니다.

##### 파라미터

* `x`: 기계에 입력할 값. (`0 ≤ x ≤ 255`)

### 예제 세션

#### 구현해야 하는 함수 : `crackDevice()`

```
void crackDevice ();
```

##### 설명

이 함수를 구현하여 제출해야 합니다.

이 함수는 승현이의 장치에 몇 가지 입력을 넣어보기 위해 그레이더 함수 `get()`을 이용해야 하며, 숨겨진 값들을 알아내면 위에서 서술한 대로

* 첫 번째 줄에 "`SOULTION`"(따옴표 제외) 를 출력하고
* 다음 259개 줄에 `R[0], R[1], R[2], M[0], M[1], ..., M[255]`의 값을 한 줄에 하나씩 출력해야 합니다.

위의 조건을 하나라도 만족하지 않을 시 해당 입력에서 점수를 받을 수 없습니다.

### 파일 내려받기

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/balkan11_decrypt/decrypt.zip)를 클릭하여 `decrypt.zip` 파일을 받으세요. 이 파일은 소스 코드를 작성할 때 이용할 수 있는 `decrypt.h`, `grader.c`와 여러분이 구현해야 할 파일 `decrypt.c`, `decrypt.cpp`가 있습니다. (둘 중 하나만 구현해서 제출하면 됩니다.)

### 예제

`R[0] = 0, R[1] = 1, R[2] = 3, M(i) = (i+1) modulo 256`으로 가정합시다. 여기서 `R[3] = 1`임을 알 수 있습니다.


<table class="table table-bordered">
 <tr>
  <th style="width: 35%;">Function Call</th>
  <th style="width: 15%;">Returns</th>
  <th>Explanation</th>
 </tr>
 <tr>
  <td><code>get(10)</code></td>
  <td><code>11</code></td>
  <td>$M(10 \oplus 0) = M(10) = 11$</td>
 </tr>
 <tr>
  <td><code>get(10)</code></td>
  <td><code>12</code></td>
  <td>$M(10 \oplus 1) = M(11) = 12$</td>
 </tr>
 <tr>
  <td><code>get(11)</code></td>
  <td><code>9</code></td>
  <td>$M(11 \oplus 3) = M(8) = 9$</td>
 </tr>
 <tr>
 <tr>
  <td><code>get(12)</code></td>
  <td><code>14</code></td>
  <td>$M(12 \oplus 1) = M(13) = 14$</td>
 </tr>
 <tr>
  <td>...</td>
  <td>...</td>
  <td>...</td>
 </tr>
 <tr>
  <th style="width: 50%;">출력</th>
  <th colspan="2">Explanation</th>
 </tr>
 <tr>
  <td><pre>
SOLUTION
0
1
3
1
2
3
4
...
254
255
0
</pre></td>
  <td colspan="2">모든 숨겨진 값들을 알아냈으므로 이를 표준 출력에 출력합니다.</td>
 </tr>
</table>


### 프로그래밍 언어 유의사항

<table class="table table-condensed table-bordered">
 <tr>
  <th style="width: 15%;">C/C++</th>
  <td><code>#include "decrypt.h"</code>를 해야 한다.</td>
 </tr>
 <tr>
</table>

예시를 위해서 솔루션 템플릿을 참조하시오.
