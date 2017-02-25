마오공 곤돌라는 타이페이의 명소 중 하나이다. 곤돌라 시스템은 원형의 레일과, 하나의 정류장이 있고, 1 부터 $n$까지 순서대로 번호가 붙은 $n$개의 곤돌라가 모두 단일한 방향으로 레일을 따라 움직이는 형태이다. $i$번 곤돌라가 정류장을 지난 직후에는 $i+1$번 곤돌라가 정류장을 지나가게 된다. (단, $i=n$번 곤돌라가 지나간 직후에 1 번 곤돌라가 지나가게 된다.)

곤돌라들은 고장이 나기도 한다. 다행히 무제한으로 많은 곤돌라의 여분이 있고, 여분 곤돌라들은 $n+1$, $n+2$과 같이 순차적으로 번호가 붙어 있다. 특정한 곤돌라가 고장이 나면 고장난 곤돌라는 빼고, 동일한 위치에 여분 곤돌라를 배치한다. 여분 곤돌라는 작은 번호부터 사용된다. 예를 들어, 사용하는 곤돌라 수가 총 5 개이고, 1 번 곤돌라가 고장난다면, 그 곤돌라는 6번으로 교체된다.

당신은 정류장에 서서 곤돌라들이 지나가는 것을 즐겨 본다. **곤돌라 수열**이라는 것은 임의의 시점에서 시작해서 정류장을 지나가는 $n$개의 곤돌라들의 번호를 순서대로 적은 것이다. 곤돌라 수열을 적기 시작하는 시점 이전에 이미 몇개의 곤돌라가 고장나서 교체되었을 수 있다. 하지만, 곤돌라 수열을 적는 도중에는 아무 곤돌라도 고장이 나지 않는다.

전체적으로 곤돌라들의 배치가 동일하더라도 어떤 시점에 곤돌라 수열을 적기 시작하느냐에 따라 서로 다른 곤돌라 수열이 나올수 있다는 점에 주의하자. 예를 들어, 총 5개의 곤돌라들 중 고장난 곤돌라가 없는 경우에 (2, 3, 4, 5, 1) 과 (4, 5, 1, 2, 3) 은 모두 가능한 곤돌라 수열들이다. 하지만, 이 경우 (4, 3, 2, 5, 1) 은 가능한 곤돌라 수열이 아니다. (곤돌라 번호의 순서가 잘못되어 있다.)

만약 곤돌라 1번 만이 고장난 상황이라면, (4, 5, 6, 2, 3) 의 곤돌라 수열을 만들 수 있다. 만약 이후 4번 곤돌라가 고장난다면, 7번 곤돌라가 그 자리에 있게 되고, (6, 2, 3, 7, 5) 가 가능한 곤돌라 수열이 된다. 만약 7번 곤돌라가 이후에 고장이 난다면, 8번이 그 자리를 차지할 것이고 (3, 8, 5, 6, 2) 가 가능한 곤돌라 수열들 중 하나가 된다.

 <div class="table-responsive">
 <table class="table table-bordered table-condensed">
  <thead>
   <tr>
    <th class="col-sm-3 col-md-3 col-lg-3">고장난 곤돌라</th>
    <th class="col-sm-3 col-md-3 col-lg-3">새 곤돌라</th>
    <th class="col-sm-6 col-md-6 col-lg-6">가능한 곤돌라 수열 중 하나</th>
   </tr>
  </thead>
  <tbody>
   <tr><td>1</td><td>6</td><td>(4, 5, 6, 2, 3)</td></tr>
   <tr><td>4</td><td>7</td><td>(6, 2, 3, 7, 5)</td></tr>
   <tr><td>7</td><td>8</td><td>(3, 8, 5, 6, 2)</td></tr>
  </tbody>
 </table>
 </div>

**교체 수열**이라는 것은 고장난 곤돌라들의 번호를 고장난 순서에 따라 쓴 것이다. 직전의 예에서 교체 수열은 (1, 4, 7) 이다. 교체 수열 $r$이 곤돌라 수열 $g$를 **만든다**고 말을 할 수 있는데, 그것은 초기 상황에서 시작해서 $r$에 해당하는 방법으로 곤돌라들이 고장난 직후에, $g$가 가능한 곤돌라 수열들 중 하나인 경우를 의미한다.

### 곤돌라 수열 확인

처음 세 개의 부분 문제에서는 입력 수열이 곤돌라 수열로서 가능한 것인지 확인하여야 한다. 몇 개의 곤돌라가 고장나서 교체된 상태일 수도 있다. 아래 표에는 곤돌라 수열인 예들과 곤돌라 수열이 아닌 예들이 나와 있다. 아래와 같이 선언된 `valid` 함수를 구현하여야 한다.

* `valid(n, inputSeq)`
  - `n`: 입력 수열의 길이.
  - `inputSeq`: 크기 $n$인 배열; `inputSeq[i]` 는 입력의 $i$번 원소이다 ($0 \le i \le n-1$).
  - 함수는 입력이 곤돌라 수열로서 가능한 경우 1을, 아닌 경우 0을 리턴해야 한다.
  
#### 부분 문제 1, 2, 3

<div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2">$n$ </th>
  <th class=""><code>inputSeq</code></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>5</td>
  <td>$n \le 100$</td>
  <td>1부터 $n$까지의 수들이 정확히 한번씩 나온다</td>
 </tr>
 <tr>
  <td>2</td>
  <td>5</td>
  <td>$n \le 100,000$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le n$</td>
 </tr>
 <tr>
  <td>3</td>
  <td>10</td>
  <td>$n \le 100,000$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le 250,000$</td>
 </tr>
</tbody>
</table>
</div>
</div></div>

#### 예제

<div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
 <thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><code>inputSeq</code></th>
  <th class="col-sm-2 col-md-2 col-lg-2">리턴 값</th>
  <th class="">비고</th>
 </tr>
 </thead>
 <tbody>
 <tr>
  <td>1</td>
  <td>(1, 2, 3, 4, 5, 6, 7)</td>
  <td>1</td>
  <td></td>
 </tr>
 <tr>
  <td>1</td>
  <td>(3, 4, 5, 6, 1, 2)</td>
  <td>1</td>
  <td></td>
 </tr>
 <tr>
  <td>1</td>
  <td>(1, 5, 3, 4, 2, 7, 6)</td>
  <td>0</td>
  <td>1 이 5 의 직전에 나오는 것은 불가능</td>
 </tr>
 <tr>
  <td>1</td>
  <td>(4, 3, 2, 1)</td>
  <td>0</td>
  <td>4 가 3 의 직전에 나오는 것은 불가능</td>
 </tr>
 <tr>
  <td>2</td>
  <td>(1, 2, 3, 4, 5, 6, 5)</td>
  <td>0</td>
  <td>5 번 곤돌라가 두 개</td>
 </tr>
 <tr>
  <td>3</td>
  <td>(2, 3, 4, 9, 6, 7, 1)</td>
  <td>1</td>
  <td>교체 수열 (5, 8) 로 가능</td>
 </tr>
 <tr>
  <td>3</td>
  <td>(10, 4, 3, 11, 12)</td>
  <td>0</td>
  <td>4 가 3 의 직전에 나오는 것은 불가능</td>
 </tr>
 </tbody>
</table>
</div>
</div></div>

### 교체 수열

다음 세 개의 부분 문제들에서는 주어진 곤돌라 수열을 만들 수 있는 교체 수열을 생성하여야 한다. 여러 개의 교체 수열이 가능한 경우 그 중 하나를 생성하면 된다. 다음과 같이 선언된 함수 `replacement` 를 구현해야 한다.

* `replacement(n, gondolaSeq, replacementSeq)`
 - `n`: 입력 곤돌라 수열의 길이이다.
 - `gondolaSeq`: 크기 $n$인 배열; gondolaSeq 는 항상 가능한 곤돌라 수열이며, `gondolaSeq[i]` 는 $i$번 원소이다 ($0 \le i \le n-1$).
 - 함수는 교체 수열의 길이 $l$을 리턴해야 한다.
 - `replacementSeq`: 교체 수열을 저장하기에 충분한 크기의 배열; `replacementSeq[i]` 에는 계산된 교체 수열의 $i$번 원소가 저장되어야 한다 ($0 \le i \le l-1$).
 
#### 부분 문제 4, 5, 6

<div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2">$n$ </th>
  <th class=""><code>gondolaSeq</code></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>4</td>
  <td>5</td>
  <td>$n \le 100$</td>
  <td>$1 \le $ <code>gondolaSeq[i]</code> $\le n+1$</td>
 </tr>
 <tr>
  <td>5</td>
  <td>10</td>
  <td>$n \le 1,000$</td>
  <td>$1 \le$ <code>gondolaSeq[i]</code> $\le 5,000$</td>
 </tr>
 <tr>
  <td>6</td>
  <td>20</td>
  <td>$n \le 100,000$</td>
  <td>$1 \le$ <code>gondolaSeq[i]</code> $\le 250,000$</td>
 </tr>
</tbody>
</table>
</div>
</div></div>

#### 예제

<div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
 <thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">부분문제</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><code>gondolaSeq</code></th>
  <th class="col-sm-3 col-md-3 col-lg-3">리턴 값</th>
  <th class=""><code>replacementSeq</code></th>
 </tr>
 </thead>
 <tbody>
 <tr>
  <td>4</td>
  <td>(3, 1, 4)</td>
  <td>1</td>
  <td>(2)</td>
 </tr>
 <tr>
  <td>5</td>
  <td>(5, 1, 2, 3, 4)</td>
  <td>0</td>
  <td>( )</td>
 </tr>
 <tr>
  <td>6</td>
  <td>(2, 3, 4, 9, 6, 7, 1)</td>
  <td>2</td>
  <td>(5, 8)</td>
 </tr>
 </tbody>
</table>
</div>
</div></div>

### 교체 수열의 개수 세기

다음 네 개의 부분 문제들에서는 주어진 수열(가능한 곤돌라 수열일 수도 아닐 수도 있음)을 만들 수 있는 교체 수열의 수를 세어서 그 값을 1,000,000,009 로 나눈 나머지를 계산해야 한다. 다음과 같이 선언된 함수 `countReplacement` 를 구현해야 한다.

* `countReplacement(n, inputSeq)`
 - `n`: 입력 수열의 길이.
 - `inputSeq`: 크기 $n$인 배열; `inputSeq[i]`는 입력 수열의 $i$번 원소이다 ($0 \le i \le n-1$).
 - 입력이 곤돌라 수열인 경우, 입력의 곤돌라 수열을 만들 수 있는 모든 교체 수열의 수를 센 다음에 (그 수는 매우 클수 있음) 그 결과를 **1,000,000,009** 로 나눈 나머지를 리턴해야 한다. 만약 입력이 곤돌라 수열이 아닌 경우 0을 리턴해야 한다. 입력이 곤돌라 수열이고 고장난 곤돌라가 하나도 없는 경우는 1을 리턴해야 한다.
 
#### 부분문제 7, 8, 9, 10

 <div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2">$n$ </th>
  <th class=""><code>inputSeq</code></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>7</td>
  <td>5</td>
  <td>$4 \le n \le 50$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le n+3$</td>
 </tr>
 <tr>
  <td>8</td>
  <td>15</td>
  <td>$4 \le n \le 50$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le 100$이고 초기 곤돌라들 중 (즉, $1, ..., n$번 중) 최소한 $n-3$개는 고장이 나지 않았다.</td>
 </tr>
 <tr>
  <td>9</td>
  <td>15</td>
  <td>$n \le 100,000$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le 250,000$</td>
 </tr>
 <tr>
  <td>10</td>
  <td>10</td>
  <td>$n \le 100,000$</td>
  <td>$1 \le$ <code>inputSeq[i]</code> $\le 1,000,000,000$</td>
 </tr>
</tbody>
</table>
</div>
</div></div>

#### 예제

<div class="row"> <div class="col-sm-12 col-md-12 col-lg-12">
<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
 <thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-3 col-md-3 col-lg-3"><code>inputSeq</code></th>
  <th class="col-sm-2 col-md-2 col-lg-2">리턴 값</th>
  <th class="">교체 수열</th>
 </tr>
 </thead>
 <tbody>
 <tr>
  <td>7</td>
  <td>(1, 2, 7, 6)</td>
  <td>2</td>
  <td>(3, 4, 5) or (4, 5, 3)</td>
 </tr>
 <tr>
  <td>8</td>
  <td>(2, 3, 4, 12, 6, 7, 1)</td>
  <td>1</td>
  <td>(5, 8, 9, 10, 11)</td>
 </tr>
 <tr>
  <td>9</td>
  <td>(4, 7, 4, 7) </td>
  <td>0</td>
  <td><code>inputSeq</code> 가 곤돌라 수열이 아님</td>
 </tr>
 <tr>
  <td>10</td>
  <td>(3, 4) </td>
  <td>2</td>
  <td>(1, 2) or (2, 1)
</td>
 </tr>
 </tbody>
</table>
</div>
</div></div>

### 구현 주의 사항

단 하나의 파일을 제출해야 한다. 이름은 `gondola.c` 또는 `gondola.cpp` 이다. 이 파일에는 위에서 말한 세가지 함수가 다 존재해야 한다. (부분 문제들 중 일부만 풀려고 하는 경우도 마찬가지이다.) 다음의 함수 선언을 이용해야 한다. C/C++ 구현에서는 `gondola.h` 를 `#include`해야 한다.

```c++
int valid(int n, int inputSeq[]);
int replacement(int n, int gondolaSeq[], int replacementSeq[]);
int countReplacement(int n, int inputSeq[]);
```

#### Sample grader

Sample grader의 입력 양식은 다음과 같다.

* line 1: `T`, 풀려고 하는 부분 문제의 번호 ( ).
* line 2: `n`, 입력 수열의 길이.
* line 3: `T` 가 4, 5, 6 인 경우, 이 줄에는 `gondolaSeq[0]`, ..., `gondolaSeq[n-1]` 가 있고, 그렇지 않은 경우 `inputSeq[0]`, ..., `inputSeq[n-1]` 가 있다.
