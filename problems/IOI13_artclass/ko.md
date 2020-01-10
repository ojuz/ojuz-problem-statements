#### 채점을 위한 추가 설명 (편집자 주)

안타깝게도 공식 그레이더의 `jpeglib.h` 파일은 윈도우에 존재하지 않는 것 같습니다. 그래서 모든 예제는 jpg 파일과 이를 텍스트 파일 형태로 치환한 txt 파일을 모두 제공하며, 그레이더는 `jpeg` 형식의 이미지 `artclass.jpg`를 입력받는 공식 그레이더 `grader.c`와 텍스트 파일 `artclass.txt`를 입력받는 `gradertxt.c`를 제공합니다. 

추가로 설명하자면, grader.zip은 아래와 같이 구성되어 있습니다.

* `images` 폴더 안 : 각 스타일에 따라 `style-X`라는 폴더가 있고, 이 폴더 안에는 `style-X-Y.jpg`와 `style-X-Y.txt`의 형태를 갖는 파일들이 각각 9개씩 존재합니다. 같은 이름을 가진 파일은 서로 같은 그림입니다. (예로, `style-1-1.jpg`와 `style-1-1.txt`는 같은 그림입니다.)

* `jpg` 폴더 안 : `artclass.jpg`를 입력받는 그레이더 `grader.c`를 이용하기 위한 모든 파일이 담겨져 있습니다.

* `txt` 폴더 안 : `artclass.txt`를 입력받는 그레이더 `gradertxt.c`를 이용하기 위한 모든 파일이 담겨져 있습니다. `artclass.txt`의 입력 형식은 아래와 같습니다.
  - Line 1: `H W`
  - Line `i*H+j+2` (`0 ≤ i ≤ H-1`, `0 ≤ j ≤ W-1`): `R[i][j] G[i][j] B[i][j]`


{{viewpdf:statement_ko}}