# problem-statements

문제 번역을 용이하게 하기 위한 프로젝트입니다. [oj.uz](https://oj.uz)와 이 github 프로젝트가 동기화되도록 설정되어 있기 때문에, 여기서 pull request를 날리시면 운영진이 검토 후 commit을 할 것이며, 그 결과 수정하신 내용이 반영될 것입니다. 

모든 문제는 Markdown으로 작성되어 있습니다.

## oj.uz 전용 문법

oj.uz에서는 유효하지만 github에서는 유효하지 않은 문법들입니다.

* `{{viewpdf:$NAME}}`: 문제 첨부 파일 폴더에 있는 `$NAME.pdf` 파일을 뷰어로 보여줍니다.
* `$..$` or `$$..$$`: Mathjax 수식입니다.

## 고쳐야 할 문제점 목록

* 코드 블럭: 여러 줄의 코드 블럭을 작성할 때 코드 블럭을 여는 <code>\`\`\`</code> 뒤에 "c++"과 같이 언어를 적어주지 않으면 Markdown이 깨지는 현상이 발생하고 있습니다. 아래와 같이 작성해야 합니다.
	<pre>\`\`\`c++
	void init(int x, int y);
	\`\`\`</pre>
* 장기적으로 Mathjax에 대한 의존도를 줄여나갈 생각입니다.
