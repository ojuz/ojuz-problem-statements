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

<div class="row">
<div class="col-sm-9 col-md-9 col-lg-9">
<p>고메즈는 고대 유적을 탐사하다 고대인들이 사용하던 문자가 써진 비석을 발견하게 되었다. 그러나 고메즈에게는 고대 문자에 대한 지식이 아무 것도 없어서 비석을 읽을 수 없었다. 그렇기에 고대 문자에 대한 지식이 해박하여 비석을 해석해줄 수 있는 사람을 찾고 있다. 당신이 고대 문자에 대한 지식이 해박하다면 불쌍한 고메즈를 도와주자!</p>

<h3>입력 형식</h3>

<p>첫 번째 줄에는 두 개의 자연수 <span class="tex-span"><i>R, C</i></span>(<span class="tex-span">1 &le; <i>R, C</i> &le; 50</span>)이 주어진다.</p>

<p>이후 <span class="tex-span">6<i>R</i>&thinsp;-&thinsp;1</span>개의 줄에는 비석의 내용이 적혀 있다. 각 줄에는 <span class="tex-span">6<i>C</i>&thinsp;-&thinsp;1</span>개의 문자가 적혀 있으며 문자는 '<span class="code-font">#</span>' 또는 '<span class="code-font">.</span>'이다. 예제를 보고 상세한 내용을 파악할 것을 권장한다.</p>

<p>쉬운 문제에서는 출력해야 하는 문자가 '<span class="code-font">a</span>', '<span class="code-font">b</span>', '<span class="code-font">c</span>', '<span class="code-font">d</span>', '<span class="code-font">z</span>', '<span class="code-font">_</span>' 밖에 없는 입력이 주어진다.</p>

<p>어려운 문제에서는 별다른 제약조건이 없다.</p>

<h3>출력 형식</h3>

<p>비석을 해석하여 출력한다. 출력하는 방식에 대한 모든 힌트는 주어져 있다.</p>
</div>
<div class="col-sm-3 col-md-3 col-lg-3">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/kriii2_Z/img.png">
</div>
</div>

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">3 4<br>
#####.#####.#####......<br>
#.#.#...#...#####......<br>
#.###.#...#.#####......<br>
#...#.#####.#...#......<br>
#####.#####.#.#.#......<br>
.......................<br>
#####.......#####.#####<br>
###.........#...#.#.#.#<br>
###.#.......#.#.#.#####<br>
###.........#.#.#.#.#.#<br>
#####.......#####.#####<br>
.......................<br>
#####.#####.......###.#<br>
#####.#...#.......###.#<br>
#####.#.#.#.......###.#<br>
..###.....#.......#...#<br>
#.###.#####.......#.###
</td>
   <td class="code-font">_10kq<br>
uv3_<br>
a_b<br>
3cd
</td>
  </tr>
 </tbody>
</table>