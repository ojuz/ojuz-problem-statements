<style type="text/css">
.tex-span {
    font-size: 125%;
    font-family: times new roman;
}
.tex-formula {
    vertical-align: middle;
    margin: 0;
    border:medium none;
    position: relative;
    bottom: 2px;
}
</style>

당신이 꿈을 이루는 과정 중에 일어날 수 있는 수많은 상황들의 관계를 그래프로 나타내어 보겠다. 많은 상황을 압축해서 <span class="tex-span"><i>N</i></span>개의 상황이 일어날 수 있다고 하고 1번에서 <span class="tex-span"><i>N</i></span>까지의 번호를 붙였다. 당신은 현재 1번 상황에 있다. 그리고 <span class="tex-span"><i>N</i></span>번 상황은 당신이 이루고자 하는 유일한 꿈이다.

상황은 당신의 선택에 따라 변화할 수 있다. 당신이 선택할 수 있는 변화는 총 <span class="tex-span"><i>M</i></span>개 있으며 <span class="tex-span"><i>x, y</i></span>의 형태로 주어진다. 이는 당신이 상태 <span class="tex-span"><i>x</i></span>에 있는 경우 상태 <span class="tex-span"><i>y</i></span>로 가는 선택을 할 수 있다는 것을 의미하며, <span class="tex-span"><i>x</i>&thinsp;&lt;&thinsp;<i>y</i></span>임이 보장된다.

당신은 꿈을 이룰 수 있을까? 이룰 수 있다면 당신의 상황이 변화하는 횟수를 최소한으로 줄이면 몇 번 만에 꿈을 이룰 수 있을까?

### 입력 형식

첫 번째 줄에는 두 개의 자연수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span>(<span class="tex-span">0&thinsp;&le;&thinsp;<i>M</i>&thinsp;&le;&thinsp;200,000</span>)이 주어진다.

이후 <span class="tex-span"><i>M</i></span>개의 줄에는 두 개의 자연수 <span class="tex-span"><i>x</i></span>, <span class="tex-span"><i>y</i></span>(<span class="tex-span">1&thinsp;&le;&thinsp;<i>x</i>&thinsp;&lt;&thinsp;<i>y</i>&thinsp;&le;&thinsp;<i>N</i></span>)가 공백으로 구분되어 주어진다

쉬운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100</span>인 입력이 주어진다.

어려운 문제에서는 <span class="tex-span">1&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100,000</span>인 입력이 주어진다.

### 출력 형식

당신이 꿈을 이룰 수 있다면 꿈을 이루기 위해 필요한 상황 변화 수의 최솟값을 출력하고, 이룰 수 없다면 -1을 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">4 4<br>
1 2<br>
2 3<br>
3 4<br>
2 4</td>
   <td class="code-font">2</td>
  </tr>
 </tbody>
</table>

<img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_Y/arrow.png"/>로 상황을 바꾸면 두 번 상황이 바뀐 후 꿈을 이루게 된다.