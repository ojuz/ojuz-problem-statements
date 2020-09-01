<h3>설명</h3>

<p>인도네시아에는 $N$ 개의 도시가 있고, $0$부터&nbsp;$N - 1$까지 번호가 매겨져 있다. 또 $M$ 개의 양방향 도로가 있는데, $0$ 부터 $M - 1$까지 번호가 매겨져 있다. 각 도로는 두 개의 서로 다른 도시를 연결한다. $i$ 번 도로는 $U[i]$ 번 도시와 $V[i]$ 번 도시를 연결하고, 자동차로 여행하려면 휘발유 $W[i]$ 만큼이 필요하다. 어떤 두 도시도 서로 오갈&nbsp;수 있도록 도로망이 구축되어 있다.</p>

<p>앞으로 $Q$ 일 동안, 매일매일 한 쌍의 도시가 자매 도시&nbsp;관계를 맺으려고 한다. 구체적으로는, $j$번째 날, $X[j]$ 번 도시는 $Y[j]$ 번 도시와 자매 도시 관계를 맺으려고 한다. 이러려면,&nbsp;$X[j]$ 번 도시는 대표단을 자동차를 이용해서 $Y[j]$ 번 도시로 보낸다. 비슷하게, $Y[j]$ 번 도시도 대표단을 자동차를 이용해서 $X[j]$ 번 도시로 보낸다.&nbsp;&nbsp;</p>

<p>혼잡을 막기 위해서, 두 자동차는 어느 순간에도 만나면 안된다. 보다 구체적으로는, 두 자동차가 동시에 같은 도시에 있으면 안된다. 또, 같은 도로를 동시에 서로 반대 방향으로 여행해도 안된다. 추가로, 어떤 도로를 여행하는 자동차는 이 도로를 끝까지 가서 목적지에 도착해야 한다. (다른 말로 하면, 도로 중간에서 유턴할 수 없다.) 그렇지만, 자동차는 같은 도시 또는 같은 도로를 한 번 이상 방문할 수 있다. 또, 자동차는 언제든지 어떤 도시에서든지&nbsp;대기할 수 있다.&nbsp;&nbsp;&nbsp;</p>

<p>연료 탱크가 큰 자동차는&nbsp;비싸기 때문에, 두 도시는 사용할 두 자동차의 연료 탱크의 최대 용량을 최소화하는 경로를 택하고 싶다. 각각의 도시에는 무한히 많은 휘발유가 있는 주유소가 있기 때문에, 자동차가 필요한&nbsp;연료 탱크의 최대 용량은 자동차가 이용할 모든 도로에서 <strong>최대</strong>로 필요한 휘발유의 양이다.&nbsp;&nbsp;</p>

<h3>할 일&nbsp;</h3>

<p>다음&nbsp;<code>init</code>와 <code>getMinimumFuelCapacity</code> 함수를 구현해야 한다.&nbsp;&nbsp;</p>

<ul>
	<li><code>init(N, M, U, V, W)</code> - 이 함수는&nbsp; <code>getMinimumFuelCapacity&nbsp;</code>함수를 호출하기 전에 정확히 한 번 호출된다.&nbsp;&nbsp;

	<ul>
		<li>$N$: 도시의 수를 나타내는 정수.</li>
		<li>$M$: 도로의 수를 나타내는 정수.&nbsp;&nbsp;</li>
		<li>$U$: 길이 $M$인 정수의 배열로 도로의 한 쪽 끝을 나타낸다.&nbsp;</li>
		<li>$V$: 길이 $M$인 정수의 배열로 도로의 다른&nbsp;쪽 끝을 나타낸다.&nbsp;</li>
		<li>$W$: 길이 $M$인 정수의 배열로 각 도로를 여행하는데 필요한 휘발유의 양을 나타낸다.</li>
	</ul>
	</li>
	<li><code>getMinimumFuelCapacity(X, Y)</code> - 이 함수는 그레이더가 정확히&nbsp;$Q$ 번 호출한다.&nbsp;&nbsp;
	<ul>
		<li>$X$: 첫번째 도시를 나타내는 정수.&nbsp;&nbsp;</li>
		<li>$Y$: 두번째 도시를 나타내는 정수.</li>
		<li>이 함수는 $X$번 도시의 대표단이 $Y$번 도시로, $Y$번 도시의 대표단이 $X$번 도시로 위에서 설명한 규칙을 따라 여행할 때 두 자동차가 필요한&nbsp;연료 탱크의 최대 용량의 최소값을 리턴한다.&nbsp;&nbsp;만약 규칙을 따라 여행하는 것이 불가능하다면, $-1$을 리턴한다.&nbsp;&nbsp;</li>
	</ul>
	</li>
</ul>

<h3>예제&nbsp;</h3>

<p>첫번째 예제에서, $N = 5$, $M = 6$, $U = [0, 0, 1, 1, 1, 2]$, $V = [1, 2, 2, 3, 4, 3]$, $W = [4, 4, 1, 2, 10, 3]$, $Q = 3$, $X = [1, 2, 0]$, $Y = [2, 4, 1]$이다. 이 예제는 다음 그림과 같다.&nbsp;&nbsp;</p>

<p><img src="https://sandalphon.tlx.toki.id/api/v2/problems/JIDPROGALYDeYjYtWab63mKaZi9/render/swap1.png" style="width:250px" /></p>

<p>그레이더는 처음에&nbsp;<code>init(5, 6, [0, 0, 1, 1, 1, 2], [1, 2, 2, 3, 4, 3], [4, 4, 1, 2, 10, 3])</code>를 호출한다. 그 후, 그레이더는 다음 일들을 한다.&nbsp;</p>

<ul>
	<li><code>getMinimumFuelCapacity(1, 2)</code>. 먼저, 1번 도시에서 출발한 자동차는 3번 도시로 이동한다. 다음, 2번 도시에서 출발한 자동차는 1번 도시로 이동하고, 3번 도시에 있던 자동차는 2번 도시로 이동한다. 따라서 두 자동차가 필요한 연료 용량의 최대값은 $3$이다.&nbsp;(3번 도시에서 2번 도시로 이동하는데 필요) 이보다 적은 연료 용량으로 갈 수 있는 경로가 없기 때문에, 이 함수의 리턴값은 $3$이어야 한다.</li>
	<li><code>getMinimumFuelCapacity(2, 4)</code>. 4번 도시에서 오거나 4번 도시로 가는 자동차는 연료가 $10$만큼 필요하기 때문에, 이 함수의 리턴값은 $10$이어야 한다.</li>
	<li><code>getMinimumFuelCapacity(0, 1)</code>. 이 함수는 $4$를 리턴해야 한다.</li>
</ul>

<p>&nbsp;</p>

<p>두번째 예제에서는,&nbsp; $N = 3$, $M = 2$, $U = [0, 0]$, $V = [1, 2]$, $W = [5, 5]$, $Q = 1$, $X = [1]$, $Y = [2]$이다. 이 예제는 다음 그림과 같다.&nbsp; &nbsp;&nbsp;</p>

<p><img src="https://sandalphon.tlx.toki.id/api/v2/problems/JIDPROGALYDeYjYtWab63mKaZi9/render/swap2.png" style="width:150px" /></p>

<p>그레이더는 처음에 <code>init(3, 2, [0, 0], [1, 2], [5, 5])</code>를 호출한다. 그 후, 그레이더는 다음 일을 한다.&nbsp;&nbsp;</p>

<ul>
	<li><code>getMinimumFuelCapacity(1, 2)</code>. 자동차가 1번 도시에서 2번 도시로 이동하는 과정에서 다른 자동차를 만나지 않는 것은 불가능하기 때문에, 이 함수는&nbsp;$-1$을 리턴해야 한다.</li>
</ul>

<p>&nbsp;</p>

<h3>제약조건</h3>

<ul>
	<li>$2 \le N \le 100\,000$.</li>
	<li>$N - 1 \le M \le 200\,000$.</li>
	<li>$0 \le U[i] \lt V[i] \lt N$.</li>
	<li>두 도시를 잇는 도로는 최대 1개이다.&nbsp;&nbsp;</li>
	<li>어떤 두 도시도 하나 또는 둘 이상의 도로를 이용하여 오갈 수 있다.&nbsp;&nbsp;</li>
	<li>$1 \le W[i] \le 10^9$.</li>
	<li>$1 \le Q \le 200\,000$.</li>
	<li>$0 \le X[j] \lt Y[j] \lt N$.</li>
</ul>

<h4>Subtask 1 (6 points)</h4>

<ul>
	<li>각 도시는 최대 2개의 도로의 끝점이다.&nbsp;&nbsp;</li>
</ul>

<h4>Subtask 2 (7 points)</h4>

<ul>
	<li>$M = N - 1$.</li>
	<li>$U[i] = 0$.</li>
</ul>

<h4>Subtask 3 (17 points)</h4>

<ul>
	<li>$Q \le 5$.</li>
	<li>$N \le 1\,000$.</li>
	<li>$M \le 2\,000$.</li>
</ul>

<h4>Subtask 4 (20 points)</h4>

<ul>
	<li>$Q \le 5$.</li>
</ul>

<h4>Subtask 5 (23 points)</h4>

<ul>
	<li>$M = N - 1$.</li>
</ul>

<h4>Subtask 6 (27 points)</h4>

<ul>
	<li>추가적인 제약 조건이 없다.&nbsp;</li>
</ul>

<p>&nbsp;</p>

<h3>샘플 그레이더</h3>

<p>샘플 그레이더는 입력을 다음 양식으로 읽는다.&nbsp;&nbsp;</p>

<pre>
N M
U[0] V[0] W[0]
U[1] V[1] W[1]
.
.
.
U[M-1] V[M-1] W[M-1]
Q
X[0] Y[0]
X[1] Y[1]
.
.
.
X[Q-1] Y[Q-1]
</pre>

<p>샘플 그레이더는 <code>getMinimumFuelCapacity</code> 함수를 호출할 때마다, 이 함수의 리턴값을 출력한다.&nbsp;&nbsp;</p>

<h3>첨부</h3>

<p>공개된 그레이더, 예제 케이스, 문제에 대한 기본 파일은 `swap.zip`에서 받을 수 있다.&nbsp;</p>