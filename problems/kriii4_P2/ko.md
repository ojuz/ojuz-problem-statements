실제로 존재하는지 아닌지는 차치하고, 당신에게 삼면체 주사위가 있어서 이 주사위를 굴린다고 생각해보자. 주사위를 굴렸을 때 각 면이 나올 확률은 모두 동일하게 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/64c94d13eeb330b494061e86538db66574ad0f7d.png">이다. 한 면에는 1, 다른 한 면에는 2, 남은 한 면에는 4가 적혀있다고 하면 주사위를 굴렸을 때 나오게 되는 숫자의 기댓값은 과연 몇일까? 간단하게도 셋의 평균인 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/660cdaf99ccb60ee655c3bb2814a1885ba596465.png">이 될 것이다. 

이 문제를 조금 확장해서, "<span class="tex-span"><i>N</i></span>면체 주사위의 각 면에 적힌 수가 주어졌을 때, 주사위를 굴렸을 때 각 면이 나올 확률이 모두 같다면 주사위를 굴렸을 때 나오게 되는 수의 기댓값은 과연 몇일까?"라는 문제가 주어졌다고 하자. 위의 예시에 대한 답을 소수로 출력한다면 <span class="tex-span">2.33333333...</span>일텐데, 무한한 자릿수를 모두 출력할 수는 없으니 적당히 끊어서 출력할 것이고, 이 끊긴 소수를 채점 프로그램이 다시 입력받아서 정답과 비교한다고 하면 결과가 얼마나 부정확할 것인가? 그렇기에 답을 정확히 판별하기 위해 출력하고자 하는 분수를 [기약분수](https://ko.wikipedia.org/wiki/%EA%B8%B0%EC%95%BD%EB%B6%84%EC%88%98)로 만들어 분모와 분자를 직접 출력하도록 했던 시기가 있었다.

이제 문제를 조금 더 확장하여, <span class="tex-span"><i>M</i></span>개의 주사위가 있어서 이 중 <span class="tex-span"><i>i</i></span>번째 주사위가 <span class="tex-span"><i>N</i><sub class="lower-index"><i>i</i></sub></span>면체 주사위이고 모든 면에 적힌 수를 더한 값이 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>일 때, 각 주사위에 대해서 주사위를 던졌을 때 주사위의 각 면이 나올 확률이 동일하다고 가정한 상태에서 모든 주사위를 각각 한 번씩 던졌을 때 나온 수들의 합의 기댓값을 구하는 문제를 만들었다. 확률변수 <span class="tex-span"><i>X</i></span>의 기댓값을 <span class="tex-span">E(<i>X</i>)</span>로 나타내면, [기댓값의 선형성](https://en.wikipedia.org/wiki/Expected_value#Linearity)에 의해서 두 확률변수 <span class="tex-span"><i>X</i>, <i>Y</i></span>에 대해 <span class="tex-span">E(<i>X</i> + <i>Y</i>) = E(<i>X</i>) + E(<i>Y</i>)</span>가 성립하므로, 이 문제의 답을 아래와 같이 간단하게 나타낼 수 있다.

<p style="text-align:center;"><img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/6c78b78822aa5b83b671c872eec2fe7d5742b60d.png" style="text-align:center;"/></p>

즉, 각 주사위에서 나오게 되는 수의 기댓값을 모두 더하면 답이 되는 것이다. 이 답을 정확하게 출력하기 위해, 모든 분수(여기서는 각 주사위의 기댓값)를 통분한다고 생각해보자. 이 분수의 분모와 분자의 값이 어떤 범위까지 치솟게 될 것인가? 즉, 분모와 분자를 모두 저장하고 있게 되면, 두 분수의 합을 구할 때 분모와 분자를 적정한 범위 내에서 계산해낼 수 없다는 문제에 부딪히게 된다. "그렇다면 분모와 분자를 어떤 모듈러 상에서 가지고 있으면 되지 않을까?"라고 생각할 수 있지만, 그러면 분모와 분자를 약분할 수가 없게 된다. 그렇기에, 분수를 다음과 같이 모듈러 상에서 하나의 정수로 가지고 있는 방법을 채택하게 되었다.

* 어떤 분수가 기약분수로 나타냈을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">이면, 이 분수는 <span class="tex-span"><i>a</i>&thinsp;&times;&thinsp;<i>b</i><sup class="upper-index">-1</sup>&thinsp;mod&thinsp;<i>X</i></span> (<span class="tex-span"><i>X</i></span>는 소수)으로 대신 계산하도록 한다. 여기서 <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 *모듈러 곱셈에 대한 역원*이다.

<span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원 <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 대체 어떤 수인 것일까? 이 수는 다음과 같은 성질을 만족하는 정수이다.

<center><span class="tex-span"><i>b</i><sup class="upper-index">-1</sup> &times; <i>b</i> &equiv; 1(mod <i>X</i>)</span></center>

소수 모듈러에서만 성립하는 페르마의 소정리에 의해 <span class="tex-span"><i>b</i><sup class="upper-index"><i>X</i>&thinsp;-&thinsp;1</sup> &equiv; 1 (mod <i>X</i>)</span>가 성립하기에, <span class="tex-span"><i>b</i><sup class="upper-index"><i>X</i>&thinsp;-&thinsp;2</sup> &equiv; <i>b</i><sup class="upper-index">-1</sup> (mod <i>X</i>)</span> 역시 성립함을 알 수 있다.

이해를 돕기 위해 <span class="tex-span"><i>X</i></span>를 <span class="tex-span">11</span>로 두고 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/6a03da956b2cd4d640c294a25781960847db1a94.png"> 을 계산해보자. <span class="tex-span">3<sup class="upper-index">-1</sup> &equiv; 4 (mod 11)</span>이므로, <span class="tex-span"><i>Q</i> &equiv; 7 &times; 4 &equiv; 6 (mod 11)</span>이다. 이 <span class="tex-span"><i>Q</i></span>에 3을 곱한 다음 <span class="tex-span">11</span>로 나눈 나머지를 구해 보면 <span class="tex-span">7</span>이 나오므로, <span class="tex-span">6</span>이라는 정수가 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/660cdaf99ccb60ee655c3bb2814a1885ba596465.png">을 적절히 저장하고 있다는 것을 알 수 있다. 

분수(유리수)를 이와 같은 방식으로 나타낸다면, 두 분수의 덧셈, 뺄셈, 곱셈은 <span class="tex-span">mod <i>X</i></span>에서 두 정수를 가지고 계산하듯이 처리하고, 나눗셈은 나누는 분수의 곱셈에 대한 역원을 구한 후 그 역원을 <span class="tex-span">mod <i>X</i></span>에서 곱하는 것으로 처리한다면, 분수를 정확히 출력하기 위해 통분을 하거나 기약분수로 만드는 골치아픈 일을 할 필요가 없어진다!

그러나 이 방법에도 문제가 있는 것은 마찬가지이다. 앞의 예에서 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/660cdaf99ccb60ee655c3bb2814a1885ba596465.png">을 <span class="tex-span">6</span>으로 저장했지만, 그냥 <IMG align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii4_P2/85ff6a6e45c826914e5e5027bc871aec3311aabc.png">도 <span class="tex-span">6</span>으로 저장할 것이다. 즉 서로 다른 두 분수도 모듈러 상에서 같은 정수로 저장하여, 정확한 판별을 한다는 우리의 목적에 부합하지 않는 것이다. 또다른 문제로는, 분모가 소인수로 <span class="tex-span"><i>X</i></span>를 가질 때에는 역원을 계산할 수 없어서 모듈러로 나타낼 수가 없다는 점이 있다. 이러한 문제를 해결하기 위해 모듈러를 <span class="tex-span">1,000,000,007</span>와 같은 큰 소수로 하는데, 이를 통해 서로 다른 두 분수가 같은 정수로 나타나게 되는 확률을 낮추고, 분모가 가질 수 있는 소인수의 범위를 늘리는 효과를 볼 수 있다. 그는 이런 방식이 그래도 가장 정확한 방식이라고 생각하게 되었다.

이제 이 방식으로 <span class="tex-span"><i>M</i>&thinsp;</span>개의 주사위가 있고, <span class="tex-span"><i>i</i></span>번째 주사위가 <span class="tex-span"><i>N</i><sub class="lower-index"><i>i</i></sub></span>면체 주사위이며, 모든 면에 적힌 숫자를 더한 값이 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>일 때, 각 주사위에 대해서 주사위를 던졌을 때 주사위의 각 면이 나올 확률이 동일하다면, 모든 주사위를 한 번씩 던졌을 때 나온 숫자들의 합의 기댓값을 구하는 문제를 해결해보자.

### 입력

첫 번째 줄에는 주사위의 수를 나타내는 정수 <span class="tex-span"><i>M</i>(1&thinsp;&leq;&thinsp;<i>M</i>&thinsp;&leq;&thinsp;10<sup class="upper-index">4</sup>)</span>이 주어진다.

다음 <span class="tex-span"><i>M</i></span>개의 줄은 각 주사위의 정보를 나타내며, 이 중 <span class="tex-span"><i>i</i></span>(<span class="tex-span">1&thinsp;&leq;&thinsp;<i>i</i>&thinsp;&leq;&thinsp;<i>M</i></span>)번째 줄에는 <span class="tex-span"><i>N</i><sub class="lower-index"><i>i</i></sub>, <i>S</i><sub class="lower-index"><i>i</i></sub>(1&thinsp;&leq;&thinsp;<i>N</i><sub class="lower-index"><i>i</i></sub>, <i>S</i><sub class="lower-index"><i>i</i></sub>&thinsp;&leq;&thinsp;10<sup class="upper-index">9</sup>)</span>가 공백으로 구분되어 주어진다.

### 출력

모든 주사위를 한 번씩 던졌을 때 나온 숫자들의 합의 기댓값을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예제</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예제</th>
		</tr>
	</thead>
	<tbody>
		<tr><td><samp>1<br>3 7</samp></td><td><samp>333333338</samp></td></tr>
    </tbody>
</table>

모듈러가 <span class="tex-span">11</span>에서 <span class="tex-span">1,000,000,007</span>이 되어 답이 달라졌지만, 역시 <span class="tex-span">3</span>을 곱한 다음 <span class="tex-span">1,000,000,007</span>으로 나눈 나머지는 <span class="tex-span">7</span>이 된다.