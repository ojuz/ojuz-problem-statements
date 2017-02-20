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
.highlighted {
	color: #0000ff;
}
</style>

간단한 문제입니다. 정수 상수인 <span class="tex-span"><i>a1, b1, ..., an, bn</i></span>의 값이 주어질 때 아래 소스코드를 실행하면 sum변수에 최종적으로 어떤 값이 저장되는지 구해주세요.

<pre class="code-font">
<span class="highlighted">very big <span class="highlighted">int</span></span> sum = 0; 
<span class="highlighted">for</span> ( <span class="highlighted">int</span> x1 = a1 ; x1 &lt;= b1 ; x1++ ) 
    <span class="highlighted">for</span> ( <span class="highlighted">int</span> x2 = a2 ; x2 &lt;= b2 ; x2++ ) 
        .... 
            <span class="highlighted">for</span> ( <span class="highlighted">int</span> xn = an ; xn &lt;= bn ; xn++ ) 
                sum = sum + gcd(x1, x2, ..., xn);
</pre>

너무 간단한가요? 저도 그렇게 생각해요. (웃음)

여기서 gcd함수는 x1, x2, ..., xn의 최대공약수를 구하는 함수입니다.

### 입력 형식

첫 번째 줄에는 자연수 <span class="tex-span"><i>n</i></span>이 주어진다.

이후 <span class="tex-span"><i>n</i></span>개의 줄의 <span class="tex-span"><i>i</i></span>번째 줄에는 <span class="tex-span"><i>ai, bi</i></span>(<span class="tex-span">1 &le; <i>ai</i> &le; <i>bi</i> &le; 1,000,000</span>)가 공백으로 구분되어 주어진다.

쉬운 문제에서는 <span class="tex-span">1 &le; <i>n</i> &le; 10</span>인 입력이 주어진다.

어려운 문제에서는 <span class="tex-span">1 &le; <i>n</i> &le; 10,000</span>인 입력이 주어진다.

### 출력 형식

C/C++에서는 <span class="code-font highlighted">very big int</span>형 같은 좋은 변수형이 없으므로 <span class="code-font">sum</span>의 값을 <span class="tex-span">1,000,000,007</span>로 나눈 나머지를 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">3<BR>
1 7<BR>
1 5<BR>
1 3</td>
   <td class="code-font">115</td>
  </tr>
 </tbody>
</table>