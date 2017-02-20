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

<span class="tex-span"><i>N</i></span> 차원 좌표계에는 여러 개의 점들이 있다. 이들은 <span class="tex-span"><i>M</i></span> 개의 자연수 <span class="tex-span"><i>X</i><sub class="lower-index">1</sub>,&thinsp;...,&thinsp;<i>X</i><sub class="lower-index"><i>M</i></sub></span>를 이용해 나타낼 수 있는데, 각 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>가 나타내는 점들의 집합 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>는 아래와 같다.

<center>
<span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub>&thinsp;=&thinsp; {(<i>x</i><sub class="lower-index">1</sub>,&thinsp;<i>x</i><sub class="lower-index">2</sub>,&thinsp;...,&thinsp;<i>x</i><sub class="lower-index"><i>N</i></sub>)&nbsp;|&nbsp;1&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index">1</sub>&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index">2</sub>&thinsp;&le;&thinsp;...&thinsp;&le;&thinsp;<i>x</i><sub class="lower-index"><i>n</i></sub>&thinsp;=&thinsp;<i>X</i><sub class="lower-index"><i>i</i></sub>,&thinsp;</span>각 <span class="tex-span"><i>x</i></span>는 모두 자연수<span class="tex-span">}</span></center>

이제 모든 <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>i</i>&thinsp;&le;&thinsp;<i>M</i></span>)을 모아 이 점들의 집합을 <span class="tex-span"><i>S</i></span>라고 하자. 즉 <img align="middle" class="tex-formula" src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_AC/9b9aafa38e1d358b2c24a04c83104d9f56e4db5d.png"/>이다. <span class="tex-span"><i>S</i></span>에 속한 점들 중에서 <span class="tex-span"><i>N</i></span>차원 좌표계의 원점 <span class="tex-span">(0,&thinsp;0,&thinsp;...,&thinsp;0)</span>에서 보이는 점들의 개수를 구하고 싶다. 어떤 점이 보인다는 것은 원점에서 그 점까지 이은 선분 위에 원점과 그 점을 제외한 다른 점이 없다는 것이다.

### 입력 형식

첫 번째 줄에는 두 개의 자연수 <span class="tex-span"><i>N</i></span>, <span class="tex-span"><i>M</i></span> (<span class="tex-span">1&thinsp;&le;&thinsp;?<i>M</i>&thinsp;&le;&thinsp;100,&thinsp;000</span>)이 공백으로 구분되어 주어진다.

다음부터 <span class="tex-span"><i>M</i></span> 개의 줄의 <span class="tex-span"><i>i</i></span>번째 줄에는 하나의 자연수 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span> (<span class="tex-span">1&thinsp;&le;&thinsp;<i>X</i><sub class="lower-index"><i>i</i></sub>&thinsp;&le;&thinsp;100,&thinsp;000</span>)가 주어진다. 각 <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i></sub></span>들 중에 중복되는 수는 없다.

쉬운 문제에서는 <span class="tex-span"><i>N</i>&thinsp;=&thinsp;2</span>을 만족하는 입력이 주어진다. 

어려운 문제에서는 <span class="tex-span">2&thinsp;&le;&thinsp;<i>N</i>&thinsp;&le;&thinsp;100,000</span>을 만족하는 입력이 주어진다.

### 출력 형식

주어진 점들 중에서 원점에서 보이는 점들의 개수를 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력한다.

### 예제


<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2 4<br>
1<br>
2<br>
3<br>
4<br>
</td>
   <td class="code-font">6</td>
  </tr>	
 </tbody>
</table>

좌표계에 있는 점들은 <span class="tex-span">(1,&thinsp;1),&thinsp;(1,&thinsp;2),&thinsp;(2,&thinsp;2),&thinsp;(1,&thinsp;3),&thinsp;(2,&thinsp;3),&thinsp;(3,&thinsp;3),&thinsp;(1,&thinsp;4),&thinsp;(2,&thinsp;4),&thinsp;(3,&thinsp;4),&thinsp;(4,&thinsp;4)</span>이다. 

보이는 점은 <span class="tex-span">(1,&thinsp;1),&thinsp;(1,&thinsp;2),&thinsp;(1,&thinsp;3),&thinsp;(2,&thinsp;3),&thinsp;(1,&thinsp;4),&thinsp;(3,&thinsp;4)</span>로 총 6개이다.