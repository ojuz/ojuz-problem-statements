[참고] 영화 선택 - Easy 문제를 먼저 읽고 오세요! 이 문제에서 명시되지 않은 조건들은 Easy 문제에 명시되어 있습니다.

나나는 영화를 선택하기 위해서 필요한 최소한의 버튼을 눌러야 하는 횟수를 알게 되어서 참 만족스러웠습니다. 그것도 잠시, 나나는 다시 지루해졌고 새로운 놀이를 찾기 시작했습니다. 자리를 둘러보니, 나나는 1등석에는 리모콘 고장에 대비해 여러 종류의 리모콘을 비치해 두었다는 것을 알게 되었습니다. 나나는 원래 리모콘을 포함해, 다음과 같은 세 종류 리모콘을 발견했습니다.

1. '오른쪽', '위', '선택' 만 있는 리모콘
2. '오른쪽', '위', '아래', '선택' 만 있는 리모콘
3. 원래의 '오른쪽', '왼쪽', '위', '아래', '선택' 이 있는 리모콘

각 버튼의 역할은 원래 리모콘과 같습니다. 세 종류의 리모콘을 가지고 놀던 나나는 각 리모콘이 할 수 있는 일의 차이에 대해서 생각하다가 다음과 같은 궁금증을 가지게 되었습니다.

각 리모콘에 대해, 최소 버튼 클릭 횟수가 <span class="tex-span"><i>K</i></span>번인 영화의 수는 얼마나 될까요?

### 입력 형식

첫 번째 줄에 테스트 케이스의 수 <span class="tex-span"><i>T</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>T</i>&thinsp;&le;&thinsp;1,000</span>) 

각 테스트 케이스는 영화의 번호 길이 <span class="tex-span"><i>D</i></span>와 최소 버튼 클릭 횟수 <span class="tex-span"><i>K</i></span>로 이루어집니다. 모든 테스트 케이스에 대해서 <span class="tex-span">1&thinsp;&le;&thinsp;<i>D</i>&thinsp;&le;&thinsp;100</span>, <span class="tex-span">0&thinsp;&le;&thinsp;<i>K</i>&thinsp;&le;&thinsp;10<i>D</i></span>를 만족합니다.

### 출력 형식

각 줄에 각각의 출력 파일에서 사용하는 리모콘에 대해 조건을 만족하는 영화의 수를 <span class="tex-span">10<sup>9</sup>+7</span>로 나눈 나머지를 출력하세요.

### 입력 파일 정보

이 문제에서 **모든 출력 파일은 같은 입력 파일을 토대로 만들어야 합니다.**

<div class="row">
<div class="col-sm-12 col-md-10 col-lg-8">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">입력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">출력 파일명</th>
  <th class="col-sm-1 col-md-1 col-lg-1">점수</th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>D</i></span></th>
  <th class="col-sm-1 col-md-1 col-lg-1"><span class="tex-span"><i>K</i></span></th>
  <th class="col-sm-1 col-md-1 col-lg-1">리모콘</th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>C.in</samp></td>
  <td><samp>C1.out</samp></td>
  <td>23</td>
  <td><span class="tex-span">&le; 100</span></td>
  <td><span class="tex-span">&le; 1000</span></td>
  <td><span class="tex-span">1번</span></td>
 </tr>
 <tr>
  <td><samp>C.in</samp></td>
  <td><samp>C2.out</samp></td>
  <td>13</td>
  <td><span class="tex-span">&le; 100</span></td>
  <td><span class="tex-span">&le; 1000</span></td>
  <td><span class="tex-span">2번</span></td>
 </tr>
 <tr>
  <td><samp>C.in</samp></td>
  <td><samp>C3.out</samp></td>
  <td>64</td>
  <td><span class="tex-span">&le; 100</span></td>
  <td><span class="tex-span">&le; 1000</span></td>
  <td><span class="tex-span">3번</span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 답안 생성 및 제출 방법

[여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_C/C.in)에서 입력 파일을 내려받아서, 위 표에 따라 출력 파일을 만듭니다. 제출하는 방법은 두 가지가 있습니다.

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
	
	<tr><td><samp>2<br>5 3<br>5 4</samp></td><td><samp>2<br>4</samp></td></tr>
	<tr><td><samp>2<br>5 3<br>5 4</samp></td><td><samp>4<br>10</samp></td></tr>
	<tr><td><samp>2<br>5 3<br>5 4</samp></td><td><samp>6<br>18</samp></td></tr>
    </tbody>
</table>