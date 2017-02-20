아래 `mystery.c`는 입력파일 X를 읽어서 그 안에 기록된 $N$개의 정수를 배열 NUM에 저장한 뒤에 이 $N$개의 숫자를 어떤 순서에 따라서 화면에 출력하는 프로그램이다. `mystery.c`가 X를 입력으로 받아 화면에 출력한 결과를 Y라고 하자. 

```
#include <stdio.h>
int NUM[101] ;
FILE *fin ;
int main(){
    int i, token,N ;
    int count=0, from= 0, value ;
    fin = fopen("X","r");
    fscanf(fin,"%d",&N);
    for(i=0; i<N; i++){
        fscanf(fin,"%d",&token);
        NUM[i]= token;
    } /* end of for */
    printf("%d\n", N ) ;
    value = NUM[ from ] ;
    while( count < N ) {
        while( value == 0 ) {
            from = (from+1)%N;
            value = NUM[ from ] ;
        } /* end of inner while */
        printf("%d ", value ) ;
        count++ ;
        NUM[ from ] = 0 ;
        from = (value +from )% N ;
        value = NUM[ from ] ;
    } /* end of outer while */
    return(0);
} /* end of main() */
```

여러분은 mystery.c에서 생성된 Y를 파일로 받아서 그것의 입력에 해당하는 X를 찾아내는 프로그램을 작성해야 한다. 

### 입력 형식

첫 줄에는 정수 $N$ ($3 \le N \le 30$)이 주어진다. 그리고 두 번째 줄에는 100이하 양의 정수 $N$개가 빈칸을 사이에 두고 모두 나열되어 있다. 단 그 정수 중에는 같은 수가 있을 수도 있다.

### 출력 형식

첫 줄에는 정수 $N$이 제시되어 있고, 그 다음 줄에는 N개의 양의 정수가 빈칸을 사이에 두고 기록되어 있어야 한다. 만일 입력을 생성하는 `mystery.c`의 입력파일 X가 없는 경우에는 <u>음수인 -1 을 첫 줄에 출력하면 된다.</u>

### 부분문제의 제약 조건

* **부분문제 1**: 전체 점수 100점 중 15점에 해당하는 데이터에 대해서, $N=4$, NUM 배열의 숫자들은 4이하의 양의 정수이고 모두 한 번씩 나타난다.
* **부분문제 2**: 전체 점수의 100점 중 21점에 해당하는 데이터에 대해서, $N \le 10$, NUM 배열의 숫자들은 $N$ 이하의 양의 정수이고, 모두 한번씩 나타난다.
* **부분문제 3**: 전체 점수 100점 중 29점에 해당하는 데이터에 대해서, $N \le 20$, NUM 배열의 숫자들은 1 또는 2이다.
* **부분문제 4**: 전체 점수의 100점 중 35점에 해당하는 데이터에 대해서, $N \le 30$, NUM 배열의 숫자들은 100이하의 양의 정수이다.

### 입력과 출력의 예

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr class="code-font">
   <td style="width: 50%;">5<br/>1 2 4 3 5</td>
   <td>5<br/>1 2 3 4 5</td>
  </tr>
  <tr class="code-font">
   <td style="width: 50%;">10<br/>1 2 4 8 6 3 7 5 10 9</td>
   <td>10<br/>1 2 3 4 5 6 7 8 9 10</td>
  </tr>
  <tr class="code-font">
   <td style="width: 50%;">10<br/>5 5 7 4 33 10 9 3 2 6</td>
   <td>10<br/>5 7 33 2 6 5 10 9 4 3</td>
  </tr>
 </tbody>
</table>