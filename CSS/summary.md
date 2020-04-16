## CSS (Cascading Style Sheets)
  
 ***
  
#### * 구조  

```
article{
    fontfamily:'맑음 고딕';  
    font-size: 16px;
    color:blue;
}
```

##### 1. 선택자(Selector)  
: HTML의 ```<article>``` 태그를 가리키고 있는 article을 말한다. 스타일을 지정할 특정 HTML 요소를 선택하는 역할을 수행한다. 
> ','로 여러 개의 스타일을 한꺼번에 지정할 수 있다.
```
h1, p {
    color:red;
}
```

##### 2. 속성(Property)  
: ```font-family```, ```font-size```에 해당하는 부분이며 지정, 변경하고 싶은 스타일 속성의 이름이다.  
> _font-size, color, background, position 등 다양한 요소를 사용할 수 있다._  
  
##### 3. 값(Value)  
: ```16px```, ```blue```에 해당하는 부분이며 값은 일반적으로 CSS에 정의된 특정 키워드(blue, block 등)과 수치와 특정 단위(px, %, em, rem, vh, vw 등)으로 나뉜다.  
> _값은 프로퍼티와 짝을 이루어 사용한다.(<b>선언</b>) 각 프로퍼티에 허용되는 값의 종류가 정해져 있다._
  
##### 4. 선언 블록(Declaratio Block)  
: {} 안의 한 덩어리를 말한다. 각각 적혀 있는 선택자에 한해 스타일이 적용된다. 선언 블록 내부의 다른 선언과 ;로 구분한다.  



#### * 기본 단위  

##### 1. 고정 크기 단위  
* ```px``` : pixel, 디스플레이를 구성하는 최소 단위  
* ```pt``` : point  
* ```in``` : inch  
* ```cm```, ```mm```  
  
##### 2. 가변 크기 단위  
* ```em``` : 현재 스타일이 지정되는 요소의 폰트 크기를 기준으로 설정한다.  
* ```rem``` : 최상위 요소의 폰트 크기를 기준으로 설정한다.  
>  _습관적으로 rem을 사용할 것_  
* ```%``` : 이미지나 레이아웃의 너비나 높이를 지정할 때 자주 쓰인다.  
  

#### * 색상  

##### 1. 키워드  
내부적으로 지정되어 있는 키워드를 쓴다. 다른 방식에 비해 수가 제한적이다.  

##### 2. RGB  
빛의 3원색인 빨,초,파를 혼합하여 색을 표현한다. 0~255값으로 나타낸다.  

##### 3. HEX Code  
16진수 6자리 코드로 색상을 표현한다.  
``` 
#FF0000 = 빨간색, #800080 = 보라색  
```
##### 4. Alpha  
투명도를 말한다.  
```
RGB에서
rgba(23,41,13,0.5)  
  
HEX Code에서  
#23fe4e55 
```  


#### * 선택자  
  
##### 1. 단순 선택자  

* ```타임 선택자``` : 해당 태그를 가지는 모든 요소에 스타일을 적용한다. 
```
<h1> 저는 h1 태그입니다. </h1>  
<p> 저는 p 태그입니다. </p>  
```

* ```아이디 선택자``` : 아이디 이름으로 스타일을 적용한다.  
```
<p id="goorm"> 저는 p 태그입니다. </p>
  
#goorm{
    background-color: blue;
}
```

* ```클래스 선택자``` : 비슷한 특징을 갖는 요소를 지정하여 묶어 그룹으로 만들 수 있다.  
```
<p class="student"> 학생</p>
<p class="teacher"> 선생님</p> 
  
.student{
    color:white;
}
.teacher{
    color:black;
}
```

* ```전체 선택자``` : 모든 요소에 스타일을 적용한다. 모든 요소에 적용시키기 때문에 속도가 저하될 수 있다. 선택자 자리에 *를 입력하면 된다.  

```
*{
    color:yellow;
}
```
  
* ```속성 선택자``` : 특정 HTML 속성을 가지고 있는 모든 요소에 스타일을 적용한다. 선택자 오른쪽에 []로 속성과 속성값을 넣으면 된다.  

```
선택자[속성명="속성값"]{
    color:pink;
}
```
  
##### 2. 복합 선택자  

* ``` 부모 - 자식 - 후손 요소```  : 관계는 상대적이다. 상위 태그가 부모태그, 하위 태그가 자식태그가 된다.  
*  ```자식 선택자``` : 선택자 A의 모든 자식 중 선택자 B와 일치하는 요소를 선택한다. 자식 선택자는 복합 선택자이기 때문에 선택자를 두 개 사용하며 '>'를 써준다. 바로 하위에 해당하는 자식 요소에만 스타일을 적용하고 싶을 때 사용한다.  
```
div > p {
    color:green;
}
``` 

* ``` 후손 선택자``` : 선택자 A의 모든 후손 중 선택자 B와 일치하는 요소를 선택한다. 중간에 띄어쓰기를 사용한다. #me 밑의 모든 태그가 선택됨
```
div p {
    color:yellow;
}
```  

* ```가상 클래스 선택자```  
가상 클래스 : 직접 정의할 수 없고 실제 HTML에 보이지 않는다.  
```
선택자:pseudo-class{
    color:red;
}
```
가장 대표적인 가상 클래스는 <font color="red">링크 태그</font>와 관련됐다.  

>   - a:link : 방문하지 않은 링크일 때
>   - a:visited : 방문한 링크일 때  
>   - a:hover : 링크에 마우스를 올렸을 때  
>   - a:active : 선택된 링크일 때  


#### * 박스 모델  
: 박스 형태를 만들 때 쓴다. 내용(Content), 패딩(Padding), 경계선(Border), 마진(Margin)으로 구성된다.  

##### 1. 내용(Content) : 실제로 내용을 담고 있는 부분

보통 요소의 크기를 정할 때 width나 height를 많이 사용한다. 이런 너비와 크기는 content의 크기에 해당한다.
>   _개발자 도구 > inspect > #inner로 크기 확인_ 
```
#inner{
    background-color:pink;
    width:200px;
    height:100px;
} 
```

##### 2. 경계선(Border) : 컨텐츠를 감싸고 있는 테두리   

경계선은 세 프로퍼티인 border-style, border-width, border-color를 사용한다.  
```
<div id="main">
	<div class="inner">
		TOP
	</div>
	<div class="inner" id="target">
		DOWN
	</div>
</div>  

body { background-color: skyblue; }
.inner {
    background-color: pink;
    width: 200px;
    height: 100px;
}
#target {
	border-color: black;
	border-style: solid;
	border-width: 8px;
}
```
_#target에 검은 테두리가 생김_  

* ```border-style``` : 선의 종류를 지정하는 프로퍼티.  
```none```, ```hidden```, ```dotteed```, ```dashed```, ```solid```, ```double```, ```groove```, ```ridge```, ```inset```, ```outset```, ```initial```, ```inherit```  
  
```
#target{
    border-style : solid dashed dotted double;
}
```
_top, right, bottom, left 순서로 스타일이 지정됨_  

>   1개 : 상하좌우, 2개 : 상하/좌우, 3개 : 상/좌우/하, 4개 : 상/우/하/좌  

* ```border-width```, ```border-color``` : 선의 두께와 색 지정하는 프로퍼티. border-style 없이 지정했을 때에는 적용되지 않는다.  

>   ```shortcut``` : 한 번에 지정할 수 있다.  
```border:red solid 1px;```  

* ```border-radius``` : 경계선을 둥글게 표현할 때 사용한다.   
```
<div id="main">
	<div class="box radius">border-radius</div>
</div>
```  
_border-radius의 값은 모서리의 반지름의 값_  
_border-radius는 테두리 존재 여부와 별개로 전체 백그라운드에 적용된다._  

_```shortcut``` : 한 번에 지정하거나 네 방향으로 나눠 부분적으로 적용가능.  
4등분으로 나눠서 top-left, top-right, bottom-right, bottom-left 순서로 적용된다._  
 _타원형의 radius를 적용할 때에는 가로 반지름, 세로 반지름 순서로 적용된다_  

##### 3. 패딩(Padding) : 컨텐츠와 경계선 사이의 여백  
_top, right, bottom, left 순서로 스타일이 지정됨_  

##### 4. 마진(Margin) : 경계선 밖의 여백  
_top, right, bottom, left 순서로 스타일이 지정됨_

* ```마진 상쇄``` : 위아래로 맞닿은 두 요소 사이의 마진은 더 큰 쪽을 기준으로 결정된다. 각각 마진을 따로 적용하더라도 서로 맞닿아 있다면 마진이 따로 존재하지 않는다는 말이다.  

##### 5. box-sizing  
box-sizng: content-box; 는 컨텐츠박스를 기준으로 크기를 정하지만, box-sizing: border-box;의 크기는 border 바로 전 padding까지를 기준으로 정해진다.  
  
```box-sizing:content-box;``` : width(height) = content size  
```box-sizing:border-box;``` : width(height) = content size + padding + border size  

#### * 글자 관련 스타일  

##### 1. 폰트 종류와 웹 폰트  

* ```font-family```

한 단어로 구성된 폰트명은 따옴표 없이 사용할 수 있지만, 띄어쓰기나 '-'가 들어간 폰트명은 따옴표를 사용해야 한다.  
```
font-family : '폰트이름1' '폰트이름2';
```  
_모든 이용자의 기기에 동일한 폰트가 없을 수도 있기 때문에 폰트를 여러 개 지정하여 앞 순서에 위치한 폰트부터 차례로 적용한다._
> 가장 보편적으로 사용하는 글꼴 : Sans-serif, Serif, Cursive, Fantasy, Monospace  

* ```Web Font``` : 링크를 통해 폰트를 불러오는 방식  

##### 2. 폰트의 크기와 형태  

* ```font-style``` : normal, italic, oblique 등이 있다.  
* ```font-weight``` : 폰트 굵기를 지정할 때 사용한다.  
>   bold나 100~900까지의 숫자 중 100 단위의 숫자값을 사용할 수 있다. _normal은 400, bold는 700_  
```
font 프로퍼티를 사용하면 모든 과정을 한 번에 사용 가능하다.  
  
font-style, font-weight, font-size, font-family를 순서대로 띄어쓰기로 구분하여 사용해야 함  
```  

##### 3. 텍스트 정렬  

* text-align : 좌, 우, 중앙 정렬할 때 사용한다.  
```
<h1>텍스트 정렬</h1>
<p id="right">오른쪽 정렬</p>
<p id="middle">가운데 정렬</p>
<p id="left">왼쪽 정렬</p>
```  
>   _```justify``` : 좌우로 띄어쓰기를 늘려 붙인다._  

* ```line-height``` : 문장 사이의 간격을 조정한다. 단위가 존재하는 값 또는 단위가 없는 숫자 값으로 높이를 조정한다. 단위 없는 숫자 값은 해당 요소의 font-size를 기준으로 한 배수로 높이를 조정한다. 
```
.line-height : 2;
```
```
.line-height : 30px;  
``` 

> _글자의 하단부 사이의 거리가 아닌 그 글자 라인의 높이를 말한다_  

* ```letter-spacing``` : 자간(각 글자 사이의 간격)을 조정한다.  
```
letter-spacing : 5px;
```  

*``` text-indent``` : 문단의 시작부에 들여쓰기를 지정한다.  
```
text-indent : 16px;
```  

#### * 위치 정렬  
  
##### 1. block과 inline  

* ```display``` : 요소가 보여지는 방식을 지정하는 프로퍼티.  

* ```display:block``` : 항상 새로운 줄에서 시작하며, 따로 너비를 지정하지 않아도 width:100%을 기본 값으로 가진다.
_div, h1~h6, p, header, footer, section 등이 해당된다._  

* ```display:inline``` : block과 달리 새로운 줄에서 시작하지 않으며 필요한 만큼의 너비만 가진다. = 요소의 컨텐츠 크기만큼만 너비를 가진다.  
_span, a, img 등이 해당된다._  

>   block은 전체 문단과 같이 큰 맥락을 가질 때 사용하는 반면, inline은 그 안에 들어가는 단어, 링크, 이미지 등에 쓰인다.  ```block은 width, height, margin, padding 등을 모두 사용할 수 있지만, inline은 지정할 수 없다.```  
  
##### 2. inline-block  
  
```display:inline```에서 width, height, margin-top, margin-bottom 프로퍼티가 적용되지 않아 불편한 것을 해결하기 위해 ```display: inline-block```을 사용한다.  
  
* ```display: lnline-block``` : block과 inline 요소의 특징을 모두 가진다. 쓰임은 inlie과 동일하지만, 사용할 수 없었던 width, height, margin-left, margin-right을 지정할 수 있다.  

* ```display:none``` : 브라우저에 해당 요소가 출력되지 않는다.  

##### 3. position  
: 요소를 배치하는 방법을 정하는 프로퍼티  

* ```position:static``` : 요소의 position 값은 static이 기본이다. static에서는 좌표 프로퍼티를 사용할 수 없다.  
_좌표 프로퍼티 : top, right, botto, left_  

* ```position:relative``` : 상대 위치. 좌표 프로퍼티를 사용할 수 있는 점만 static과 다르다.  

* ```position:absolute``` : 절대 위치. 부모 요소나 조상 요소 중 relative, absolut, fixed가 선언된 곳을 기준으로 좌표 프로퍼티가 작동한다.  

* ```position:fixed``` : 보이는 화면을 기준으로 좌표 프로퍼티를 이용하여 위치를 고정시킨다.
>   _스크롤할 때 따라다니는 메뉴_  

* ```z-index``` : 수직으로 어떻게 쌓이는지를 정하는 프로퍼티로 값은 숫자로 표현된다. 숫자가 클수록 전면에 출력된다. static을 제외한 요소에서만 적용된다.  

##### 4. float  
: 요소를 어떻게 띄울지 결정한다. 요소를 디자인의 흐름에서 벗어나게 한 뒤, 사용자가 지정한 방향에 배치하도록 하는 프로퍼티다.  


#### * 위치 정렬 - flexbox  
: flexbox는 부모요소인 flex container와 자식요소인 flex item으로 구성되어 있는데, 부모요소와 자식요소는 사용할 수 있는 프로퍼티가 다르다.  
 
>   flexbox를 사용하려면 정렬하고자 하는 요소의 부모요소인 flex container에 ```display: flex;```를 추가하면 된다.  

>   ```flexbox``` : 가로 혹은 세로로 정해둔 방향을 기준으로 프로퍼티를 정렬, 줄을 세운다는 것이 핵심이다.  

##### 1. flex container : 방향과 흐름  

* ```flex-direction``` : flex container 안에서 flex item이 배치될 기본 방향을 정할 수 있다. 이 프로퍼티를 따로 지정하지 않으면 ```row```라는 값으로 기본 설정되며 ```item```은 왼쪽에서 오른쪽으로 정렬한다.  
>   _row는 가로방향, column은 세로방향_  
```
.container {
	background-color: skyblue;
	padding: 16px;
	display: flex;
	flex-direction: column; /* column은 세로방향, row는 가로방향 */
}
```  

>   row, column 이외에 ```row-reverse```와 ```column-reverse```도 사용가능한데, 이는 각각 row와 column의 역순으로 item을 정렬한다.  

* ```flex-wrap``` : flex item이 여러 줄에 걸쳐지지 않고 한 줄에 들어가도록 정렬된다. 위의 예시에서 .container의 width를 줄이면, 기존에 .item에 정의되어 있던 width는 무시되고 부모 요소인 .container의 너비에 맞춰 줄어든다.  

>   flex item들을 여러 줄에 나열하고 싶다면 ```flex-wrap```프로퍼티를 사용하면 된다.  
  
* ```flex-flow``` : ```flex-direction```과 ```flex-wrap```을 한번에 지정할 수 있다. ```flex-flow```의 값으로 direction과 wrap을 순서대로 써주면 된다.  


##### 2. flex container : 정렬1  

```justify-content``` : flex-direction으로 정해진 방향에 flex item들을 어떻게 정렬할 것인지를 결정한다.  

```
flex-direction : row;

flex-direction : column;
```

* ```flex-start```, ```center```, ```flex-end```  
: flex-direction이 row일 때는 각각 왼쪽 끝, 가운데, 오른쪽 끝을 기준으로 정렬한다. column일 때는 각각 위 끝, 가운데, 아래 끝을 기준으로 정렬한다.  

* ```space-between``` : 시작과 끝을 기준으로 하여 item들을 동일한 간격으로 배치한다.  

* ```space-around``` : 시작과 끝에 item을 하나씩 두고 그 사이 남은 공간을 동일한 간격으로 나눠 나머지 item을 배치한다.  


##### 3. flex container : 정렬2  

```align-items```는 ```justify-content```와 달리 item을 ```flex-direction```에서 정해진 방향의 <br>수직방향<br>으로 정렬한다.  

* stretch : ```align-items```가 기본 값으로 가진다. 별다른 크기가 지정되지 않았을 때 flex 아이템을 늘려서 맞춰준다.  

>   _```align-itmes: flex-start```를 추가하면 높이가 콘텐츠의 크기만큼으로 바뀐다.  

* ```flex-start``` : 수직이 시작하는 부분부터 정렬한다.  

* ```center``` : 가운데 위치에 정렬한다.  

*  ```flex-end``` : 수직이 끝나는 부분부터 정렬한다.  

* ```baseline``` : ```justify-content```와 ```align-items``` 모두에서 사용할 수 있는 값이다. 글꼴의 기준선인 baseline을 기준으로 flex item들을 정렬한다. 만약 서로 다른 크기의 글자들에 적용해야 할 경우 baseline을 기준으로 맞춘다.  

##### 4. flex container : 정렬3  

```align-content```는 flex item들이 여러 줄일 경우 ```flex-direction```방향을 기준으로 수직 정렬 방법을 결정한다.  

* ```stretch``` : 기본값. 
* ```flex-start``` : 시작 부분에 맞춰서 정렬  
* ```center``` : 가운데 정렬  
* ```flex-end``` : 끝 부분에 맞춰서 정렬  
   
![b430a583955c4b129e3aa25285d27d37142eea704e89e36731096fb8cc1e2173](https://user-images.githubusercontent.com/58182440/79418789-6b761200-7ff0-11ea-9edc-2a87fab5b4d7.png)
 
![e4bdfb5b1350631110bdba4a5d78506602851382e7f4c96c92bf8a83902b369e](https://user-images.githubusercontent.com/58182440/79418885-9f513780-7ff0-11ea-917d-9f86999d5c2c.png)


>   코드에서 align-content를 쓰기 위해서는 ```flex-wrap:wrap```이 꼭 포함되어야 한다.  
>   >   ```align-content```는 여러 줄에 걸친 item들이 한 몸처럼 움직이고, ```align-items```는 각 줄이 따로 나누어져 정렬된다.  

* ```space-between``` : 수직 방향으로 끝과 끝에 하나씩 기준을 두고 그 사이에 배치한다.  

* ```space-around``` : 모든 간격을 동일하게 배치한다.  

##### 5. flex item  
  
flex item의 프로퍼티는 ```display:flex```가 적용된 부모 요소의 자식 요소에만 사용할 수 있다.  
  
* ```flex-grow``` : flex item의 확장과 관련된다.  단위 없는 숫자 값(비율)을 사용하며 기본값은 0이다.  값이 0일 경우에 flex container가 커져도 flex item의 크기는 커ㅣ지 않고 원래 크기를 유지하지만, 값이 1 이상일 경우에 flex item의 원래 크기와 상관 없이 flex container를 채우기 위해 flex item도 커지게 된다.  
  

  




