이제 조금 더 어려운 문제를 해결해 보자. 당신은 지금 <span class="tex-span"><i>P</i></span>면체 주사위를 굴리고 있다. 각 면에는 <span class="tex-span">1</span> 이상 <span class="tex-span"><i>P</i></span> 이하의 자연수가 하나씩 적혀 있으며, 주사위를 굴렸을 때 각 면이 나올 확률은 모든 면에 대해 동일하다. 이제 다음과 같은 놀이를 할 것이다.

* 처음에는 <span class="tex-span"><i>K</i></span>라는 수를 가지고 있다.
* 가지고 있는 수가 <span class="tex-span">0</span>이거나 <span class="tex-span"><i>N</i></span>이면 놀이를 끝낸다. 놀이가 끝나지 않았다면 주사위를 굴린다. 만약에 <span class="tex-span"><i>Q</i></span> 이하인 수가 나오면 현재 가지고 있는 수에서 1을 빼주고, 아니라면(즉 <span class="tex-span"><i>Q</i></span> 초과의 수가 나오면) 1을 더해준다. 이를 계속 반복한다.

놀이가 끝났을 때 가지고 있는 수가 <span class="tex-span"><i>N</i></span>일 확률을 구하는 프로그램을 작성하라.

### 입력

첫 번째 줄에는 정수 <span class="tex-span"><i>P</i></span>(<span class="tex-span">1&thinsp;&leq;&thinsp;<i>P</i>&thinsp;&leq;&thinsp;100</span>)가 주어진다.

두 번째 줄에는 정수 <span class="tex-span"><i>Q</i></span>(<span class="tex-span">0&thinsp;&leq;&thinsp;<i>Q</i>&thinsp;&leq;&thinsp;<i>P</i></span>)가 주어진다.

세 번째 줄에는 정수 <span class="tex-span"><i>N</i></span>(<span class="tex-span">1&thinsp;&leq;&thinsp;<i>N</i>&thinsp;&leq;&thinsp;100</span>)이 주어진다.

네 번째 줄에는 정수 <span class="tex-span"><i>K</i></span>(<span class="tex-span">0&thinsp;&leq;&thinsp;<i>K</i>&thinsp;&leq;&thinsp;<i>N</i></span>)가 주어진다.

### 출력

놀이가 끝났을 때의 숫자가 <span class="tex-span"><i>N</i>&thinsp;</span>일 확률을 출력한다. 정확한 판별을 위해, 답을 기약분수로 나타내었을 때 <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/fbeee0515b7b42d69c1c46762557590d4b94269c.png">가 된다면, <IMG align="middle" class="tex-formula" src="https://attach.oj.uz/contest/kriii4/ab064a1354823102a9c2a5fb867f6f09c72a1a22.png">을 대신 출력하도록 한다. <span class="tex-span"><i>b</i><sup class="upper-index">-1</sup></span>은 <span class="tex-span"><i>b</i></span>의 모듈러 곱셈에 대한 역원이다. 이 문제에서는 가능한 모든 입력에 대해 답이 존재한다.

### 입출력 예제

<table class="table table-condensed table-bordered " id="examples_table">
	<thead>
		<tr>
			<th class="col-lg-6 col-md-6 col-sm-6">입력 예제</th>
			<th class="col-lg-6 col-md-6 col-sm-6">출력 예제</th>
		</tr>
	</thead>
	<tbody>
		<tr><td><samp>3<br>2<br>5<br>3</samp></td><td><samp>903225813</samp></td></tr>
    </tbody>
</table>