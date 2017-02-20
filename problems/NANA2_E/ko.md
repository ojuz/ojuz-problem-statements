2014년 12월 25일, 드디어 부족전쟁 1세계의 막이 내렸습니다. 그 장대한 서사시는 [대하소설로 써도](https://mirror.enha.kr/wiki/%EB%B6%80%EC%A1%B1%EC%A0%84%EC%9F%81%20%ED%95%9C%EA%B5%AD%EC%84%9C%EB%B2%84%201%EC%84%B8%EA%B3%84) 모자람이 없지만, 그것도 과거의 일, 최근에는 몇십 명 정도의 거대 유저들만이 남아 게임을 떠난 유저들의 마을들을 흡수해나갈 뿐이었습니다.

마지막 날 유저 <samp>NanaPanzer</samp>는 과거의 추억에 잠겨 자신의 오천여 개 마을들을 바라보다가, 다음과 같은 생각을 했습니다.

<blockquote>
'이 마을들을 모두 먹는 데에 참 시간이 오래 걸렸지. 수십명의 유저들이 격렬히 저항했고, 이 마을들을 모두 손에 넣기까지는 무려 7년이나 지났어. 이 마을들이 원래부터 주인이 없는 마을들이었다면 어땠을까?'
 <footer>유저 <samp>NanaPanzer</samp></footer>
</blockquote>

<samp>NanaPanzer</samp>는 시간이 훨씬 적게 걸렸을 것으로 생각은 했지만, 정확하게 얼마나 걸렸을지는 어림잡기도 힘들었습니다. 이제 부족을 잊고 쉬려고 하는 <samp>NanaPanzer</samp>를 위해서, 이 궁금증을 해결해줍시다.

### 필수 정보

마을은 총 <span class="tex-span"><i>n</i></span>개 있으며, 각 마을에는 1 이상 <span class="tex-span"><i>n</i></span> 이하의 자연수 번호가 붙어 있습니다. <span class="tex-span"><i>i</i></span>번 마을은 2차원 평면 위의 점 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>)</span>로 나타낼 수 있습니다. 한 점에는 많아야 한 마을만 있을 수 있습니다. 1번 마을은 "시작 마을"이라고 불리는데, 게임을 처음 시작할 때 자신이 소유하고 있는 유일한 마을입니다.

시작 마을에서는 5시간에 1번씩 귀족이 생산됩니다. 생산된 귀족은 자신의 소유가 아닌 임의의 마을로 가서, 그 마을의 영주로 군림하여, 자신의 소유로 만들 수 있습니다. 이렇게 해서 소유하게 된 마을들에서도 5시간에 1번씩 귀족이 생산됩니다. 만약 생산된 귀족이 다른 마을로 떠나지 않는다면, 이 귀족은 자동으로 사라지고, 이 귀족을 생산한 마을에서는 더 이상 귀족이 생산되지 않습니다.

어떤 귀족이 마을 <span class="tex-span"><i>A</i></span>에서 마을 <span class="tex-span"><i>B</i></span>로 가는 데 걸리는 시간은 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_E/cfb12686d2cb09a82de9e0943c714cb2ba8ee6e9.png"/>분입니다.

### 해야 할 일

<samp>NanaPanzer</samp>가 모든 마을을 자신의 소유로 만드는 데에 걸리는 시간을 최소화해주세요. 이를 위해 여러분은 귀족들이 어느 마을로 이동할지를 결정해야 합니다.

### 입력 형식

첫 번째 줄에는 마을의 수 <span class="tex-span"><i>n</i></span>이 주어집니다.

이후 <span class="tex-span"><i>n</i></span>개 줄이 주어지는데, 이 중 <span class="tex-span"><i>i</i></span>번째 줄 (<span class="tex-span">1 &le; <i>i</i> &le; <i>n</i></span>)에는 두 개의 정수 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>와 <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i></sub></span>가 공백을 사이로 두고 주어집니다. 이것은 <span class="tex-span">(<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;<i>Y</i><sub class="lower-index"><i>i</i></sub>)</span>가 <span class="tex-span"><i>i</i></span>번 마을의 좌표임을 의미합니다.

위에서 언급했듯이, 입력으로 주어진 1번 마을이 시작 마을이며, 좌표가 겹치는 마을은 없습니다.

### 출력 형식

총 <span class="tex-span"><i>n</i></span>줄을 출력합니다. <span class="tex-span"><i>i</i></span>번째 줄 (<span class="tex-span">1 &le; <i>i</i> &le; <i>n</i></span>)에는 처음에 <span class="tex-span"><i>i</i></span>번 마을에서 생산된 귀족의 수를 출력하고, 그 다음부터 시간 순서대로 귀족이 어느 마을로 떠났는지를 공백을 사이로 두고 출력합니다.

### 파일 정보

각 입력 파일은 모두 부족전쟁 1세계의 실제 유저 데이터이며, 각 데이터의 유저 아이디와 <span class="tex-span"><i>n</i></span>, 기준시간의 값은 다음과 같습니다. 입력 파일은 [여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_E/e_input.zip)에서 내려받을 수 있습니다.

<div class="row">
<div class="col-sm-12 col-md-8 col-lg-6">
<div class='table-responsive'>
<table class='table table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">입력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">출력 파일명</th>
  <th class="col-sm-2 col-md-2 col-lg-2">유저 아이디</th>
  <th class="col-sm-2 col-md-2 col-lg-2"><span class="tex-span"><i>n</i></span></th>
  <th class="col-sm-2 col-md-2 col-lg-2">기준 시간 <span class="tex-span"><i>S</i></span></th>
 </tr>
</thead>
<tbody>
 <tr>
  <td><samp>E1.in</samp></td>
  <td><samp>E1.out</samp></td>
  <td>일루일루이</td>
  <td><span class="tex-span">305</span></td>
  <td><span class="tex-span">8,100</span></td>
 </tr>
 <tr>
  <td><samp>E2.in</samp></td>
  <td><samp>E2.out</samp></td>
  <td>바람</td>
  <td><span class="tex-span">2,675</span></td>
  <td><span class="tex-span">10,700</span></td>
 </tr>
 <tr>
  <td><samp>E3.in</samp></td>
  <td><samp>E3.out</samp></td>
  <td>bismark77</td>
  <td><span class="tex-span">2,919</span></td>
  <td><span class="tex-span">12,200</span></td>
 </tr>
 <tr>
  <td><samp>E4.in</samp></td>
  <td><samp>E4.out</samp></td>
  <td>NanaPanzer</td>
  <td><span class="tex-span">5,269</span></td>
  <td><span class="tex-span">15,700</span></td>
 </tr>
 <tr>
  <td><samp>E5.in</samp></td>
  <td><samp>E5.out</samp></td>
  <td>이동꾸옹</td>
  <td><span class="tex-span">11,022</span></td>
  <td><span class="tex-span">16,800</span></td>
 </tr>
</tbody>
</table>
</div>
</div>
</div>

### 채점 방식

각 출력 파일에 대한 여러분의 점수는 아래와 같이 계산됩니다.

* 만약 여러분의 계획이 문제에서 제시한 조건을 만족하지 않는다면 0점입니다.
* 만약 여러분의 계획이 문제에서 제시한 조건을 만족한다면, 다음과 같이 점수가 계산됩니다. 기준시간을 <span class="tex-span"><i>S</i></span>, 여러분이 모든 마을을 정복하는 데 들인 시간을 <span class="tex-span"><i>Y</i></span>로 둡시다.
 - <span class="tex-span"><i>S</i> &lt; <i>Y</i></span>이면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_E/d9446cde57f8cd0118d24f3d537b54eabdb2185c.png"/>점. 
 - <span class="tex-span"><i>S</i> &ge; <i>Y</i></span>이면 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/NANA2_E/99f72a9b2f2910490c65a46f6b566147c84a7dae.png"/>점.
 
제출한 답안의 점수는 각 출력 파일에서 받은 점수들의 합이 됩니다.

### 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예시</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예시</th>
		</tr>
	</thead>
	<tbody>
	
	<tr><td><samp>4<br>0 0<br>0 10<br>10 0<br>10 10</samp></td><td><samp>3 4 2 3<br>0<br>0<br>0</samp></td></tr>
    </tbody>
</table>

총 걸리는 시간은 1250분입니다.