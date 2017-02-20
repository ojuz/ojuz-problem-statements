<div style="text-align: center; margin-bottom: 10px;"><img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NOI12_forensic/fig1.png" style=""/></div>

지학이는 오늘도 위와 같이 생긴 배열 $A$를 가지고 놀고 있습니다. 이 배열은 1차원 연결 리스트의 *포인터*들을 저장합니다. 이 문제에서 포인터는 그냥 정수 하나입니다. 첫 번째 노드의 포인터는 $A[0]$에 저장되어 있습니다. 다시 말해, $A[0]$의 값은 두 번째 노드의 위치를 가리킨다고 할 수 있습니다. 두 번째 노드의 포인터는 $A[A[0]]$에 저장되어 있고, 세 번째 노드의 포인터는 $A[A[A[0]]]$에 저장되어 있고, 이러한 것이 반복됩니다. 만약 포인터의 값이 $-1$이라면, 이 노드가 연결 리스트의 마지막 노드임을 알 수 있습니다. 

위의 예제에서, $A[0]$의 값은 2이고, 따라서 두 번째 노드의 포인터는 $A[2]$에 저장되어 있습니다. $A[2]$의 값은 4이고 따라서 세 번째 노드의 포인터는 $A[4]$에 저장되어 있습니다. $A[4]$의 값은 $-1$이므로, 더 이상 연결 리스트에 붙은 노드는 없습니다. 이 과정은 아래와 같이 나타낼 수 있고 이를 통해 연결 리스트에는 노드가 3개 있다는 것도 알 수 있습니다.

\\[A[0]=2 \rightarrow A[2]=4 \rightarrow A[4]=-1 \\] 

그런데 갑자기 승현이가 나타나 배열의 한 원소를 새로운 값으로 바꾸더니 달아나 버렸습니다! (바꾸지 않았을 수도 있습니다.) 너무 순식간에 일어난 일이라 놀란 지학이는 승현이가 바꿔 놓은 원소가 어디인지도, 어떤 값으로 바꾸었는지도 기억하지 못했습니다.

이에 과학 수사대의 에이스인 석환이는 지학이의 부탁을 받고 배열을 원래대로 복구하기로 했습니다. 그러나 지학이와 상담을 하던 석환이는 원래대로 복구할 수는 없다고 판단했고, 지학이가 실망하지 않도록 하기 위해 배열의 한 원소를 새로운 값으로 바꾸었을 때 (바꾸지 않을 수도 있습니다), 그 배열에 저장된 포인터들로 만든 연결 리스트의 노드 수가 가장 많아지는 경우를 찾기로 했습니다. 맨 위 그림에 있는 배열을 고려해 봅시다.

* $A[4]$의 값을 6으로 바꾸면 연결 리스트의 노드 수는 4개가 됩니다.
* $A[0]$의 값을 7으로 바꾸면 연결 리스트의 노드 수는 4개가 됩니다.
* $A[0]$의 값을 9로 바꾸면 사이클이 생겨 연결 리스트가 유효하지 않습니다.
* $A[2]$의 값을 7으로 바꾸면 연결 리스트의 노드 수는 5개가 됩니다.

위 그림에서 한 원소를 다른 어떤 값으로 바꾸더라도 연결 리스트의 노드 수는 최대 5개까지만 가능합니다. 따라서 석환이는 "$A[2]$의 값이 원래는 7이었다"고 지학이에게 알려주었고 지학이는 행복해했다고 합니다.

안타깝게도 그 이후에도 승현이는 다른 배열을 가지고 놀고 있는 지학이를 위와 같은 방식으로 괴롭혔고, 지친 석환이는 이러한 일을 대신 해주는 프로그램을 작성하기로 했습니다. 승현이가 한 원소의 값을 바꿔 놓은 배열이 주어졌을 때, 원소 하나를 적절히 바꾸었을 때 만들 수 있는 연결 리스트의 최대 노드 수를 출력하세요.


### 입력 형식

입력은 두 줄로 주어집니다. 첫 번째 줄에 배열의 크기 $N$이 주어집니다. 두 번째 줄에 배열의 $N$개 원소들이 $A[0]$부터 시작해서 차례대로 주어집니다. 각 원소는 정수이며 $-1$ 이상 $N$ 이하입니다.

### 출력 형식

복구 가능한 연결 리스트들 중 가장 긴 것의 길이를 출력합니다.

### 서브태스크

1. (5점) $1 < N \le 20.$
2. (5점) $20 < N \le 3000.$ 복구된 연결리스트의 길이가 100을 넘지 않습니다.
3. (5점) $20 < N \le 3000.$ 위의 조건들과 다르게, 복구된 연결리스트의 길이가 100보다 길 수도 있습니다.
4. (10점) $3000 < N \le 20000.$

### 예제

특별한 케이스가 정말 많으니 조심하세요. 단 하나라도 놓지면 안 됩니다.

#### 예제 1

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">10<br/>
2 5 4 4 -1 1 -1 3 0 8</td>
   <td class="code-font">5</td>
  </tr>
 </tbody>
</table>

#### 예제 2

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">4<br/>
0 0 0 0</td>
   <td class="code-font">1</td>
  </tr>
 </tbody>
</table>

$A[0]$을 $-1$로 바꾸면 노드가 하나인 연결 리스트가 됩니다.

#### 예제 3

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">6<br/>
1 2 3 4 5 -1</td>
   <td class="code-font">6</td>
  </tr>
 </tbody>
</table>

그냥 안 바꾸면 됩니다.

#### 예제 4

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">10<br/>
2 5 4 4 0 1 -1 3 0 8</td>
   <td class="code-font">4</td>
  </tr>
 </tbody>
</table>

$A[4]$를 6으로 바꾸면 됩니다.

#### 예제 5

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">10<br/>
2 5 4 4 -1 1 -1 6 0 8</td>
   <td class="code-font">5</td>
  </tr>
 </tbody>
</table>

$A[4]$를 7로 바꾸면 됩니다.