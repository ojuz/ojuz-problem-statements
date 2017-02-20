마리타의 남동생은 모든 장난감을 거실 바닥에 어질러놓았다! 다행히도 마리타는 장난감을 정리하는 특별한 로봇들을 개발하였다. 마리타는 어떤 로봇이 어떤 장난감을 집어야 하는지 결정하도록 당신에게 도움을 청했다.

장난감은 총 `T` 개가 있으며, 각각은 정수 무게 `W[i]` 와 정수 크기 `S[i]` 를 가진다.
로봇들은 연약한 로봇과 작은 로봇 두 가지 종류가 있다.

* 연약한 로봇은 총 `A` 개가 있다. 각 연약한 로봇에는 무게 제한 `X[i]` 가 있어서, `X[i]` 미만의 무게를 가진 장난감만을 운반할 수 있다. 장난감의 크기는 상관없다.
* 작은 로봇은 총 `B` 개가 있다. 각 작은 로봇에는 크기 제한 `Y[i]` 가 있어서, `Y[i]` 미만의 크기를 가진 장난감만을 운반할 수 있다. 장난감의 무게는 상관없다.

마리타의 로봇들 각각은 하나의 장난감을 정리하는 데 1분이 걸린다. 여러 로봇들이 서로 다른 장난감들을 동시에 정리할 수 있다.

당신의 임무는 마리타의 로봇들이 모든 장난감들을 정리할 수 있는지 결정하고, 만약 가능하다면, 모든 장난감을 정리하는데 걸리는 가장 짧은 시간을 찾는 것이다.

### 예시

첫 번째 예시로, 무게 제한 `X = [6, 2, 9]` 를 가진 `A = 3` 개의 연약한 로봇과 크기 제
한 `Y = [4, 7]` 을 가진 `B = 2` 개의 작은 로봇이 있고, `T = 10` 개의 장난감이 아래와
같이 있다고 하자:

<div style="text-align: center; width: inherit; margin-bottom: 10px;">

<table class="table table-condensed table-bordered" style="width: 550px; margin: 0 auto;">
  <tr>
   <th style="width: 150px;">장난감 번호</th>
   <td style="width: 40px;">0</td>
   <td style="width: 40px;">1</td>
   <td style="width: 40px;">2</td>
   <td style="width: 40px;">3</td>
   <td style="width: 40px;">4</td>
   <td style="width: 40px;">5</td>
   <td style="width: 40px;">6</td>
   <td style="width: 40px;">7</td>
   <td style="width: 40px;">8</td>
   <td style="width: 40px;">9</td>
  </tr>
  <tr>
   <th>무게</th>
   <td>4</td>
   <td>8</td>
   <td>2</td>
   <td>7</td>
   <td>1</td>
   <td>5</td>
   <td>3</td>
   <td>8</td>
   <td>7</td>
   <td>10</td>
  </tr>
  <tr>
   <th>크기</th>
   <td>6</td>
   <td>5</td>
   <td>3</td>
   <td>9</td>
   <td>8</td>
   <td>1</td>
   <td>3</td>
   <td>7</td>
   <td>6</td>
   <td>5</td>
  </tr>
</table>

</div>

모든 장난감들을 정리하는 데 걸리는 가장 짧은 시간은 3분이다:

<div style="text-align: center; width: inherit; margin-bottom: 10px;">

<table class="table table-bordered table-condensed" style="width: 620px; margin: 0 auto;">
 <tr>
  <th style="width: 70px;"></th>
  <th style="width: 110px;">연약한 로봇 0</th>
  <th style="width: 110px;">연약한 로봇 1</th>
  <th style="width: 110px;">연약한 로봇 2</th>
  <th style="width: 110px;">작은 로봇 0</th>
  <th style="width: 110px;">작은 로봇 1</th>
 </tr>
 <tr>
  <th>1분째</th>
  <td>장난감 0</td>
  <td>장난감 4</td>
  <td>장난감 1</td>
  <td>장난감 6</td>
  <td>장난감 2</td>
 </tr>
 <tr>
  <th>2분째</th>
  <td>장난감 5</td>
  <td></td>
  <td>장난감 3</td>
  <td></td>
  <td>장난감 8</td>
 </tr>
 <tr>
  <th>3분째</th>
  <td></td>
  <td></td>
  <td>장난감 7</td>
  <td></td>
  <td>장난감 9</td>
 </tr>
</table>

</div>

두 번째 예시로, 무게 제한 `X = [2, 5]` 를 가진 `A = 2` 개의 연약한 로봇과 크기 제한 `Y = [2]` 를 가진 `B = 1` 개의 작은 로봇이 있고, `T = 3` 개의 장난감이 아래와 같이 있다고 하자:

<div style="text-align: center; width: inherit; margin-bottom: 10px;">

<table class="table table-condensed table-bordered" style="width: 270px; margin: 0 auto;">
  <tr>
   <th style="width: 150px;">장난감 번호</th>
   <td style="width: 40px;">0</td>
   <td style="width: 40px;">1</td>
   <td style="width: 40px;">2</td>
  </tr>
  <tr>
   <th>무게</th>
   <td>3</td>
   <td>5</td>
   <td>2</td>
  </tr>
  <tr>
   <th>크기</th>
   <td>1</td>
   <td>3</td>
   <td>2</td>
  </tr>
</table>

</div>


어떤 로봇도 무게 5, 크기 3짜리의 장난감을 정리할 수 없기 때문에, 모든 장난감들을 치우는 것은 불가능하다.

### 구현

다음 조건을 만족하는 함수 `putaway()`를 구현한 파일을 제출하시오.

#### 구현해야 할 함수 : `putaway()`

```
int putaway (int A, int B, int T, int X[], int Y[], int W[], int S[]);
```

##### 설명

이 함수는 로봇들이 모든 장난감들을 정리하는데 걸리는 가장 짧은 시간(분)을 계산하여야 한다. 만약 정리하는 것이 불가능하다면, `-1`을 반환해야 한다.

##### 파라미터

* `A` : 연약한 로봇의 개수.
* `B` : 작은 로봇의 개수.
* `T` : 장난감의 개수.
* `X` : 각 연약한 로봇의 무게 제한을 나타내는 길이가 `A`인 배열.
* `Y` : 각 작은 로봇의 크기 제한을 나타내는 길이가 `B`인 배열.
* `W` : 각 장난감의 무게를 나타내는 길이가 `T`인 배열.
* `S` : 각 장난감의 크기를 나타내는 길이가 `T`인 배열.
* 반환값 : 모든 장난감을 정리하는데 걸리는 가장 짧은 시간(분). 만약, 정리하
는 것이 불가능하다면, `-1`.

### 예제 세션

다음 예제 세션은 위의 첫 번째 예시를 나타낸 것이다:

|파라미터|값|
|-|-|
|**`A`**|`3`|
|**`B`**|`2`|
|**`T`**|`10`|
|**`X`**|`[6, 2, 9]`|
|**`Y`**|`[4, 7]`|
|**`W`**|`[4, 8, 27, 1, 5, 3, 8, 7, 10]`|
|**`S`**|`[6, 5, 3, 9, 8, 1, 3, 7, 6, 5]`|
|반환값|`3`|

다음 예제 세션은 위의 두 번째 예시를 나타낸 것이다:

|파라미터|값|
|-|-|
|**`A`**|`2`|
|**`B`**|`1`|
|**`T`**|`3`|
|**`X`**|`[2, 5]`|
|**`Y`**|`[2]`|
|**`W`**|`[3, 5, 2]`|
|**`S`**|`[1, 3, 2]`|
|반환값|`-1`|

### 서브태스크
### 제약 조건

* 시간 제한 : 3초
* 메모리 제한 : 64MB
* `1 ≤ T ≤ 1,000,000`
* `0 ≤ A, B ≤ 50,000` 및 `1 ≤ A + B`
* `1 ≤ X[i], Y[i], S[i] ≤ 2,000,000,000`

### 서브태스크

<table class='table table-condensed table-bordered'>
 <tr>
  <th style="width: 10%;">서브태스크</th>
  <th style="width: 10%;">배점</th>
  <th>추가적인 입력 제한 사항</th>
 </tr>
 <tr>
  <td>1</td>
  <td>14</td>
  <td><code>T = 2</code> 및 <code>A + B = 2</code> (정확히 두 개의 장난감 및 두 개의 로봇)</td>
 </tr>
 <tr>
  <td>2</td>
  <td>14</td>
  <td><code>B = 0</code> (모든 로봇이 연약함)</td>
 </tr>
 <tr>
  <td>3</td>
  <td>25</td>
  <td><code>T ≤ 50</code> 및 <code>A + B ≤ 50</code></td>
 </tr>
 <tr>
  <td>4</td>
  <td>37</td>
  <td><code>T ≤ 10,000</code> 및 <code>A + B ≤ 1,000</code></td>
 </tr>
 <tr>
  <td>5</td>
  <td>10</td>
  <td>(없음)</td>
 </tr>
</table>

### 테스트용 입력 형식

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/IOI13_wombats/robots.zip)서 내려받을 수 있는 샘플 그레이더는 입력을 파일 `robots.in`에서 읽어들이는데, 포맷은 다음과 같아야 한다.

* line 1: `A B T`
* line 2 : `X[0] X[1] ` ... ` X[A - 1]`
* line 3 : `Y[0] Y[1] ` ... ` Y[B - 1]`
* the next `T` lines : `W[i] S[i]`

예를 들어, 위의 첫 번째 예시는 다음과 같은 형식을 따라야 한다.

<pre>
3 2 10
6 2 9
4 7
4 6
8 5
2 3
7 9
1 8
5 1
3 3
8 7
7 6
10 5
</pre>

만약 `A = 0` 또는 `B = 0`이라면, 해당하는 (두 번째 또는 세 번째) 줄은 비어 있어야 한다.

### 언어 유의사항

<table class="table table-condensed table-bordered">
 <tr>
  <th style="width: 15%;">C/C++</th>
  <td>당신의 프로그램은 <code>#include "robots.h"</code> 명령어를 통해 헤더 파일을 추가시켜야 한다.</td>
 </tr>
 <tr>
</table>

예시를 위해서 솔루션 템플릿을 참조하시오.