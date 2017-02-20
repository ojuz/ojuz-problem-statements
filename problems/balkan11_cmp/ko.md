여러분은 메모리가 10240비트의 1차원 배열에 불과한 고대의 컴퓨터에서 실행할 알고리즘을 작성해야 합니다. 초기에 메모리는 0으로 초기화되어 있고, 여러분은 한 비트 단위로 쓰고 읽을 수 있습니다.

여러분은 이 컴퓨터에서 동작할 두 가지의 함수를 작성해야 합니다.

#### **`remember(a)`**: `a`는 0 이상 4095 이하의 정수입니다.
  - 이 함수는 아래의 그레이더 함수를 호출할 수 있습니다.
    - **`bit_set(address)`**: `address`는 1 이상 10240 이하의 정수입니다. 이 함수를 호출하면 고대 컴퓨터의 `address`번째 비트가 1로 바뀔 것입니다.

#### **`compare(b)`**: `b`는 0 이상 4095 이하의 정수입니다.
  - 만약 `b < a`라면 이 함수는 `-1`을 반환해야 합니다.
  - 만약 `b = a`라면 이 함수는 `0`을 반환해야 합니다.
  - 만약 `b > a`라면 이 함수는 `1`을 반환해야 합니다.
  - 이 함수는 아래의 그레이더 함수를 호출할 수 있습니다.
    - **`bit_get(address)`**: 고대 컴퓨터의 `address`번째 비트에 저장된 값을 돌려줍니다: 즉 만약 `remember(a)`에서 `bit_get(address)` 함수가 호출되었다면 `1`이 반환되고, 그렇지 않다면 `0`이 반환됩니다.

### 해야 할 일

`remember()` 함수와 `compare()` 함수를 구현하세요. 이 때 모든 가능한 `a`와 `b`값에 대해 메모리에 접근(`bit_set()` 호출과 `bit_get()`)하는 횟수를 최소화해야 합니다.

여러분이 제출한 소스 코드는 아래와 같이 채점됩니다.

<pre>
define AllMemory = array [0..4095][1..10240] of bits
set AllMemory to zeros
for a = 0..4095:
	define bit_set(address): AllMemory[a][address] = 1
	remember(a)
let maxA= the maximum number of bit_set() calls executed for any a
for (a,b) ∈ {0..4095}×{0..4095} in random order (i.e. all valid pairs (a,b) are considered, in some random order)
	define bit_get(address): return AllMemory[a][address]
	answer =compare(b)
	if answer for comparing a and b is incorrect : your score = 0; exit
let maxB = the maximum number of bit_get() calls executed for any (a,b) pair
T=maxA + maxB
If (T>20): your score = 0; exit
else your score = 1 + 9 * (21? T); exit
</pre>

### 구현 시 유의사항

여러분의 소스 코드는 반드시 아래 줄로 시작해야 합니다.

```
#include "cmp.h"
```

메모리에 접근하는 두 가지 함수의 프로토타입은 아래와 같습니다.

```
void bit_set (int addr);
int bit_get (int addr);
```

여러분은 아래 두 함수를 구현해야 합니다.

```
void remember (int value);
int compare (int value);
```

#### 파일 내려받기

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/balkan11_cmp/cmp.zip)를 클릭하여 `cmp.zip` 파일을 받으세요. 이 파일은 소스 코드를 작성할 때 이용할 수 있는 `cmp.h`와 여러분이 구현해야 할 파일 `cmp.c`, `cmp.cpp`가 있습니다. (둘 중 하나만 구현해서 제출하면 됩니다.)

### 제약 조건

* 그레이더의 메모리에 접근하려고 해서는 안 됩니다
* 위에 적어 놓은 제약 조건을 만족하지 않는 코드를 제출할 시(예: `bit_set()` 함수를 `compare()`에서 호출), 0점을 받습니다
* **시간 제한**: 여러분이 제출한 코드는 4096번의 `remember()` 호출과 `4096*4096`번의 `compare()` 호출을 10초 안에 실행해야 합니다.