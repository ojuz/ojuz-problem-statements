$a$의 거듭제곱 $a^{b}$를 편하게 $pow_{a}(b)$라고 나타내어 보자.

그리고 $pow_{a}^{0}(a) = a, pow_{a}^{k+1}(a) = pow_{a} (pow_{a}^{k}(a)) (k \ge 0)$라고 하자.

우리의 일은 $a$와 $k$가 주어질 때 $pow_{a}^{k}(a)$를 계산하는 것이다. 즉

<center><span style="font-size: 25px;">$a^{a^{a^{a^{a^{...^{{...}^{{a}^{a}}}}}}}}$</span> ($a$가 $k+1$개)</center>

을 계산하는 것이다. 주의해야 할 점은 만약 $k = 3$이라고 할 때

<center>$(a^{a})^{a} \neq a^{(a^{a})}$</center>

라는 것이다. 우리가 구하는 것은 후자이다.

### 입력 형식

첫 번째 줄에 $a$와 $k$ $(1 \le a \le 10^{9}, 0 \le k \le 10^{9})$가 공백으로 구분되어 주어진다.

### 출력 형식

$pow_{a}^{k}(a)$의 값을 출력한다. 답이 매우 커질 수 있으므로 답을 $a+1$로 나눈 나머지를 출력한다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>예제 입력</th>
   <th>예제 출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2 3</td>
   <td class="code-font">1</td>
  </tr>
 </tbody>
</table>

$pow_{2}^{3}(2) = 2^{2^{2^{2}}} = 65,536$이므로, 이를 $3$으로 나눈 나머지인 $1$을 출력한다.