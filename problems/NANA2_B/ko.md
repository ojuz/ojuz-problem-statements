나나는 오늘도 우주선을 탔습니다. 우주선을 상시로 이용하는 나나는 항공사 마일리지를 많이 쌓아, 드디어 1등석을 끊었습니다! 나나는 좋아하는 땅콩도 먹으면서 즐거운 시간을 보냈습니다.

하지만 그것도 잠시, 곧 지루해졌습니다. 목적지는 아주 멀기 때문에, 나나는 '역사상 개봉된 모든 영화를 보겠다는 원대한 계획을 세웠습니다. 물론 우주선이 이동하는 동안에도 개봉된 영화가 지구에서부터 계속 전송되기 때문에, 상당히 도전적인 과제가 될 것이라고 생각했습니다.

우주선에는 확실히 검증된 시스템만이 들어와야 한다는 규칙 때문에, 우주선의 엔터테인먼트 시스템은 상당히 복잡합니다. 모든 영화에는 0으로도 시작할 수 있는 <span class="tex-span"><i>D</i></span>자리의 정수 번호가 부여되어 있습니다. 특정 영화를 보려면, 리모콘을 이용하여 시스템에 영화 번호를 입력해야 합니다. 그 방법은 아래와 같습니다.

1. 처음에 화면에 <span class="tex-span"><i>D</i></span>자리의 수가 보여지고, 가장 왼쪽의 숫자에 커서가 위치해 있습니다. 처음에 모든 숫자는 0입니다.
2. 리모콘에는 '위', '아래', '왼쪽', '오른쪽', '선택'의 다섯 가지 버튼밖에 없습니다.
 - '왼쪽' 버튼을 누르면 커서가 왼쪽으로 한 칸 이동하고, '오른쪽' 버튼을 누르면 커서가 오른쪽으로 한 칸 이동합니다. 단, 가장 왼쪽 칸과 가장 오른쪽 칸은 서로 연결되어 있어서, 예를 들어서 가장 왼쪽 칸에서 '왼쪽' 버튼을 누르면 가장 오른쪽 칸으로 이동합니다.
 - '위' 버튼을 누르면 커서가 위치한 자리의 숫자가 1 커지고, '아래' 버튼을 누르면 커서가 위치한 자리의 숫자가 1 작아집니다. 0과 9는 서로 연결되어 있어서, 9에서 '위' 버튼을 누르면 0이 되고, 0에서 '아래' 버튼을 누르면 9가 됩니다. 이 두 버튼은 커서가 위치한 자리에만 영향을 미칩니다.
 - 아무 때나 '선택' 버튼을 눌러서 영화 관람을 시작할 수 있습니다. 모든 <span class="tex-span"><i>D</i></span>자리의 영화 번호에는 해당하는 영화가 존재하며, 영화가 끝나면 다시 1.의 상태로 돌아갑니다.

원대한 계획에도 불구하고 영화를 몇 편 본 뒤 나나는 지루해졌습니다. 버튼을 누르는 것도 지루해진 나머지, 나나는 '선택하기 위해 눌러야 하는 버튼의 수'를 기준으로 영화를 분류해보기로 했습니다. 이를 위해서는, 우선 특정한 영화를 선택하기 위해서 필요한 버튼을 눌러야 하는 횟수의 최솟값을 알아야 합니다.

주어진 영화에 대해서, 최소 버튼 클릭 횟수는 몇 번일까요?

### 입력 형식

첫 번째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;100</span>)가 주어집니다.

각 테스트 케이스는 0, 1, 2, 3, 4, 5, 6, 7, 8, 9로만 이루어진 <span class="tex-span"><i>D</i></span>자리의 문자열 <span class="tex-span"><i>S</i></span>와 반복 횟수 <span class="tex-span"><i>P</i></span>로 구성됩니다. 실제 영화 번호는 문자열 <span class="tex-span"><i>S</i></span>가 <span class="tex-span"><i>P</i></span>회 반복된 형태입니다. 입력에서 <span class="tex-span"><i>D</i></span>는 주어지지 않습니다.

### 출력 형식

각 줄에 주어진 영화 번호를 선택하기 위한 최소 버튼 클릭 횟수를 출력하세요.

### 입력 파일 정보

<div class="row">
<div class="col-sm-12 col-md-10 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-3 col-md-3 col-lg-3">입력 파일명</th>
  <th class="col-sm-3 col-md-3 col-lg-3">출력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">점수</th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>D</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>P</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>B1.in</samp></td>
  <td><samp>B1.out</samp></td>
  <td>20</td>
  <td><span class="tex-span">&le; 10</span></td>
  <td><span class="tex-span">= 1</span></td>
 </tr>
 <tr>
  <td><samp>B2.in</samp></td>
  <td><samp>B2.out</samp></td>
  <td>45</td>
  <td><span class="tex-span">&le; 1000</span></td>
  <td><span class="tex-span">&le; 1000</span></td>
 </tr>
 <tr>
  <td><samp>B3.in</samp></td>
  <td><samp>B3.out</samp></td>
  <td>35</td>
  <td><span class="tex-span">&le; 1000</span></td>
  <td><span class="tex-span">&le; 10<sup class="upper-index">9</sup></span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 답안 생성 및 제출 방법

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_B/b_input.zip)에서 입력 파일을 내려받아서, 위 표에 따라 출력 파일을 만듭니다. 제출하는 방법은 두 가지가 있습니다.

* 모든 출력 파일을 하나의 zip 파일에 압축하여 제출합니다. 다른 폴더 안에 출력 파일을 넣고 압축하는 등의 행위를 할 시 업로드 공격으로 의심되어 업로드가 즉시 차단됩니다.
* 각 출력 파일을 하나씩 업로드하여 제출합니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>3<br>12345 1<br>460005 1<br>1 100</samp></td><td><samp>20<br>17<br>200</samp></td></tr></tbody>
</table>